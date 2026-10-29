# Cassandra

## Lightweight transactions in Cassandra and Paxos

### Official Documents

- [Lightweight transactions in Cassandra 2.0 @ The DataStax Blog](https://www.datastax.com/blog/lightweight-transactions-cassandra-20)
- [Lightweight transactions @ DataStax Doc](https://docs.datastax.com/en/cassandra-oss/2.1/cassandra/dml/dml_ltwt_transaction_c.html#:~:text=Cassandra%20implements%20lightweight%20transactions%20by%20extending%20the%20Paxos,for%20a%20master%20database%20or%20%20two-phase%20commit.)
- [Using lightweight transactions @ DataStax Doc](https://docs.datastax.com/en/cql-oss/3.3/cql/cql_using/useInsertLWT.html)
- [How do I accomplish lightweight transactions with linearizable consistency @ DataStax Doc](https://docs.datastax.com/en/cassandra-oss/3.0/cassandra/dml/dmlLtwtTransactions.html)
- [issues about Paxos](https://issues.apache.org/jira/browse/CASSANDRA-5830?jql=text%20~%20%22paxos%22)
- [Cassandra-Issues-LWT](https://issues.apache.org/jira/browse/CASSANDRA-16784?jql=project%20%3D%20CASSANDRA%20AND%20component%20%3D%20%22Feature%2FLightweight%20Transactions%22)

### Testing

- [Jepsen: Cassandra 2.0.0; 2013-09-24](https://aphyr.com/posts/294-call-me-maybe-cassandra)
- [PODC 2021 Keynote by Kyle Kingsbury](https://youtu.be/EjNf_kbx36E)
  - ***26:39 Scylla 4.2-rc3***
- [Testing Apache Cassandra with Jepsen; 2016-01-21](https://www.datastax.com/blog/testing-apache-cassandra-jepsen)
  - [对应的测试集仓库](https://github.com/riptano/jepsen/tree/cassandra/cassandra)

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
- [PaxosRMW:arXiv2021](refs/arXiv2021-210314701ExtendingClassicPaxosforHighperformanceReadModifyWriteRegisters.pdf)
- [CAS:arXiv2013](refs/arXiv2013-13092772APracticalDistributedUniversalConstructionwithUnknownParticipants.pdf)
- [RAMP:SIGMOD2014](refs/SIGMOD2014-ScalableAtomicVisibilitywithRAMPTransactions.pdf)

Apache Cassandra is a free and open source NoSQL distributed database management system. It provides high availability, high scalability, and fault tolerance, even while running on commodity hardware. Cassandra has no single-point of failure, and is well-suited for clusters spanning multiple datacenter. Cassandra is decentralized and master-less. Therefore, data in a Cassandra cluster is…

## 基本信息

- **数据库类型**: 宽列
- **许可证**: Apache v2
- **首次发布**: 2008
- **国家/地区**: US

## 官网与文档

- [官网](https://cassandra.apache.org/_/index.html)
- [官方文档](https://cassandra.apache.org/doc/latest/)
- [GitHub](https://github.com/apache/cassandra)

## 数据源

- [Database of Databases](https://dbdb.io/db/cassandra)

## 收录资料

### 论文

| 文件 | 发表 | 标题 | 来源 |
| --- | --- | --- | --- |
| [SIGMOD2014-ScalableAtomicVisibilitywithRAMPTransactions.pdf](refs/SIGMOD2014-ScalableAtomicVisibilitywithRAMPTransactions.pdf) | — | ScalableAtomicVisibilitywithRAMPTransactions | [来源]() |
| [VLDB2015-UnderstandingtheCausesofConsistencyAnomaliesinApacheCassandra.pdf](papers/VLDB2015-UnderstandingtheCausesofConsistencyAnomaliesinApacheCassandra.pdf) | VLDB 2015 | Understanding the Causes of Consistency Anomalies in Apache Cassandra | [来源](https://vldb.org/pvldb/vol8/p810-fan.pdf) |
| [VLDB2022-TriememtablesinCassandra.pdf](papers/VLDB2022-TriememtablesinCassandra.pdf) | VLDB 2022 | Trie memtables in Cassandra | [来源](https://www.vldb.org/pvldb/vol15/p3359-lambov.pdf) |
| [arXiv2013-13092772APracticalDistributedUniversalConstructionwithUnknownParticipants.pdf](refs/arXiv2013-13092772APracticalDistributedUniversalConstructionwithUnknownParticipants.pdf) | — | 13092772APracticalDistributedUniversalConstructionwithUnknownParticipants | [来源]() |
| [arXiv2021-210314701ExtendingClassicPaxosforHighperformanceReadModifyWriteRegisters.pdf](refs/arXiv2021-210314701ExtendingClassicPaxosforHighperformanceReadModifyWriteRegisters.pdf) | — | 210314701ExtendingClassicPaxosforHighperformanceReadModifyWriteRegisters | [来源]() |

### 官方文档与白皮书

| 文件 | 标题 | 来源 |
| --- | --- | --- |
| [WelcometoApacheCassandrasdocumentationApacheCassandraDocumentation.md](docs/WelcometoApacheCassandrasdocumentationApacheCassandraDocumentation.md) | Welcome to Apache Cassandra’s documentation! \| Apache Cassandra Documentation | [来源](https://cassandra.apache.org/doc/latest/) |
