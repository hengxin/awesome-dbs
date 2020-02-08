# mongodb-read-write-concerns

- [read-write-concern.rst specification](https://github.com/mongodb/specifications/blob/master/source/read-write-concern/read-write-concern.rst#read-concern)

## [Read Concern](https://docs.mongodb.com/manual/reference/read-concern/)

> The readConcern option allows you to control the consistency and isolation properties of the data 
read from replica sets and replica set shards.

## [Write Concern](https://docs.mongodb.com/manual/reference/write-concern/)

> Write concern describes the level of acknowledgment requested from MongoDB for write operations 
to a standalone mongod or to replica sets or to sharded clusters.
In sharded clusters, mongos instances will pass the write concern on to the shards.

## [Read Isolation, Consistency, and Recency](https://docs.mongodb.com/manual/core/read-isolation-consistency-recency/)

- [Real Time Order](https://docs.mongodb.com/manual/core/read-isolation-consistency-recency/#real-time-order)

> For read and write operations *on the primary*, 
issuing read operations with "linearizable" read concern and write operations with "majority" write concern 
enables multiple threads to perform reads and writes on a single document 
as if a single thread performed these operations in real time; 
that is, the corresponding schedule for these reads and writes is considered linearizable.

- [Causal Consistency](https://docs.mongodb.com/manual/core/read-isolation-consistency-recency/#causal-consistency)

> With causally consistent sessions, 
MongoDB executes causal operations in an order that respect their causal relationships, 
and clients observe results that are consistent with the causal relationships.

- [IMPORTANT: Causal Consistency and Read and Write Concerns](https://docs.mongodb.com/manual/core/causal-consistency-read-write-concerns/)

> With MongoDB’s causally consistent client sessions, 
different combinations of read and write concerns provide different causal consistency guarantees. 

> If causal consistency *implies durability*, then, as seen from the table, 
only read operations with "majority" read concern and write operations with "majority" write concern 
can guarantee all four causal consistency guarantees. 

> If causal consistency does *not imply durability* (i.e. writes may be rolled back), 
then write operations with { w: 1 } write concern can also provide causal consistency.
