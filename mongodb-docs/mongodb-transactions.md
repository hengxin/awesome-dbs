# mongodb-transactions

## [Transactions](https://docs.mongodb.com/manual/core/transactions/)

### Overview
> In MongoDB, *an operation on a single document is atomic*. Because you can use embedded documents and arrays to capture relationships between data in a single document structure instead of normalizing across multiple documents and collections, this single-document atomicity *obviates* the need for multi-document transactions for many practical use cases.

> For situations that require *atomicity of reads and writes to multiple documents* (in a single or multiple collections), MongoDB supports *multi-document transactions*. With distributed transactions, transactions can be used across multiple operations, collections, databases, documents, and shards.

### Examples
- [Example using Transactions (Callback) API](https://docs.mongodb.com/manual/core/transactions/#transactions-api)
- [mongo Shell Example using Transactions (Callback) API](https://docs.mongodb.com/manual/core/transactions-in-applications/#txn-mongo-shell-example)

### Specifications (VERY IMPORTANT)
- [Read Concern/Write Concern/Read Preference](https://docs.mongodb.com/manual/core/transactions/#read-concern-write-concern-read-preference)
First of all, they are all *transaction-level*.

#### Read Preference
> [Multi-document transactions](https://docs.mongodb.com/manual/core/transactions/#) that contain read operations must use read preference [`primary`]. All operations in a given transaction must route to the same member.

Question: What does "All operations in a given transaction must route to the same member" mean? Is it only applied to a single replica-set deployment? Is it applied to shared deployment?

#### Read Concern
- `local`
- `majority`
- `snapshot`

#### Write Concern
- `w:1`
- `w:majority`

`r : majority + w : majority`:
-  When you commit with  `w:  "majority` write concern, transaction-level  `majority`  read concern guarantees that operations have read majority-committed data. 
- For transactions on sharded clusters, this view of the majority-committed data is *not* synchronized across shards.

**`r:snapshot + w:majority`:**
-   When you commit with  `w: majority` write concern and `r: snapshot` read concern guarantees that operations have from a synchronized snapshot of majority-committed data.

### Protocols
- [Section 5 of Paper MongoDB@VLDB2019]()
