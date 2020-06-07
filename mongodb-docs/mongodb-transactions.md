# mongodb-transactions

## Terms
- [Distributed Transactions and Multi-Document Transactions](https://docs.mongodb.com/manual/core/transactions/#transactions-and-atomicity)
> Starting in MongoDB 4.2, the two terms are synonymous. 
> Distributed transactions refer to multi-document transactions on sharded clusters and replica sets.
> Multi-document transactions (whether on sharded clusters or replica sets) 
> are also known as distributed transactions starting in MongoDB 4.2.

## [Overview](https://docs.mongodb.com/manual/core/transactions/)
> In MongoDB, *an operation on a single document is atomic*. 
> Because you can use embedded documents and arrays to capture relationships between data 
> in a single document structure instead of normalizing across multiple documents and collections,
> this single-document atomicity *obviates* the need for multi-document transactions 
> for many practical use cases.

> For situations that require *atomicity of reads and writes to multiple documents* 
> (in a single or multiple collections), MongoDB supports *multi-document transactions*. 
> With *distributed transactions*, transactions can be used across multiple operations, 
> collections, databases, documents, and shards.

## API Examples
- [Example using Transactions (Callback) API](https://docs.mongodb.com/manual/core/transactions/#transactions-api)
> The example uses the new callback API for working with transactions, 
> which *starts a transaction, executes the specified operations, and commits (or aborts on error)*.

- [mongo Shell Example using Transactions (Callback) API](https://docs.mongodb.com/manual/core/transactions-in-applications/#txn-mongo-shell-example)

## Specifications
### [Atomicity](https://docs.mongodb.com/manual/core/transactions/#transactions-and-atomicity)
  - When a transaction commits, all data changes made in the transaction 
    are saved and visible outside the transaction. 
    That is, a transaction will not commit some of its changes while rolling back others.
    Until a transaction commits, the data changes made in the transaction are not visible 
    outside the transaction.
    ***However, when a transaction writes to multiple shards, 
    not all outside read operations need to wait for the result of the committed transaction 
    to be visible across the shards.*** 
    For example, if a transaction is committed and write 1 is visible on shard A 
    but write 2 is not yet visible on shard B, 
    an outside read at read concern "local" can read the results of write 1 without seeing write 2.

    > Q: What kind of "atomicity" is guaranteed in distributed transactions across shards?

    > See [Outside Reads During Commit](https://docs.mongodb.com/manual/core/transactions-production-consideration/#outside-reads-during-commit)
  - When a transaction aborts, all data changes made in the transaction are discarded 
    without ever becoming visible. 
    For example, if any operation in the transaction fails, 
    the transaction aborts and all data changes made in the transaction are discarded 
    without ever becoming visible.

- [Read Concern/Write Concern/Read Preference](https://docs.mongodb.com/manual/core/transactions/#read-concern-write-concern-read-preference)
First of all, they are all *transaction-level*.

### Read Preference
> [Multi-document transactions](https://docs.mongodb.com/manual/core/transactions/#) that contain read operations must use read preference [`primary`]. All operations in a given transaction must route to the same member.

Question: What does "All operations in a given transaction must route to the same member" mean? Is it only applied to a single replica-set deployment? Is it applied to shared deployment?

### Read Concern
- `local`
- `majority`
- `snapshot`
> Read concern "snapshot" returns data from a snapshot of majority committed data 
> ***if*** the transaction commits with write concern "majority".

### Write Concern
- `w:1`
- `w:majority`

`r : majority + w : majority`:
-  When you commit with  `w:  "majority` write concern, transaction-level  `majority`  read concern guarantees that operations have read majority-committed data. 
- For transactions on sharded clusters, this view of the majority-committed data is *not* synchronized across shards.

**`r:snapshot + w:majority`:**
-   When you commit with  `w: majority` write concern and `r: snapshot` read concern guarantees that operations have from a synchronized snapshot of majority-committed data.

## Protocols
- [Section 5 of Paper MongoDB@VLDB2019]()

## Miscellaneous
- [Runtime Limit](https://docs.mongodb.com/manual/core/transactions-production-consideration/#runtime-limit)
> By default, a transaction must have a runtime of less than *one minute*. 
> You can modify this limit using `transactionLifetimeLimitSeconds` for the mongod instances. 

- [Oplog Size Limit](https://docs.mongodb.com/manual/core/transactions-production-consideration/#oplog-size-limit)
> *Starting in Version 4.2:* MongoDB creates as many oplog entries as necessary to 
> encapsulate all write operations in a transaction, 
> instead of a single entry for all write operations in the transaction. 