# Transactions

# [YCQL Transactions](https://docs.yugabyte.com/preview/api/ycql/dml_transaction/)
- > select `writetime`
## [Transactions](https://docs.yugabyte.com/preview/explore/transactions/)
	- [Distributed Transactions](https://docs.yugabyte.com/preview/explore/transactions/distributed-transactions-ysql/)
	  > The following diagram shows the sequence of events that occur when a transaction is running:
	- [Isolation levels: Serializable, Snapshot, and Read committed isolation in YugabyteDB](https://docs.yugabyte.com/preview/explore/transactions/isolation-levels/)
	  > The Snapshot isolation level is only aware of data committed before the transaction began (in other words, it works on a snapshot of the table). Transactions running under Snapshot isolation are not aware of either uncommitted data or changes committed during transaction execution by other concurrently running transactions.
	- [Explicit Locking: Row locking in YugabyteDB](https://docs.yugabyte.com/preview/explore/transactions/explicit-locking/)