
# questions about MongoDB

## Architecture
- What is the relationship among "client", "shell" and "driver"?
	- (Page 642, System Model Section) "client" refers to the application processe, which communicates with one or more MongoDB deployments via a "driver".
	-  "shell" refers to the mongo shell which is used to query and update data as well as perform administrative operations.
## Protocols
### Causal Consistency Protocol
#### `get`
- Page 649 of MongoDB@SIGMOD2019:
  - (7.) The result is returned to the client (in this example it is *`empty`*??? because the data it searches for is not on Shard B).
	  - yes
  - What to return??? 
	  - (empty, ct, aot)
#### `put`
- Page 649 of MongoDB@SIGMOD2019:
  - (4.) The client *conditionally updates*??? its local value of the `lastOperationTime` with the returned `operationTime` value	
	- I think the returned `operationTime` value must be greater than the local value of `lastOperationTime`  if there is no error.

#### `no-op` writes
- What are the parameters of `no-op-write-request`?
  - `clusterTime`?
  - `last operation time`?
  - others???
	  - clustertime and last applied time
- periodically for primary??? 
	- yes (referring to the specification on the github)
#### Replication
- What are the parameters of `pull-oplog-request`?
  - `clusterTime`?
  - `last applied time`?
  - others ???
	  - I simplify the arguments with only cluster time and last applied time if there is no error, like pulling from a node which has a different configuration version from the sender. Other arguments includes configuration version, id of the shard, id of the sender, etc.
- What are the parameters of `pull-oplog-reply`?
  - `clusterTime`? yes
  - partial `oplog` 
	  - It includes several interval `FindMore` commands to achieve data batches. 
  - others ???
	  - Similar to `pull-oplog-request`
