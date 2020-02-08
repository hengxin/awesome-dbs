# mongodb-replication

## [Replication](https://docs.mongodb.com/manual/replication/)

- [Replica Set Oplog](https://docs.mongodb.com/manual/core/replica-set-oplog/#replica-set-oplog)
> The [oplog](https://docs.mongodb.com/manual/reference/glossary/#term-oplog) (operations log) is a special *capped* (fixed-sized) collection that keeps a *rolling* record of all operations that modify the data stored in your databases.
    
  - [term: oplog]([https://docs.mongodb.com/manual/reference/glossary/#term-oplog](https://docs.mongodb.com/manual/reference/glossary/#term-oplog))
    > A copped collection that stores an *ordered* history of logical writes to a MongoDB database. The oplog is the basic mechanism enabling *replication* in MongoDB.

> MongoDB applies database operations on the *primary* and *then* records the operations on the primary’s oplog. The secondary members then *copy and apply* these operations in an asynchronous process. All replica set members contain a copy of the oplog, in the `local.oplog.rs` collection, which allows them to maintain the current state of the database.

Note: The operations are applied *before* they are recorded in the primary's oplog.

> To facilitate replication, all replica set members send heartbeats (pings) to all other members. Any  secondary member can import oplog entries *from any other member*.

> Each operation in the oplog is  *idempotent*. That is, oplog operations produce the same results whether applied once or multiple times to the target dataset.

Question: How is *idempotent* achieved?
Answer: See Section 3.3.2 (Page 11) of "Master Thesis 2017: Serializability Checking for MongoDB Clients."

- [Replica Set Configuration](https://docs.mongodb.com/manual/reference/replica-configuration/index.html)

> You can access the configuration of a replica set using the `rs.conf()` method or the `replSetGetConfig` command.

Example: -   [Replica Set Configuration Document Example](https://docs.mongodb.com/manual/reference/replica-configuration/index.html#replica-set-configuration-document-example)

> To modify the configuration for a replica set, use the `rs.reconfig()` method, passing a *configuration document* to the method.

- [Replication Commands](https://docs.mongodb.com/manual/reference/command/nav-replication/)

- [Replica Set Data Synchronization](https://docs.mongodb.com/manual/core/replica-set-sync/index.html)

> In order to maintain up-to-date copies of the shared data set, secondary members of a replica set sync or replicate data from other members. MongoDB uses two forms of data synchronization: *initial sync* to populate new members with the full data set, and *replication* to apply ongoing changes to the entire data set.

- [Initial Sync: Resync a Member of a Replica Set](https://docs.mongodb.com/manual/tutorial/resync-replica-set-member/)
    > A replica set member becomes “stale” when its replication process falls so far behind that the primary *overwrites* oplog entries the member has not yet replicated. The member cannot catch up and becomes “stale.” When this occurs, you must completely resynchronize the member by *removing* its data and performing an initial sync.
- [Replication: ](https://docs.mongodb.com/manual/core/replica-set-sync/index.html#replication)
  > Secondary members replicate data continuously after the initial sync. Secondary members copy the oplog from their *sync from* source and apply these operations in an *asynchronous* process.
