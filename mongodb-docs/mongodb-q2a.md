# mongodb-q2a

## Programming over MongoDB
- Tunable Consistency
- Causal Consistency
  - See [causal-consistency-examples @ client-session](https://docs.mongodb.com/manual/core/read-isolation-consistency-recency/#causal-consistency-examples).

## Causal Consistency Protocol

### Code
> [Database Commands](https://docs.mongodb.com/manual/reference/command/)
- Find the source code for "client sessions"
  - [Session](https://docs.mongodb.com/manual/reference/method/Session/)
- Find the source code for "read"
  - On primary
    - ClusterTime
    - OperationTime (what is this?)
  - On secondary
    - ClusterTime (what is this?)
    - OperationTime (what is this?)
- Find the source code for "write"
  - Return ClusterTime = OperationTime?
- Find the source code for "replication"
  - Only `oplog` vs. `ClusterTime` included?