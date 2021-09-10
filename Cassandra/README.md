# Cassandra

## Lightweight transactions in Cassandra and Paxos
### Official Documents
- [Lightweight transactions in Cassandra 2.0 @ The DataStax Blog](https://www.datastax.com/blog/lightweight-transactions-cassandra-20)
- [Lightweight transactions @ DataStax Doc](https://docs.datastax.com/en/cassandra-oss/2.1/cassandra/dml/dml_ltwt_transaction_c.html#:~:text=Cassandra%20implements%20lightweight%20transactions%20by%20extending%20the%20Paxos,for%20a%20master%20database%20or%20%20two-phase%20commit.)
- [Using lightweight transactions @ DataStax Doc](https://docs.datastax.com/en/cql-oss/3.3/cql/cql_using/useInsertLWT.html)
- [How do I accomplish lightweight transactions with linearizable consistency @ DataStax Doc](https://docs.datastax.com/en/cassandra-oss/3.0/cassandra/dml/dmlLtwtTransactions.html)
- [issues about Paxos](https://issues.apache.org/jira/browse/CASSANDRA-5830?jql=text%20~%20%22paxos%22)
### Testing
- [Jepsen: Cassandra 2.0.0; 2013-09-24](https://aphyr.com/posts/294-call-me-maybe-cassandra)
### Videos
- [The Power of Cassandra Lightweight Transactions](https://youtu.be/KQZKIxRoreE)
- [Light Weight Transactions Under Stress by Christopher Batey, The Last Pickle @ Cassandra Summit 2016](https://youtu.be/wcxQM3ZN20c)
- [Lightweight Transactions in Scylla versus Apache Cassandra](https://youtu.be/IaJIsMApvN0)
### Blog Articles
- [深入解析cassandra 轻量级事务原理 @ aliyun; 2019](https://developer.aliyun.com/article/714656)
- [Apache Cassandra: The Truth Behind Tunable Consistency, Lightweight Transactions & Secondary Indexes @ yugabyteDB; 2018](https://blog.yugabyte.com/apache-cassandra-lightweight-transactions-secondary-indexes-tunable-consistency/)
  - 提到了社区改进: 使用 EPaxos 代替 Paxos
- [Cassandra lightweight transactions; 2016](http://www.beyondthelines.net/databases/cassandra-lightweight-transactions/)
### Other Databases Supporting LWT
- [Getting the Most out of Lightweight Transactions in Scylla](https://www.scylladb.com/2020/07/15/getting-the-most-out-of-lightweight-transactions-in-scylla/)
  - 对比了 Scylla 与 Cassandra 对 LWT 的支持情况
- [Lightweight Transactions Under the Hood](https://university.scylladb.com/courses/data-modeling/lessons/lightweight-transactions/topic/lightweight-transactions-under-the-hood/)

### Extension
- LWT in Theory and Practice