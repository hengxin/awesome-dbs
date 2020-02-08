# mongodb-causal-consistency

## Papers
- [SIGMOD2019: Implementation of Cluster-wide Logical Clock and Causal Consistency in MongoDB](https://dl.acm.org/citation.cfm?id=3314049)

## Videos
- [Implementation of Cluster-Wide Causal Consistency in MongoDB @ mongoDB offical site; December 14, 2017](https://www.mongodb.com/presentations/implementation-of-cluster-wide-causal-consistency-in-mongodb)
> In the new 3.6 release, MongoDB adds Causal Consistency support, 
which simplifies the task of "reading your writes", 
while maintaining the scalability and availability advantages of distributed systems.
This talk will be presented by the developer of MongoDB’s causal consistency feature. 

## Articles
- [Causal Guarantees are Anything but Casual (Aly Cabral, October 23, 2018)](https://engineering.mongodb.com/post/ryp0ohr2w9pvv0fks88kq6qkz9k9p3)
- [Causal Consistency Violation for local read/write concerns in Jepsen Sharded Cluster Test (May 2018)](https://jira.mongodb.org/browse/SERVER-35316)

> ***Response:*** We've created DOCS-11866 and updated the documentation 
to recommend read and write concern configurations that are always safe, even during network partitions. 
When used with causal consistency, the combination of read concern majority and write concern majority 
always safely delivers causal guarantees. 

## Protocols (in [`docs.mongodb.com`](https://docs.mongodb.com/manual/reference/program/mongod/#bin.mongod?searchProperty=current&query=causal%20consistency))

- [Causal Consistency in Release Notes for MongoDB 3.6](https://docs.mongodb.com/manual/release-notes/3.6/index.html#causal-consistency)

> To provide causal consistency, MongoDB 3.6 enables causal consistency in client sessions.
A causally consistent client session denotes that the associated sequence of read and acknowledged write operations 
have a causal relationship that is reflected by their ordering.
Client applications must ensure that only one thread at a time executes these operations in a client session.

### Client
- [Session](https://docs.mongodb.com/manual/reference/method/Session/index.html)
  - [`Session.advanceClusterTime(clusterTime, signature)`](https://docs.mongodb.com/manual/reference/method/Session/index.html#Session.advanceClusterTime)
    > Updates the cluster time tracked by the session.
  - [`Session.advanceOperationTime(timestamp)`](https://docs.mongodb.com/manual/reference/method/Session/index.html#Session.advanceOperationTime)
    > Updates the operation time.
  - [`Session.getClusterTime()`](https://docs.mongodb.com/manual/reference/method/Session/index.html#Session.getClusterTime)
    > Returns the *most recent cluster time* as seen by the session. Applicable for replica sets and sharded clusters only.
  - [`Session.getOperationTime()`](https://docs.mongodb.com/manual/reference/method/Session/index.html#Session.getOperationTime)
    > Returns the timestamp of *the last acknowledged operation* for the session.

> A client [can advance the cluster time and the operation time](https://docs.mongodb.com/manual/core/read-isolation-consistency-recency/#client-sessions-and-causal-consistency-guarantees) of one client session 
to be consistent with the operations of another client session.

- [SessionOptions](https://docs.mongodb.com/manual/reference/method/SessionOptions/)
  > The options for a session in the mongo shell. 
    To access the `SessionOptions` object, use the `Session.getOptions()` method.
  - `causalConsistency`
  - `readConcern`
  - `readPreference`
  - `retryWrites`
  - `writeConcern`

- [Causally Consistent Sessions](https://docs.mongodb.com/manual/core/read-isolation-consistency-recency/#client-sessions-and-causal-consistency-guarantees)

> To provide causal consistency, MongoDB 3.6 enables causal consistency in client sessions.
A causally consistent session denotes that the associated sequence of read operations with "majority" read concern *and* write operations with "majority" write concern have a causal relationship that is reflected by their ordering. 
Applications must ensure that only one thread at a time executes these operations in a client session.

1. A client starts a client session.
2. As the client issues a sequence of read with *"majority" read concern* and write operations 
(with *"majority" write concern*), the client includes the session information with each operation.
3. For each read operation with "majority" read concern *and* write operation with "majority" write concern associated with the session, 
MongoDB returns *the operation time and the cluster time*, even if the operation errors. 
The client session keeps track of the operation time and the cluster time.
4. The associated client session tracks these two time fields.

> "Majority" concerns for reads and writes are required only for *causal consistency with data durability*.
See below.

- [Read Operations and afterClusterTime](https://docs.mongodb.com/manual/reference/read-concern/#afterclustertime)

> MongoDB 3.6 introduces support for *causally consistent sessions*. 
For read operations associated with causally consistent session, 
MongoDB 3.6 introduces the `afterClusterTime` read concern option 
to be set *automatically* by the drivers for operations associated with causally consistent sessions.

> To satisfy a read request *with* an `afterClusterTime` value of T, 
a mongod must perform the request *after its oplog reaches time T*. 
If its oplog has not reached time T, the mongod must `wait` to service the request.

- [Server Parameter: `waitForSecondaryBeforeNoopWriteMS`](https://docs.mongodb.com/manual/reference/parameters/index.html#param.waitForSecondaryBeforeNoopWriteMS)
> The length of time (in milliseconds; Default: 10) that a secondary must wait if the `afterClusterTime` is greater than the *last applied time* from the oplog. After the `waitForSecondaryBeforeNoopWriteMS` passes, *if* the `afterClusterTime` is still greater than the last applied time, the secondary makes a *no-op write* to advance the last applied time.

Question: How does the secondary make a `no-op write`?

> ***Important:***
Do *not* manually set `afterClusterTime` for a read operation. 
MongoDB drivers set this value *automatically* for operations associated with causally consistent sessions. 
However, you can advance the operation time and the cluster time for the session, 
such as to be consistent with the operations of another client session.
See [causal-consistency-examples @ client-session](https://docs.mongodb.com/manual/core/read-isolation-consistency-recency/#causal-consistency-examples).

> For read operations not associated with causally consistent sessions, `afterClusterTime` is unset.

- [Isolation](https://docs.mongodb.com/manual/core/read-isolation-consistency-recency/#isolation)

> Operations within a causally consistent session are *not isolated* from operations outside the session. 
If a concurrent write operation interleaves between the session’s write and read operations, 
the session’s read operation *may* return results that reflect a write operation 
that occurred *after* the session’s write operation.

### Server
- [`db.runCommand()`](https://docs.mongodb.com/manual/reference/method/db.runCommand/)

> `db.runCommand()` runs the command in the context of the current database.
The method returns a response document that contains the following fields:
  - `ok`, 
    > A number that indicates whether the command has succeeded (1) or failed (0).
  - `operationTime`,
	> The *logical time of the performed operation*, represented in MongoDB by the *timestamp* from the *oplog entry*.  Only for replica sets and sharded clusters.
	
	The above applies to *write* operations. Below applies to *read* operations.
	> If the command does not generate an oplog entry, e.g. a *read* operation, 
	  then the operation does not advance the logical clock. In this case, `operationTime` returns:
	    - For read concern "local", ***the timestamp of the most recent entry in the oplog***.
	    - For read concern "majority" and "linearizable", the timestamp of the most recent majority-acknowledged entry in the oplog.
	> For operations associated with causally consistent sessions, 
	  MongoDB drivers use this time to automatically set the *Read Operations and afterClusterTime*.

Question: For read concern "local", `operationTime` returned is *not* the timestamp of the write from which the value is read?
  - `$clusterTime`
    > A document that returns the *signed* cluster time. Cluster time is a logical time used for ordering of operations.
    - `clusterTime`: timestamp of the *highest* known cluster time for the member.
    - `signature`: a document that contains the *hash* of the cluster time and the id of the *key* used to sign the cluster time.

## Causal Consistency in MongoDB
- [IMPORTANT: Causal Consistency and Read and Write Concerns](https://docs.mongodb.com/manual/core/causal-consistency-read-write-concerns/)

> With MongoDB's [causally consistent client sessions](https://docs.mongodb.com/manual/core/read-isolation-consistency-recency/#sessions), 
different combinations of read and write concerns provide different causal consistency guarantees. 

> If causal consistency *implies durability*, then, as seen from the table, 
only read operations with "majority" read concern and write operations with "majority" write concern 
can guarantee all four causal consistency guarantees. 

> If causal consistency does *not imply durability* (i.e. writes may be rolled back), 
then write operations with { w: 1 } write concern can also provide causal consistency.

## [Code](https://github.com/mongodb/mongo)
- [ClusterTime Increment: `reserverTicks()`](https://github.com/mongodb/mongo/blob/master/src/mongo/db/logical_clock.cpp)
- [ClusterTime Distribution: `advanceClusterTime()`](https://github.com/mongodb/mongo/blob/master/src/mongo/db/logical_clock.cpp)
- [ ] [Causally Consistent Session]()
- [ ] [READ?]()
- [ ] [WRITE?]()
- [ ] [For Appendix A2.2@SIGMOD2019]()

## TLA/TLAPS
- [mongo-repl-tla](https://github.com/tlaplus/Examples/tree/master/specifications/mongo-repl-tla)
- [tla-at-mongodb@reddit](https://www.reddit.com/r/tlaplus/comments/76zule/tla_at_mongodb/)
- [Fixing a MongoDB Replication Protocol Bug with TLA+ (TLA+ Conf, William Schultz (MongoDB), Sep, 2019)](https://conf.tlapl.us/program/williamschultz/)
