# questions about MongoDB

## Architecture
- What is the relationship among "client", "shell" and "driver"?

## Protocols
### Causal Consistency Protocol
#### `get`
- Page 649 of MongoDB@SIGMOD2019:
  - (7.) The result is returned to the client (in this example it is *`empty`*??? because the data it searches for is not on Shard B).
  - What to return??? 
#### `put`
- Page 649 of MongoDB@SIGMOD2019:
  - (4.) The client *conditionally updates*??? its local value of the `lastOperationTime` with the returned `operationTime` value
#### `no-op` writes
- What are the parameters of `no-op-write-request`?
  - `clusterTime`?
  - `last operation time`?
  - others???
- periodically for primary??? 
#### Replication
- What are the parameters of `pull-oplog-request`?
  - `clusterTime`?
  - `last applied time`?
  - others ???
- What are the parameters of `pull-oplog-reply`?
  - `clusterTime`?
  - partial `oplog` 
  - others ???

> Written with [StackEdit](https://stackedit.io/).
