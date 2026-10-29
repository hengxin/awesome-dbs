# Database Index

由 [DB-Engines Ranking](https://db-engines.com/en/ranking) 与 [Database of Databases](https://dbdb.io/) 两个数据源整理生成。

- 数据库总数: **250**
- 数据来源: DB-Engines Ranking (2026-10) + Database of Databases (2026-10-28 快照, 1,228 个系统) + 项目内既有目录
- 标记说明: ⚠️链接失效 = 抓取时返回 404; ⚠️需登录 = 站点拒绝自动访问; ⚠️本次不可达 = 网络不可达

## 目录

## 类型分布

| 类型 | 数量 |
| --- | ---: |
| SQL | 108 |
| OLAP | 33 |
| 文档 | 62 |
| KV | 52 |
| 宽列 | 12 |
| 图 | 32 |
| 时序 | 31 |
| 向量 | 29 |
| 搜索 | 25 |
| 空间 | 40 |
| RDF | 1 |
| XML | 1 |
| 内容 | 1 |
| 多值 | 2 |
| 层次 | 1 |
| 嵌入式 | 6 |
| 流 | 3 |
| HTAP | 1 |
| 分布式 | 3 |
| 多模型 | 1 |

## 数据库总表

| # | 名称 | 目录 | 官方链接 | GitHub | 类型 | 所属机构 | 许可证 | 首次发布 | 数据源 |
| ---: | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | 4D | [4D](./4D/) | [官网](https://us.4d.com) | — | SQL | 4D, Inc | Proprietary | 1984 | [DB-Engines](https://db-engines.com/en/system/4D) [DBDB](https://dbdb.io/db/4d) |
| 2 | abhot | [abhot](./abhot/) | [官网](https://github.com/quqiangsheng/abhot) | [repo](https://github.com/quqiangsheng/abhot) | 时序 | — | Apache v2 | 2017 | [DBDB](https://dbdb.io/db/abhot) |
| 3 | Adabas | [Adabas](./Adabas/) | [官网](https://www.softwareag.com/en/adabas-natural)  ⚠️本次网络不可达 | — | 多值 | Software AG | Proprietary | — | [DB-Engines](https://db-engines.com/en/system/Adabas) [DBDB](https://dbdb.io/db/adabas) |
| 4 | Aerospike | [Aerospike](./Aerospike/) | [官网](https://aerospike.com) | [repo](https://github.com/aerospike/aerospike-server) | 文档、KV、图、空间 | Aerospike | AGPL v3 | 2012 | [DB-Engines](https://db-engines.com/en/system/Aerospike) [DBDB](https://dbdb.io/db/aerospike) |
| 5 | AgateDB | [AgateDB](./AgateDB/) | [官网](https://github.com/tikv/agatedb) | [repo](https://github.com/tikv/agatedb) | KV | PingCAP | Apache v2 | 2019 | [DBDB](https://dbdb.io/db/agatedb) |
| 6 | Algolia | [Algolia](./Algolia/) | [官网](https://www.algolia.com/) | — | 搜索 | — | 商业或开源（DB-Engines 未给出具体许可证） | 2012 | [DB-Engines](https://db-engines.com/en/system/Algolia) |
| 7 | Alibaba Cloud PolarDB | [PolarDB](./PolarDB/) | [官网](https://www.alibabacloud.com/en/product/polardb?_p_lc=1) | [repo](https://github.com/alibaba/polardb) | SQL | Alibaba | 商业或开源（DB-Engines 未给出具体许可证） | 2017 | [DB-Engines](https://db-engines.com/en/system/Alibaba+Cloud+PolarDB) [DBDB](https://dbdb.io/db/polardb) |
| 8 | Amazon Aurora | [Amazon Aurora](./Amazon Aurora/) | [官网](https://aws.amazon.com/rds/aurora) | — | SQL、文档、向量、空间 | Amazon | 商业或开源（DB-Engines 未给出具体许可证） | 2015 | [DB-Engines](https://db-engines.com/en/system/Amazon+Aurora) [DBDB](https://dbdb.io/db/aurora) |
| 9 | Amazon CloudSearch | [Amazon CloudSearch](./Amazon CloudSearch/) | [官网](https://aws.amazon.com/cloudsearch/) | — | 搜索 | Amazon | 商业或开源（DB-Engines 未给出具体许可证） | 2012 | [DB-Engines](https://db-engines.com/en/system/Amazon+CloudSearch) |
| 10 | Amazon DocumentDB | [Amazon DocumentDB](./Amazon DocumentDB/) | [官网](https://aws.amazon.com/documentdb/) | — | 文档 | — | 商业或开源（DB-Engines 未给出具体许可证） | 2019 | [DB-Engines](https://db-engines.com/en/system/Amazon+DocumentDB) |
| 11 | Amazon DynamoDB | [Amazon DynamoDB](./Amazon DynamoDB/) | [官网](https://aws.amazon.com/dynamodb) | [repo](https://github.com/awslabs/dynamodb-transactions) | 文档、KV | Amazon | Proprietary | 2012 | [DB-Engines](https://db-engines.com/en/system/Amazon+DynamoDB) [DBDB](https://dbdb.io/db/dynamodb) |
| 12 | Amazon Neptune | [Amazon Neptune](./Amazon Neptune/) | [官网](https://aws.amazon.com/neptune/) | — | 图 | Amazon | 商业或开源（DB-Engines 未给出具体许可证） | 2017 | [DB-Engines](https://db-engines.com/en/system/Amazon+Neptune) |
| 13 | Amazon Redshift | [Amazon Redshift](./Amazon Redshift/) | [官网](https://aws.amazon.com/redshift/) | — | SQL | Amazon (based on PostgreSQL ) | 商业或开源（DB-Engines 未给出具体许可证） | 2012 | [DB-Engines](https://db-engines.com/en/system/Amazon+Redshift) |
| 14 | Amazon SimpleDB | [Amazon SimpleDB](./Amazon SimpleDB/) | [官网](https://aws.amazon.com/simpledb/) | — | KV | Amazon | 商业或开源（DB-Engines 未给出具体许可证） | 2007 | [DB-Engines](https://db-engines.com/en/system/Amazon+SimpleDB) |
| 15 | AntDB | [AntDB](./AntDB/) | [官网](https://www.asiainfo.com/en_us/product_aisware_antDB.html) | [repo](https://github.com/ADBSQL/AntDB) | SQL | AsiaInfo Technologies Limited | Apache v2 | — | [DB-Engines](https://db-engines.com/en/system/AntDB) [DBDB](https://dbdb.io/db/antdb) |
| 16 | Apache Accumulo | [Apache Accumulo](./Apache Accumulo/) | [官网](https://accumulo.apache.org/) | [repo](https://github.com/apache/accumulo) | 宽列 | — | 商业或开源（DB-Engines 未给出具体许可证） | 2008 | [DB-Engines](https://db-engines.com/en/system/Apache+Accumulo) |
| 17 | Apache Cassandra | [Cassandra](./Cassandra/) | [官网](https://cassandra.apache.org/_/index.html) | [repo](https://github.com/apache/cassandra) | 宽列 | — | Apache v2 | 2008 | [DBDB](https://dbdb.io/db/cassandra) |
| 18 | Apache CouchDB | [CouchDB](./CouchDB/) | [官网](https://couchdb.apache.org) | [repo](https://github.com/apache/couchdb) | 文档、空间 | Apache Software Foundation Apache top-level project, originally developed by Damien Katz, a former Lotus Notes developer | Apache v2 | 2005 | [DB-Engines](https://db-engines.com/en/system/CouchDB) [DBDB](https://dbdb.io/db/couchdb) |
| 19 | Apache Derby | [Apache Derby](./Apache Derby/) | [官网](https://db.apache.org/derby/) | — | SQL | Apache Software Foundation | 商业或开源（DB-Engines 未给出具体许可证） | 1997 | [DB-Engines](https://db-engines.com/en/system/Apache+Derby) |
| 20 | Apache Drill | [Apache Drill](./Apache Drill/) | [官网](https://drill.apache.org/) | — | SQL、文档 | Apache Software Foundation | 商业或开源（DB-Engines 未给出具体许可证） | 2012 | [DB-Engines](https://db-engines.com/en/system/Apache+Drill) |
| 21 | Apache Druid | [Apache Druid](./Apache Druid/) | [官网](https://druid.apache.org/) | [repo](https://github.com/apache/druid) | SQL、时序 | Apache Software Foundation and contributors | 商业或开源（DB-Engines 未给出具体许可证） | 2012 | [DB-Engines](https://db-engines.com/en/system/Apache+Druid) |
| 22 | Apache Flink | [Apache Flink](./Apache Flink/) | [官网](https://flink.apache.org/) | [repo](https://github.com/apache/flink) | SQL | Apache Software Foundation and contributors | 商业或开源（DB-Engines 未给出具体许可证） | — | [DB-Engines](https://db-engines.com/en/system/Apache+Flink) |
| 23 | Apache HBase | [Apache HBase](./Apache HBase/) | [官网](https://hbase.apache.org/) | [repo](https://github.com/apache/hbase) | 宽列 | Apache Software Foundation Apache top-level project, originally developed by Powerset | 商业或开源（DB-Engines 未给出具体许可证） | 2008 | [DB-Engines](https://db-engines.com/en/system/Apache+HBase) |
| 24 | Apache Hive | [Apache Hive](./Apache Hive/) | [官网](https://hive.apache.org/) | [repo](https://github.com/apache/hive) | SQL | Apache Software Foundation initially developed by Facebook | 商业或开源（DB-Engines 未给出具体许可证） | 2012 | [DB-Engines](https://db-engines.com/en/system/Apache+Hive) |
| 25 | Apache Ignite | [Apache Ignite](./Apache Ignite/) | [官网](https://ignite.apache.org/) | [repo](https://github.com/apache/ignite) | SQL、KV | Apache Software Foundation | 商业或开源（DB-Engines 未给出具体许可证） | 2015 | [DB-Engines](https://db-engines.com/en/system/Apache+Ignite) |
| 26 | Apache Impala | [Apache Impala](./Apache Impala/) | [官网](https://impala.apache.org/) | — | SQL、文档 | Apache Software Foundation Apache top-level project, originally developed by Cloudera | 商业或开源（DB-Engines 未给出具体许可证） | 2013 | [DB-Engines](https://db-engines.com/en/system/Apache+Impala) |
| 27 | Apache IoTDB | [Apache IoTDB](./Apache IoTDB/) | [官网](https://iotdb.apache.org/) | [repo](https://github.com/apache/iotdb) | 时序 | Apache Software Foundation | 商业或开源（DB-Engines 未给出具体许可证） | 2018 | [DB-Engines](https://db-engines.com/en/system/Apache+IoTDB) |
| 28 | Apache Jackrabbit | [Apache Jackrabbit](./Apache Jackrabbit/) | [官网](https://jackrabbit.apache.org/) | [repo](https://github.com/apache/jackrabbit) | 内容 | Apache Software Foundation | 商业或开源（DB-Engines 未给出具体许可证） | 2006 | [DB-Engines](https://db-engines.com/en/system/Apache+Jackrabbit) |
| 29 | Apache Jena TDB | [Apache Jena TDB](./Apache Jena TDB/) | [官网](https://jena.apache.org/documentation/tdb/index.html) | [repo](https://github.com/apache/jena) | RDF | Apache Software Foundation originally developed by HP Labs | 商业或开源（DB-Engines 未给出具体许可证） | 2000 | [DB-Engines](https://db-engines.com/en/system/Apache+Jena+-+TDB) |
| 30 | Apache Phoenix | [Apache Phoenix](./Apache Phoenix/) | [官网](https://phoenix.apache.org/) | — | SQL | Apache Software Foundation | 商业或开源（DB-Engines 未给出具体许可证） | 2014 | [DB-Engines](https://db-engines.com/en/system/Apache+Phoenix) |
| 31 | Apache Solr | [Apache Solr](./Apache Solr/) | [官网](https://solr.apache.org/) | [repo](https://github.com/apache/solr) | 搜索、空间 | Apache Software Foundation | 商业或开源（DB-Engines 未给出具体许可证） | 2006 | [DB-Engines](https://db-engines.com/en/system/Apache+Solr) |
| 32 | Apache Spark | [Apache Spark](./Apache Spark/) | — | [repo](https://github.com/apache/spark) | SQL、OLAP、流 | — | — | — | — |
| 33 | Apache ZooKeeper | [ZooKeeper](./ZooKeeper/) | [官网](https://zookeeper.apache.org) | [repo](https://github.com/apache/zookeeper) | KV | Apache Software Foundation | Apache v2 | 2008 | [DBDB](https://dbdb.io/db/zookeeper) |
| 34 | Ardb | [Ardb](./Ardb/) | [官网](https://github.com/yinqiwen/ardb) | [repo](https://github.com/yinqiwen/ardb) | KV | Yinqi Wen | BSD License | 2013 | [DBDB](https://dbdb.io/db/ardb) |
| 35 | AwaDB | [AwaDB](./AwaDB/) | [官网](https://github.com/awa-ai/awadb) | [repo](https://github.com/awa-ai/awadb) | 向量 | — | Apache v2 | 2023 | [DBDB](https://dbdb.io/db/awadb) |
| 36 | BaikalDB | [BaikalDB](./BaikalDB/) | [官网](https://baikaldb.com) | [repo](https://github.com/baidu/BaikalDB) | SQL | Baidu, Inc. | Apache v2 | 2018 | [DBDB](https://dbdb.io/db/baikaldb) |
| 37 | BaseX | [BaseX](./BaseX/) | [官网](https://basex.org) | [repo](https://github.com/BaseXdb/basex) | XML | BaseX GmbH | BSD License | 2007 | [DB-Engines](https://db-engines.com/en/system/BaseX) [DBDB](https://dbdb.io/db/basex) |
| 38 | Berkeley DB | [Berkeley DB](./Berkeley DB/) | [官网](https://www.oracle.com/database/technologies/related/berkeleydb.html) | [repo](https://github.com/berkeleydb/libdb) | SQL | — | — | 1994 | [DBDB](https://dbdb.io/db/berkeley-db) |
| 39 | ByConity | [ByConity](./ByConity/) | [官网](https://byconity.github.io) | [repo](https://github.com/ByConity/ByConity) | OLAP | ByteDance Ltd. | Apache v2 | 2020 | [DBDB](https://dbdb.io/db/byconity) |
| 40 | Calvin | [Calvin](./Calvin/) | [官网](http://dslam.cs.umd.edu/calvin) | [repo](https://github.com/cmu-db/calvin) | SQL | Yale University | — | 2012 | [DBDB](https://dbdb.io/db/calvin) |
| 41 | Chroma | [Chroma](./Chroma/) | [官网](https://www.trychroma.com) | [repo](https://github.com/chroma-core/chroma) | 向量 | Chroma | Apache v2 | 2022 | [DB-Engines](https://db-engines.com/en/system/Chroma) [DBDB](https://dbdb.io/db/chroma) |
| 42 | Citus | [Citus](./Citus/) | [官网](https://www.citusdata.com) | [repo](https://github.com/citusdata/citus) | SQL、OLAP、文档 | Citus Data, Inc. | AGPL v3 | 2010 | [DB-Engines](https://db-engines.com/en/system/Citus) [DBDB](https://dbdb.io/db/citus) |
| 43 | ClickHouse | [ClickHouse](./ClickHouse/) | [官网](https://clickhouse.com) | [repo](https://github.com/ClickHouse/ClickHouse) | OLAP、文档、时序、向量、空间 | Clickhouse Inc. | Apache v2 | 2016 | [DB-Engines](https://db-engines.com/en/system/ClickHouse) [DBDB](https://dbdb.io/db/clickhouse) |
| 44 | CloseVector | [CloseVector](./CloseVector/) | [官网](https://closevector-docs.getmegaportal.com) | — | 向量 | MegaPortal | Apache v2 | 2023 | [DBDB](https://dbdb.io/db/closevector) |
| 45 | Cloudberry | [Cloudberry](./Cloudberry/) | [官网](https://cloudberry.apache.org) | [repo](https://github.com/apache/cloudberry) | OLAP | HashData Technology Limited | Apache v2 | 2023 | [DBDB](https://dbdb.io/db/cloudberry) |
| 46 | CloudKit | [CloudKit](./CloudKit/) | [官网](http://getcloudkit.com) | [repo](https://github.com/jcrosby/cloudkit) | 文档 | — | MIT License | 2016 | [DB-Engines](https://db-engines.com/en/system/CloudKit) [DBDB](https://dbdb.io/db/cloudkit) |
| 47 | CnosDB | [CnosDB](./CnosDB/) | [官网](https://github.com/cnosdb/cnosdb) | [repo](https://github.com/cnosdb/cnosdb) | 时序 | CnosDB | AGPL v3 | 2022 | [DB-Engines](https://db-engines.com/en/system/CnosDB) [DBDB](https://dbdb.io/db/cnosdb) |
| 48 | CockroachDB | [CockroachDB](./CockroachDB/) | [官网](https://www.cockroachlabs.com) | [repo](https://github.com/cockroachdb/cockroach) | SQL | Cockroach Labs | Business Source License | 2014 | [DBDB](https://dbdb.io/db/cockroachdb) |
| 49 | Coherence | [Coherence](./Coherence/) | [官网](https://www.oracle.com/java/coherence) | [repo](https://github.com/oracle/coherence) | KV | — | Universal Permissive License | 2000 | [DBDB](https://dbdb.io/db/coherence) |
| 50 | Couchbase | [Couchbase](./Couchbase/) | [官网](https://www.couchbase.com) | [repo](https://github.com/apache/hbase) | 文档、KV、宽列、时序、向量、搜索、空间 | Couchbase, Inc. | Apache v2 | 2011 | [DB-Engines](https://db-engines.com/en/system/Couchbase) [DBDB](https://dbdb.io/db/couchbase) |
| 51 | CovenantSQL | [CovenantSQL](./CovenantSQL/) | [官网](https://covenantsql.io) | [repo](https://github.com/CovenantSQL/CovenantSQL) | SQL | Covenant Labs | Apache v2 | 2018 | [DB-Engines](https://db-engines.com/en/system/CovenantSQL) [DBDB](https://dbdb.io/db/covenantsql) |
| 52 | Coveo | [Coveo](./Coveo/) | [官网](https://www.coveo.com) | — | 搜索 | Coveo | 商业或开源（DB-Engines 未给出具体许可证） | 2012 | [DB-Engines](https://db-engines.com/en/system/Coveo) |
| 53 | CrossDB | [CrossDB](./CrossDB/) | [官网](https://crossdb.org) | [repo](https://github.com/crossdb-org/CrossDB) | 嵌入式 | JC Wang | Proprietary | 2019 | [DBDB](https://dbdb.io/db/crossdb) |
| 54 | Databend | [Databend](./Databend/) | [官网](http://github.com/databendlabs/databend) | [repo](https://github.com/databendlabs/databend) | SQL、OLAP | Databend Labs | Apache v2 | 2021 | [DB-Engines](https://db-engines.com/en/system/Databend) [DBDB](https://dbdb.io/db/databend) |
| 55 | Databricks | [Databricks](./Databricks/) | [官网](https://www.databricks.com) | — | SQL、OLAP、文档 | Databricks | Proprietary | 2013 | [DB-Engines](https://db-engines.com/en/system/Databricks) [DBDB](https://dbdb.io/db/databricks) |
| 56 | Datastax Enterprise | [Datastax Enterprise](./Datastax Enterprise/) | [官网](https://www.datastax.com/products/datastax-enterprise) | — | 文档、宽列、图、向量、搜索、空间 | DataStax | 商业或开源（DB-Engines 未给出具体许可证） | 2011 | [DB-Engines](https://db-engines.com/en/system/Datastax+Enterprise) |
| 57 | Datomic | [Datomic](./Datomic/) | [官网](https://www.datomic.com) | — | SQL | Cognitect | Proprietary | 2012 | [DB-Engines](https://db-engines.com/en/system/Datomic) [DBDB](https://dbdb.io/db/datomic) |
| 58 | dBASE | [dBASE](./dBASE/) | [官网](http://www.dbase.com/)  ⚠️HTTP 500 | — | SQL | Asthon Tate | Proprietary | — | [DB-Engines](https://db-engines.com/en/system/dBASE) [DBDB](https://dbdb.io/db/dbase) |
| 59 | Dgraph | [Dgraph](./Dgraph/) | [官网](https://dgraph.io/) | [repo](https://github.com/dgraph-io/dgraph) | 图 | Dgraph Labs, Inc. | Apache v2 | 2016 | [DB-Engines](https://db-engines.com/en/system/Dgraph) [DBDB](https://dbdb.io/db/dgraph) |
| 60 | DolphinDB | [DolphinDB](./DolphinDB/) | [官网](https://dolphindb.com) | [repo](https://github.com/dolphindb/DolphinDB) | SQL、OLAP、时序、向量 | DolphinDB, Inc | Proprietary | 2018 | [DB-Engines](https://db-engines.com/en/system/DolphinDB) [DBDB](https://dbdb.io/db/dolphindb) |
| 61 | Doris | [Doris](./Doris/) | [官网](https://doris.apache.org) | [repo](https://github.com/apache/doris) | OLAP | Baidu, Inc. | Apache v2 | 2017 | [DBDB](https://dbdb.io/db/doris) |
| 62 | DuckDB | [DuckDB](./DuckDB/) | [官网](https://duckdb.org/) | [repo](https://github.com/duckdb/duckdb) | SQL、OLAP | — | MIT License | 2018 | [DB-Engines](https://db-engines.com/en/system/DuckDB) [DBDB](https://dbdb.io/db/duckdb) |
| 63 | EDB Postgres | [EDB Postgres](./EDB Postgres/) | [官网](https://www.enterprisedb.com/) | — | SQL、文档、空间 | EnterpriseDB | 商业或开源（DB-Engines 未给出具体许可证） | 2005 | [DB-Engines](https://db-engines.com/en/system/EDB+Postgres) |
| 64 | Ehcache | [Ehcache](./Ehcache/) | [官网](https://www.ehcache.org) | [repo](https://github.com/ehcache/ehcache3) | KV | Terracotta Inc, owned by Software AG | Apache v2 | 2009 | [DB-Engines](https://db-engines.com/en/system/Ehcache) [DBDB](https://dbdb.io/db/ehcache) |
| 65 | Elasticsearch | [Elasticsearch](./Elasticsearch/) | [官网](https://www.elastic.co) | [repo](https://github.com/elastic/elasticsearch) | 文档、向量、搜索、空间 | Elastic | Apache v2 | 2010 | [DB-Engines](https://db-engines.com/en/system/Elasticsearch) [DBDB](https://dbdb.io/db/elasticsearch) |
| 66 | Engula | [Engula](./Engula/) | [官网](https://www.engula.io) | [repo](https://github.com/engula/engula) | KV | Huachao Huang | Apache v2 | 2022 | [DBDB](https://dbdb.io/db/engula) |
| 67 | Essbase | [Essbase](./Essbase/) | [官网](https://www.oracle.com/business-analytics/essbase.html) | — | OLAP | — | Proprietary | 1992 | [DBDB](https://dbdb.io/db/essbase) |
| 68 | etcd | [etcd](./etcd/) | [官网](https://etcd.io) | [repo](https://github.com/etcd-io/etcd) | KV | — | Apache v2 | 2013 | [DB-Engines](https://db-engines.com/en/system/etcd) [DBDB](https://dbdb.io/db/etcd) |
| 69 | EuclidOLAP | [EuclidOLAP](./EuclidOLAP/) | [官网](http://www.euclidolap.com) | [repo](https://github.com/EuclidOLAP/EuclidOLAP) | OLAP | Chen Zhigang | Apache v2 | 2022 | [DBDB](https://dbdb.io/db/euclidolap) |
| 70 | EXASOL | [EXASOL](./EXASOL/) | [官网](https://www.exasol.com) | — | SQL、OLAP | Exasol | Proprietary | 2000 | [DB-Engines](https://db-engines.com/en/system/EXASOL) [DBDB](https://dbdb.io/db/exasol) |
| 71 | Fauna | [Fauna](./Fauna/) | [官网](https://fauna.com)  ⚠️本次网络不可达 | [repo](https://github.com/fauna/fauna) | SQL、文档、图、时序 | Fauna, Inc. | Proprietary | 2014 | [DB-Engines](https://db-engines.com/en/system/Fauna) [DBDB](https://dbdb.io/db/faunadb) |
| 72 | FileMaker | [FileMaker](./FileMaker/) | [官网](https://www.claris.com/filemaker/) | — | SQL | Claris a subsidiary of Apple | Proprietary | 1983 | [DB-Engines](https://db-engines.com/en/system/FileMaker) [DBDB](https://dbdb.io/db/filemaker) |
| 73 | Firebase Realtime Database | [Firebase Realtime Database](./Firebase Realtime Database/) | [官网](https://firebase.google.com/products/realtime-database/)  ⚠️本次网络不可达 | — | 文档 | Google acquired by Google 2014 | 商业或开源（DB-Engines 未给出具体许可证） | 2012 | [DB-Engines](https://db-engines.com/en/system/Firebase+Realtime+Database) |
| 74 | Firebird | [Firebird](./Firebird/) | [官网](http://www.firebirdsql.org/) | [repo](https://github.com/firebird-sql/firebird) | SQL | Firebird Foundation | Mozilla Public License | 2000 | [DB-Engines](https://db-engines.com/en/system/Firebird) [DBDB](https://dbdb.io/db/firebird) |
| 75 | FlashDB | [FlashDB](./FlashDB/) | [官网](https://armink.github.io/FlashDB) | [repo](https://github.com/armink/FlashDB) | KV、嵌入式 | Armink | Apache v2 | 2020 | [DBDB](https://dbdb.io/db/flashdb) |
| 76 | FoundationDB | [FoundationDB](./FoundationDB/) | [官网](https://github.com/apple/foundationdb) | [repo](https://github.com/apple/foundationdb) | SQL、文档、KV | FoundationDB | Apache v2 | 2013 | [DB-Engines](https://db-engines.com/en/system/FoundationDB) [DBDB](https://dbdb.io/db/foundationdb) |
| 77 | Galaxybase | [Galaxybase](./Galaxybase/) | [官网](https://galaxybase.com/) | — | 图 | Chuanglin(Createlink) Technology Co., Ltd 浙江创邻科技有限公司 | Proprietary | 2017 | [DB-Engines](https://db-engines.com/en/system/Galaxybase) [DBDB](https://dbdb.io/db/galaxybase) |
| 78 | GBase | [GBase](./GBase/) | [官网](http://www.gbase.cn) | — | SQL | General Data Technology Co., Ltd. | Proprietary | 2004 | [DB-Engines](https://db-engines.com/en/system/GBase) [DBDB](https://dbdb.io/db/gbase) |
| 79 | GemFire | [GemFire](./GemFire/) | [官网](https://network.tanzu.vmware.com/products/pivotal-gemfire/) | — | 文档、KV | VMware | 商业或开源（DB-Engines 未给出具体许可证） | 2004 | [DB-Engines](https://db-engines.com/en/system/GemFire) |
| 80 | GoldenDB | [GoldenDB](./GoldenDB/) | [官网](https://www.zte.com.cn/china/solutions_latest/goldendb.html) | — | SQL、分布式 | — | — | — | [DBDB](https://dbdb.io/db/goldendb) |
| 81 | Google BigQuery | [Google BigQuery](./Google BigQuery/) | [官网](https://cloud.google.com/bigquery/)  ⚠️本次网络不可达 | — | SQL | Google | 商业或开源（DB-Engines 未给出具体许可证） | 2010 | [DB-Engines](https://db-engines.com/en/system/Google+BigQuery) |
| 82 | Google Bigtable | [Google Bigtable](./Google Bigtable/) | — | — | 宽列 | — | — | — | — |
| 83 | Google Cloud Datastore | [Google Cloud Datastore](./Google Cloud Datastore/) | [官网](https://cloud.google.com/datastore/)  ⚠️本次网络不可达 | — | 文档 | Google | 商业或开源（DB-Engines 未给出具体许可证） | 2008 | [DB-Engines](https://db-engines.com/en/system/Google+Cloud+Datastore) |
| 84 | Google Cloud Firestore | [Google Cloud Firestore](./Google Cloud Firestore/) | [官网](https://firebase.google.com/products/firestore/)  ⚠️本次网络不可达 | — | 文档 | Google | 商业或开源（DB-Engines 未给出具体许可证） | 2017 | [DB-Engines](https://db-engines.com/en/system/Google+Cloud+Firestore) |
| 85 | Google F1 | [Google F1](./Google F1/) | [官网](https://ai.google/research/pubs/pub41344)  ⚠️本次网络不可达 | — | SQL | Google LLC | — | 2013 | [DBDB](https://dbdb.io/db/google-f1) |
| 86 | Google Megastore | [Google Megastore](./Google Megastore/) | — | — | KV | — | — | — | — |
| 87 | Google Percolator | [Google Percolator](./Google Percolator/) | — | — | KV | — | — | — | — |
| 88 | Google Spanner | [Google Spanner](./Google Spanner/) | [官网](https://cloud.google.com/spanner)  ⚠️本次网络不可达 | — | SQL | Google LLC | Proprietary | 2007 | [DBDB](https://dbdb.io/db/cloud-spanner) |
| 89 | GraphDB | [GraphDB](./GraphDB/) | [官网](https://graphdb.ontotext.com) | [repo](https://github.com/google/snappy) | 图 | Ontotext, trading as Graphwise | Proprietary | 2000 | [DB-Engines](https://db-engines.com/en/system/GraphDB) [DBDB](https://dbdb.io/db/graphdb) |
| 90 | Graphite | [Graphite](./Graphite/) | [官网](https://github.com/graphite-project/graphite-web) | [repo](https://github.com/graphite-project/graphite-web) | 时序 | Chris Davis | 商业或开源（DB-Engines 未给出具体许可证） | 2006 | [DB-Engines](https://db-engines.com/en/system/Graphite) |
| 91 | GreatSQL | [GreatSQL](./GreatSQL/) | [官网](https://greatsql.cn) | [repo](https://github.com/GreatSQL/greatsql) | SQL | Beijing Wanli Open Source Software Co. | GPL v2 | 2020 | [DBDB](https://dbdb.io/db/greatsql) |
| 92 | Greenplum | [Greenplum](./Greenplum/) | [官网](https://greenplum.org)  ⚠️本次网络不可达 | [repo](https://github.com/greenplum-db/gpdb) | SQL、OLAP、文档、空间 | Pivotal Software Inc. | 商业或开源（DB-Engines 未给出具体许可证） | 2005 | [DB-Engines](https://db-engines.com/en/system/Greenplum) [DBDB](https://dbdb.io/db/greenplum) |
| 93 | GreptimeDB | [GreptimeDB](./GreptimeDB/) | [官网](https://greptime.com) | [repo](https://github.com/GreptimeTeam/greptimedb) | 时序 | Greptime Inc. | Apache v2 | 2022 | [DB-Engines](https://db-engines.com/en/system/GreptimeDB) [DBDB](https://dbdb.io/db/greptimedb) |
| 94 | H2 | [H2](./H2/) | [官网](http://www.h2database.com) | [repo](https://github.com/h2database/h2database) | SQL、空间 | Thomas Mueller | 商业或开源（DB-Engines 未给出具体许可证） | 2005 | [DB-Engines](https://db-engines.com/en/system/H2) [DBDB](https://dbdb.io/db/h2) |
| 95 | Haixun | [Haixun](./Haixun/) | [官网](https://www.amazon.com/real-time-database-management-application-development/dp/7512360703) | — | SQL、分布式 | — | — | — | [DBDB](https://dbdb.io/db/haixun) |
| 96 | Hazelcast | [Hazelcast](./Hazelcast/) | [官网](https://hazelcast.com) | [repo](https://github.com/hazelcast/hazelcast) | 文档、KV | Hazelcast | Apache v2 | 2008 | [DB-Engines](https://db-engines.com/en/system/Hazelcast) [DBDB](https://dbdb.io/db/hazelcast) |
| 97 | HexaDB | [HexaDB](./HexaDB/) | [官网](https://dataeasy.cn) | — | SQL、HTAP | Shuyi Technology (Beijing) Co. | Proprietary | 2023 | [DBDB](https://dbdb.io/db/hexadb) |
| 98 | HoraeDB | [HoraeDB](./HoraeDB/) | [官网](https://incubator.apache.org/projects/horaedb.html) | [repo](https://github.com/apache/horaedb) | 时序 | Ant Group | Apache v2 | 2021 | [DBDB](https://dbdb.io/db/horaedb) |
| 99 | HStreamDB | [HStreamDB](./HStreamDB/) | [官网](https://hstream.io) | [repo](https://github.com/hstreamdb/hstream) | 流 | EMQ Technologies Co. | BSD License | 2020 | [DBDB](https://dbdb.io/db/hstreamdb) |
| 100 | HugeGraph | [HugeGraph](./HugeGraph/) | [官网](https://hugegraph.apache.org) | [repo](https://github.com/apache/incubator-hugegraph) | 图 | Baidu, Inc. | Apache v2 | 2017 | [DBDB](https://dbdb.io/db/hugegraph) |
| 101 | HyperSQL | [HyperSQL](./HyperSQL/) | [官网](http://hsqldb.org)  ⚠️HTTP 502 | — | SQL | HSQLDB Development Group | BSD License | 2001 | [DB-Engines](https://db-engines.com/en/system/HyperSQL) [DBDB](https://dbdb.io/db/hypersql) |
| 102 | IBM Cloudant | [IBM Cloudant](./IBM Cloudant/) | [官网](https://www.ibm.com/products/cloudant) | — | 文档 | IBM, Apache Software Foundation IBM acquired Cloudant in February 2014 | 商业或开源（DB-Engines 未给出具体许可证） | 2010 | [DB-Engines](https://db-engines.com/en/system/IBM+Cloudant) |
| 103 | IBM Db2 | [IBM-Db2-pureScale](./IBM-Db2-pureScale/) | [官网](https://www.ibm.com/products/db2) | — | SQL、文档、空间 | IBM | Proprietary | 1983 | [DB-Engines](https://db-engines.com/en/system/IBM+Db2) [DBDB](https://dbdb.io/db/db2) |
| 104 | iBoxDB | [iBoxDB](./iBoxDB/) | [官网](https://www.iboxdb.com) | — | 文档 | iBoxDB | Proprietary | 2013 | [DB-Engines](https://db-engines.com/en/system/iBoxDB) [DBDB](https://dbdb.io/db/iboxdb) |
| 105 | IceFireDB | [IceFireDB](./IceFireDB/) | [官网](https://www.icefiredb.xyz) | [repo](https://github.com/IceFireDB/IceFireDB) | KV | Li Biao | Apache v2 | 2021 | [DBDB](https://dbdb.io/db/icefiredb) |
| 106 | IMS | [IMS](./IMS/) | [官网](https://www.ibm.com/products/ims) | — | 层次 | IBM | Proprietary | — | [DB-Engines](https://db-engines.com/en/system/IMS) [DBDB](https://dbdb.io/db/ims) |
| 107 | Infinispan | [Infinispan](./Infinispan/) | [官网](https://infinispan.org) | [repo](https://github.com/infinispan/infinispan) | KV | Red Hat, Inc. | Apache v2 | 2009 | [DB-Engines](https://db-engines.com/en/system/Infinispan) [DBDB](https://dbdb.io/db/infinispan) |
| 108 | Infinity | [Infinity](./Infinity/) | [官网](https://github.com/infiniflow/infinity) | [repo](https://github.com/infiniflow/infinity) | 向量 | InfiniFlow | Apache v2 | 2022 | [DBDB](https://dbdb.io/db/infinity) |
| 109 | InfluxDB | [InfluxDB](./InfluxDB/) | [官网](https://www.influxdata.com) | [repo](https://github.com/influxdata/influxdb) | 时序、空间 | InfluxData | MIT License | 2013 | [DB-Engines](https://db-engines.com/en/system/InfluxDB) [DBDB](https://dbdb.io/db/influxdb) |
| 110 | Informix | [Informix](./Informix/) | [官网](https://www.ibm.com/products/informix) | — | SQL、文档、时序、空间 | IBM, HCL Technologies Effective May 1st, 2017, HCL took on development, technical support, and product management teams, and works jointly with IBM on product strategy, marketing, and sales. | Proprietary | 1984 | [DB-Engines](https://db-engines.com/en/system/Informix) [DBDB](https://dbdb.io/db/informix) |
| 111 | Ingres | [Ingres](./Ingres/) | [官网](https://www.actian.com/databases/ingres) | — | SQL | Actian Corporation | Proprietary | — | [DB-Engines](https://db-engines.com/en/system/Ingres) [DBDB](https://dbdb.io/db/ingres) |
| 112 | Interbase | [Interbase](./Interbase/) | [官网](http://www.embarcadero.com/products/interbase) | — | SQL | Embarcadero | Proprietary | 1984 | [DB-Engines](https://db-engines.com/en/system/Interbase) [DBDB](https://dbdb.io/db/interbase) |
| 113 | InterSystems IRIS | [InterSystems IRIS](./InterSystems IRIS/) | [官网](https://www.intersystems.com/products/intersystems-iris/) | — | SQL、文档、KV | InterSystems | 商业或开源（DB-Engines 未给出具体许可证） | 2018 | [DB-Engines](https://db-engines.com/en/system/InterSystems+IRIS) |
| 114 | IoTDB | [IoTDB](./IoTDB/) | [官网](https://iotdb.apache.org) | [repo](https://github.com/apache/iotdb) | 时序 | Tsinghua University | Apache v2 | 2017 | [DBDB](https://dbdb.io/db/iotdb) |
| 115 | JanusGraph | [JanusGraph](./JanusGraph/) | [官网](https://janusgraph.org) | [repo](https://github.com/janusgraph/janusgraph) | 图 | Linux Foundation; originally developed as Titan by Aurelius | Apache v2 | 2017 | [DB-Engines](https://db-engines.com/en/system/JanusGraph) [DBDB](https://dbdb.io/db/janusgraph) |
| 116 | JoinBase | [JoinBase](./JoinBase/) | [官网](https://aimen.io) | [repo](https://github.com/open-joinbase/joinbase) | 时序 | — | Proprietary | — | [DBDB](https://dbdb.io/db/joinbase) |
| 117 | Kdb | [Kdb](./Kdb/) | [官网](https://kx.com) | — | SQL | Inspur Group | Proprietary | 1998 | [DB-Engines](https://db-engines.com/en/system/K-DB) [DBDB](https://dbdb.io/db/kdb) |
| 118 | KingbaseES | [KingbaseES](./KingbaseES/) | [官网](https://www.kingbase.com.cn) | — | SQL | Jincang Information Technology | Proprietary | 1999 | [DBDB](https://dbdb.io/db/kingbase) |
| 119 | Kunlun | [Kunlun](./Kunlun/) | [官网](http://kunlunbase.com) | [repo](https://github.com/zettadb/kunlun) | SQL | Zetuo Technology Co., Ltd. | Commons Clause License | 2019 | [DBDB](https://dbdb.io/db/kunlun) |
| 120 | KVDB | [KVDB](./KVDB/) | [官网](https://kvdb.io) | — | KV | Pilvy, Inc. | Proprietary | 2018 | [DBDB](https://dbdb.io/db/kvdb) |
| 121 | Kvrocks | [Kvrocks](./Kvrocks/) | [官网](https://kvrocks.apache.org) | [repo](https://github.com/apache/kvrocks) | KV | Meitu | Apache v2 | 2019 | [DBDB](https://dbdb.io/db/kvrocks) |
| 122 | Kylin | [Kylin](./Kylin/) | [官网](http://www.kylin.io) | [repo](https://github.com/apache/kylin) | OLAP | eBay Inc. | Apache v2 | 2013 | [DBDB](https://dbdb.io/db/kylin) |
| 123 | Kyuubi | [Kyuubi](./Kyuubi/) | [官网](https://kyuubi.apache.org) | [repo](https://github.com/apache/kyuubi) | SQL | — | Apache v2 | 2017 | [DBDB](https://dbdb.io/db/kyuubi) |
| 124 | Lealone | [Lealone](./Lealone/) | [官网](http://lealone.org) | [repo](https://github.com/lealone/Lealone) | SQL、嵌入式 | — | — | 2012 | [DBDB](https://dbdb.io/db/lealone) |
| 125 | LedisDB | [LedisDB](./LedisDB/) | [官网](http://ledisdb.com) | [repo](https://github.com/ledisdb/ledisdb) | KV | Siddon Tang | MIT License | 2014 | [DB-Engines](https://db-engines.com/en/system/LedisDB) [DBDB](https://dbdb.io/db/ledisdb) |
| 126 | LevelDB | [LevelDB](./LevelDB/) | [官网](http://leveldb.org)  ⚠️链接失效 | [repo](https://github.com/google/leveldb) | KV | Google | BSD License | 2011 | [DB-Engines](https://db-engines.com/en/system/LevelDB) [DBDB](https://dbdb.io/db/leveldb) |
| 127 | LinDB | [LinDB](./LinDB/) | [官网](https://www.lindb.io/oss/lindb) | [repo](https://github.com/lindb/lindb) | 时序 | ELEME | Apache v2 | 2019 | [DBDB](https://dbdb.io/db/lindb) |
| 128 | LMDB | [LMDB](./LMDB/) | [官网](https://lmdb.tech)  ⚠️本次网络不可达 | [repo](https://github.com/LMDB/lmdb) | KV | Symas | OpenLDAP Public License | 2011 | [DB-Engines](https://db-engines.com/en/system/LMDB) [DBDB](https://dbdb.io/db/lmdb) |
| 129 | LotusDB | [LotusDB](./LotusDB/) | [官网](https://lotusdblabs.github.io) | [repo](https://github.com/lotusdblabs/lotusdb) | SQL | Rose Duan | Apache v2 | 2021 | [DBDB](https://dbdb.io/db/lotusdb) |
| 130 | MariaDB | [MariaDB](./MariaDB/) | [官网](https://mariadb.com/) | [repo](https://github.com/MariaDB/server) | SQL、文档、图、空间 | MariaDB plc (MariaDB Enterprise Platform and MariaDB) The lead developer Monty Widenius is the original author of MySQL | GPL v2 | 2009 | [DB-Engines](https://db-engines.com/en/system/MariaDB) [DBDB](https://dbdb.io/db/mariadb) |
| 131 | MarkLogic | [MarkLogic](./MarkLogic/) | [官网](http://www.progress.com/marklogic) | — | 文档、向量、搜索 | MarkLogic Corp. | Proprietary | 2001 | [DB-Engines](https://db-engines.com/en/system/MarkLogic) [DBDB](https://dbdb.io/db/marklogic) |
| 132 | MatrixOne | [MatrixOne](./MatrixOne/) | [官网](https://www.matrixorigin.io) | [repo](https://github.com/matrixorigin/matrixone) | SQL、OLAP、流 | MatrixOrigin Inc. | Apache v2 | 2021 | [DB-Engines](https://db-engines.com/en/system/MatrixOne) [DBDB](https://dbdb.io/db/matrixone) |
| 133 | MaxDB | [MaxDB](./MaxDB/) | [官网](http://maxdb.sap.com)  ⚠️HTTP 502 | — | SQL | SAP, acquired from Software AG (Adabas-D) in 1997 | Proprietary | 1984 | [DB-Engines](https://db-engines.com/en/system/MaxDB) [DBDB](https://dbdb.io/db/maxdb) |
| 134 | Meilisearch | [Meilisearch](./Meilisearch/) | [官网](https://github.com/meilisearch/meilisearch) | [repo](https://github.com/meilisearch/meilisearch) | 向量、搜索 | Meilisearch SAS | MIT License | 2020 | [DB-Engines](https://db-engines.com/en/system/Meilisearch) [DBDB](https://dbdb.io/db/meilisearch) |
| 135 | Memcached | [Memcached](./Memcached/) | [官网](http://www.memcached.org/) | [repo](https://github.com/memcached/memcached) | KV | Danga Interactive originally developed by Brad Fitzpatrick for LiveJournal | BSD License | 2003 | [DB-Engines](https://db-engines.com/en/system/Memcached) [DBDB](https://dbdb.io/db/memcached) |
| 136 | Memgraph | [Memgraph](./Memgraph/) | [官网](https://memgraph.com) | [repo](https://github.com/memgraph/memgraph) | 图 | Memgraph Ltd | Business Source License | 2017 | [DB-Engines](https://db-engines.com/en/system/Memgraph) [DBDB](https://dbdb.io/db/memgraph) |
| 137 | Microsoft Access | [Microsoft Access](./Microsoft Access/) | [官网](https://www.microsoft.com/en-us/microsoft-365/access) | — | SQL | Microsoft | 商业或开源（DB-Engines 未给出具体许可证） | 1992 | [DB-Engines](https://db-engines.com/en/system/Microsoft+Access) |
| 138 | Microsoft Azure AI Search | [Microsoft Azure AI Search](./Microsoft Azure AI Search/) | [官网](https://azure.microsoft.com/en-us/services/search/) | — | 向量、搜索 | Microsoft | 商业或开源（DB-Engines 未给出具体许可证） | 2015 | [DB-Engines](https://db-engines.com/en/system/Microsoft+Azure+AI+Search) |
| 139 | Microsoft Azure Cosmos DB | [Microsoft Azure CosmosDB](./Microsoft Azure CosmosDB/) | [官网](https://azure.microsoft.com/en-us/products/cosmos-db) | — | 文档、KV、宽列、图、搜索、空间 | Microsoft | Proprietary | 2014 | [DB-Engines](https://db-engines.com/en/system/Microsoft+Azure+Cosmos+DB) [DBDB](https://dbdb.io/db/cosmos-db) |
| 140 | Microsoft Azure Data Explorer | [Microsoft Azure Data Explorer](./Microsoft Azure Data Explorer/) | [官网](https://azure.microsoft.com/services/data-explorer/) | — | SQL、文档、图、时序、搜索、空间 | Microsoft | 商业或开源（DB-Engines 未给出具体许可证） | 2019 | [DB-Engines](https://db-engines.com/en/system/Microsoft+Azure+Data+Explorer) |
| 141 | Microsoft Azure SQL Database | [Microsoft Azure SQL Database](./Microsoft Azure SQL Database/) | [官网](https://azure.microsoft.com/en-us/products/azure-sql/database/) | — | SQL、文档、图、空间 | Microsoft | 商业或开源（DB-Engines 未给出具体许可证） | 2010 | [DB-Engines](https://db-engines.com/en/system/Microsoft+Azure+SQL+Database) |
| 142 | Microsoft Azure Synapse Analytics | [Microsoft Azure Synapse Analytics](./Microsoft Azure Synapse Analytics/) | [官网](https://azure.microsoft.com/services/synapse-analytics/) | — | SQL | Microsoft | 商业或开源（DB-Engines 未给出具体许可证） | 2016 | [DB-Engines](https://db-engines.com/en/system/Microsoft+Azure+Synapse+Analytics) |
| 143 | Microsoft Azure Table Storage | [Microsoft Azure Table Storage](./Microsoft Azure Table Storage/) | [官网](https://azure.microsoft.com/en-us/services/storage/tables/) | — | 宽列 | Microsoft | 商业或开源（DB-Engines 未给出具体许可证） | 2012 | [DB-Engines](https://db-engines.com/en/system/Microsoft+Azure+Table+Storage) |
| 144 | Microsoft Fabric | [Microsoft Fabric](./Microsoft Fabric/) | [官网](https://www.microsoft.com/en-us/microsoft-fabric) | — | SQL | Microsoft | — | — | [DB-Engines](https://db-engines.com/en/system/Microsoft+Fabric) |
| 145 | Microsoft SQL Server | [Microsoft SQL Server](./Microsoft SQL Server/) | [官网](https://www.microsoft.com/en-us/sql-server/) | — | SQL、文档、图、空间 | Microsoft | 商业或开源（DB-Engines 未给出具体许可证） | 1989 | [DB-Engines](https://db-engines.com/en/system/Microsoft+SQL+Server) |
| 146 | Milvus | [Milvus](./Milvus/) | [官网](https://milvus.io)  ⚠️HTTP 302 | [repo](https://github.com/milvus-io/milvus) | 向量 | The Milvus Project | Apache v2 | 2019 | [DB-Engines](https://db-engines.com/en/system/Milvus) [DBDB](https://dbdb.io/db/milvus) |
| 147 | MMKV | [MMKV](./MMKV/) | [官网](https://github.com/Tencent/MMKV) | [repo](https://github.com/Tencent/MMKV) | KV | — | BSD License | 2018 | [DBDB](https://dbdb.io/db/mmkv) |
| 148 | MonetDB | [MonetDB](./MonetDB/) | [官网](https://www.monetdb.org) | [repo](https://github.com/MonetDB/MonetDB) | SQL、OLAP、文档、空间 | MonetDB BV | Mozilla Public License | 2004 | [DB-Engines](https://db-engines.com/en/system/MonetDB) [DBDB](https://dbdb.io/db/monetdb) |
| 149 | MongoDB | [MongoDB](./MongoDB/) | [官网](https://www.mongodb.com) | [repo](https://github.com/mongodb) | 文档、KV、时序、向量、搜索、空间 | MongoDB, Inc | Server Side Public License | 2009 | [DB-Engines](https://db-engines.com/en/system/MongoDB) [DBDB](https://dbdb.io/db/mongodb) |
| 150 | MonographDB | [MonographDB](./MonographDB/) | [官网](http://monographdata.com) | — | SQL、文档 | MonographDB | Proprietary | 2021 | [DBDB](https://dbdb.io/db/monographdb) |
| 151 | MyScaleDB | [MyScaleDB](./MyScaleDB/) | [官网](https://myscale.com) | [repo](https://github.com/myscale/MyScaleDB) | OLAP | Moqi Technology | Apache v2 | 2021 | [DBDB](https://dbdb.io/db/myscaledb) |
| 152 | MySQL | [MySQL](./MySQL/) | [官网](https://www.mysql.com) | [repo](https://github.com/mysql/mysql-server) | SQL、文档、空间 | Oracle since 2010, originally MySQL AB, then Sun | GPL v2 | 1995 | [DB-Engines](https://db-engines.com/en/system/MySQL) [DBDB](https://dbdb.io/db/mysql) |
| 153 | Nebula Graph | [Nebula Graph](./Nebula Graph/) | [官网](https://github.com/vesoft-inc/nebula) | [repo](https://github.com/vesoft-inc/nebula) | 图 | Vesoft Inc. | Apache v2 | 2019 | [DB-Engines](https://db-engines.com/en/system/NebulaGraph) [DBDB](https://dbdb.io/db/nebula-graph) |
| 154 | NebulaGraph | [NebulaGraph](./NebulaGraph/) | [官网](https://github.com/vesoft-inc/nebula) | [repo](https://github.com/vesoft-inc/nebula) | 图 | Vesoft Inc. | Apache v2 | 2019 | [DB-Engines](https://db-engines.com/en/system/NebulaGraph) [DBDB](https://dbdb.io/db/nebula-graph) |
| 155 | Neo4j | [Neo4j](./Neo4j/) | [官网](https://neo4j.com) | [repo](https://github.com/neo4j/neo4j) | 图 | Neo4j, Inc. | 商业或开源（DB-Engines 未给出具体许可证） | 2007 | [DB-Engines](https://db-engines.com/en/system/Neo4j) [DBDB](https://dbdb.io/db/neo4j) |
| 156 | nessDB | [nessDB](./nessDB/) | [官网](https://github.com/BohuTANG/nessDB) | [repo](https://github.com/BohuTANG/nessDB) | KV、嵌入式 | Bohu Tang | BSD License | 2011 | [DBDB](https://dbdb.io/db/nessdb) |
| 157 | Netezza | [Netezza](./Netezza/) | [官网](https://www.ibm.com) | — | SQL、OLAP | IBM | Proprietary | 2000 | [DB-Engines](https://db-engines.com/en/system/Netezza) [DBDB](https://dbdb.io/db/netezza) |
| 158 | Neug | [Neug](./Neug/) | [官网](https://graphscope.io/neug) | [repo](https://github.com/alibaba/neug) | 图、嵌入式 | Alibaba Group | Apache v2 | 2026 | [DBDB](https://dbdb.io/db/neug) |
| 159 | NeuroDB | [NeuroDB](./NeuroDB/) | [官网](https://neurodb.org) | [repo](https://github.com/pangguoming/neurodb-pages) | 图 | Pang Guoming | Proprietary | 2020 | [DBDB](https://dbdb.io/db/neurodb) |
| 160 | NutsDB | [NutsDB](./NutsDB/) | [官网](https://xujiajun.cn/nutsdb) | [repo](https://github.com/nutsdb/nutsdb) | KV | Jiajun Xu | Apache v2 | 2018 | [DBDB](https://dbdb.io/db/nutsdb) |
| 161 | OceanBase | [OceanBase](./OceanBase/) | [官网](https://en.oceanbase.com/) | [repo](https://github.com/oceanbase/oceanbase) | SQL、文档、宽列、向量 | OceanBase previously Alibaba and Ant Group | Mulan PubL v2 | 2010 | [DB-Engines](https://db-engines.com/en/system/OceanBase) [DBDB](https://dbdb.io/db/oceanbase) |
| 162 | OnceDB | [OnceDB](./OnceDB/) | [官网](https://oncedb.com) | [repo](https://github.com/OnceDoc/OnceDB) | KV | OnceAI | Proprietary | 2016 | [DBDB](https://dbdb.io/db/oncedb) |
| 163 | OpenEdge | [OpenEdge](./OpenEdge/) | [官网](https://www.progress.com/openedge) | — | SQL | Progress Software Corporation | Proprietary | 1984 | [DB-Engines](https://db-engines.com/en/system/OpenEdge) [DBDB](https://dbdb.io/db/openedge) |
| 164 | openGauss / GaussDB | [GaussDB](./GaussDB/) | [官网](https://e.huawei.com/en/solutions/cloud-computing/big-data/gaussdb-distributed-database)  ⚠️本次网络不可达 | [repo](https://github.com/openGauss/openGauss-server) | SQL、文档、空间 | Huawei and openGauss community | Proprietary | 2019 | [DB-Engines](https://db-engines.com/en/system/openGauss) [DBDB](https://dbdb.io/db/gaussdb) |
| 165 | openGemini | [openGemini](./openGemini/) | [官网](http://www.opengemini.org/) | [repo](https://github.com/openGemini) | 时序 | Huawei and openGemini community | Apache v2 | 2022 | [DB-Engines](https://db-engines.com/en/system/openGemini) [DBDB](https://dbdb.io/db/opengemini) |
| 166 | OpenMLDB | [OpenMLDB](./OpenMLDB/) | [官网](https://github.com/4paradigm/OpenMLDB) | [repo](https://github.com/4paradigm/OpenMLDB) | SQL、时序 | 4 Paradigm Inc. | Apache v2 | 2020 | [DB-Engines](https://db-engines.com/en/system/OpenMLDB) [DBDB](https://dbdb.io/db/openmldb) |
| 167 | OpenSearch | [OpenSearch](./OpenSearch/) | [官网](https://github.com/opensearch-project) | [repo](https://github.com/opensearch-project) | 向量、搜索 | The OpenSearch Software Foundation | Apache v2 | 2021 | [DB-Engines](https://db-engines.com/en/system/OpenSearch) [DBDB](https://dbdb.io/db/opensearch) |
| 168 | OpenViking | [OpenViking](./OpenViking/) | [官网](https://openviking.ai) | [repo](https://github.com/volcengine/OpenViking) | 文档、向量 | — | AGPL v3 | 2026 | [DBDB](https://dbdb.io/db/openviking) |
| 169 | Oracle | [Oracle](./Oracle/) | [官网](https://www.oracle.com/database/) | — | SQL、文档、图、向量、空间 | Oracle | Proprietary | 1980 | [DB-Engines](https://db-engines.com/en/system/Oracle) [DBDB](https://dbdb.io/db/oracle) |
| 170 | Oracle NoSQL | [Oracle NoSQL](./Oracle NoSQL/) | [官网](https://github.com/oracle/nosql) | [repo](https://github.com/oracle/nosql) | SQL、文档、KV | Oracle | 商业或开源（DB-Engines 未给出具体许可证） | 2011 | [DB-Engines](https://db-engines.com/en/system/Oracle+NoSQL) [DBDB](https://dbdb.io/db/oracle-nosql) |
| 171 | OrientDB | [OrientDB](./OrientDB/) | [官网](https://orientdb.dev) | [repo](https://github.com/orientechnologies/orientdb) | 文档、KV、图 | OrientDB LTD; CallidusCloud; SAP | Apache v2 | 2010 | [DB-Engines](https://db-engines.com/en/system/OrientDB) [DBDB](https://dbdb.io/db/orientdb) |
| 172 | OushuDB | [OushuDB](./OushuDB/) | [官网](http://www.oushu.com) | — | SQL | Oushu | 商业或开源（DB-Engines 未给出具体许可证） | 2016 | [DB-Engines](https://db-engines.com/en/system/OushuDB) [DBDB](https://dbdb.io/db/oushudb) |
| 173 | Percona Server for MySQL | [Percona Server for MySQL](./Percona Server for MySQL/) | [官网](https://www.percona.com/software/mysql-database/percona-server) | [repo](https://github.com/mysql/mysql-server) | SQL | Percona | 商业或开源（DB-Engines 未给出具体许可证） | 2008 | [DB-Engines](https://db-engines.com/en/system/Percona+Server+for+MySQL) |
| 174 | PhotonDB | [PhotonDB](./PhotonDB/) | [官网](https://photondb.io) | [repo](https://github.com/photondb/photondb) | KV | Huachao Huang | Apache v2 | 2022 | [DBDB](https://dbdb.io/db/photondb) |
| 175 | PieCloudDB | [PieCloudDB](./PieCloudDB/) | [官网](https://www.openpie.com) | — | SQL、OLAP | OpenPie | Proprietary | 2021 | [DB-Engines](https://db-engines.com/en/system/PieCloudDB) [DBDB](https://dbdb.io/db/pieclouddb) |
| 176 | Pika | [Pika](./Pika/) | [官网](https://github.com/OpenAtomFoundation/pikiwidb) | [repo](https://github.com/OpenAtomFoundation/pikiwidb) | KV | Qihoo | MIT License | 2014 | [DBDB](https://dbdb.io/db/pika) |
| 177 | Pinecone | [Pinecone](./Pinecone/) | [官网](https://www.pinecone.io) | [repo](https://github.com/pinecone-io/pinecone-python-client) | 向量、搜索 | Pinecone Systems, Inc | Proprietary | 2019 | [DB-Engines](https://db-engines.com/en/system/Pinecone) [DBDB](https://dbdb.io/db/pinecone) |
| 178 | PinusDB | [PinusDB](./PinusDB/) | [官网](http://www.pinusdb.cn) | [repo](https://github.com/pinusdb/pinusdb) | 时序 | ChangSha JuSong Soft | GPL v3 | 2019 | [DBDB](https://dbdb.io/db/pinusdb) |
| 179 | PlanetScale | [PlanetScale](./PlanetScale/) | [官网](https://planetscale.com) | — | SQL、文档、空间 | PlanetScale | Proprietary | 2020 | [DB-Engines](https://db-engines.com/en/system/PlanetScale) [DBDB](https://dbdb.io/db/planetscale) |
| 180 | PoloDB | [PoloDB](./PoloDB/) | [官网](https://www.polodb.org) | [repo](https://github.com/PoloDB/PoloDB) | KV | Vincent Chen | Apache v2 | 2020 | [DBDB](https://dbdb.io/db/polodb) |
| 181 | PostGIS | [PostGIS](./PostGIS/) | [官网](https://postgis.net/) | [repo](https://github.com/postgis/postgis) | SQL、空间 | — | 商业或开源（DB-Engines 未给出具体许可证） | 2005 | [DB-Engines](https://db-engines.com/en/system/PostGIS) |
| 182 | PostgreSQL | [PostgreSQL](./PostgreSQL/) | [官网](https://www.postgresql.org) | [repo](https://github.com/postgres/postgres) | SQL、文档、图、向量、空间 | PostgreSQL Global Development Group www.postgresql.org/­developer | PostgreSQL License | 1989 | [DB-Engines](https://db-engines.com/en/system/PostgreSQL) [DBDB](https://dbdb.io/db/postgresql) |
| 183 | PouchDB | [PouchDB](./PouchDB/) | [官网](https://pouchdb.com) | [repo](https://github.com/apache/pouchdb) | 文档 | Apache Software Foundation | Apache v2 | 2012 | [DB-Engines](https://db-engines.com/en/system/PouchDB) [DBDB](https://dbdb.io/db/pouchdb) |
| 184 | Presto | [Presto](./Presto/) | [官网](https://prestodb.io/) | [repo](https://github.com/prestodb/presto) | SQL | Facebook; Presto Foundation | 商业或开源（DB-Engines 未给出具体许可证） | 2013 | [DB-Engines](https://db-engines.com/en/system/Presto) |
| 185 | Prometheus | [Prometheus](./Prometheus/) | [官网](https://prometheus.io) | [repo](https://github.com/prometheus/prometheus) | 时序 | SoundCloud | Apache v2 | 2015 | [DB-Engines](https://db-engines.com/en/system/Prometheus) [DBDB](https://dbdb.io/db/prometheus) |
| 186 | ProtonBase | [ProtonBase](./ProtonBase/) | [官网](https://protonbase.com) | — | OLAP | Xiaozhi Technology | Proprietary | 2021 | [DBDB](https://dbdb.io/db/protonbase) |
| 187 | Qdrant | [Qdrant](./Qdrant/) | [官网](https://github.com/qdrant/qdrant) | [repo](https://github.com/qdrant/qdrant) | 向量、搜索 | Qdrant | Apache v2 | 2021 | [DB-Engines](https://db-engines.com/en/system/Qdrant) [DBDB](https://dbdb.io/db/qdrant) |
| 188 | QuestDB | [QuestDB](./QuestDB/) | [官网](https://questdb.com) | [repo](https://github.com/questdb/questdb) | SQL、时序 | QuestDB Technology Inc | Apache v2 | 2014 | [DB-Engines](https://db-engines.com/en/system/QuestDB) [DBDB](https://dbdb.io/db/questdb) |
| 189 | RadonDB | [RadonDB](./RadonDB/) | [官网](http://radondb.io) | [repo](https://github.com/radondb/radon) | SQL、分布式 | Yunify Technologies | GPL v3 | 2018 | [DBDB](https://dbdb.io/db/radondb) |
| 190 | RapidsDB | [RapidsDB](./RapidsDB/) | [官网](https://rapidsdb.com) | — | OLAP | Boray Data Technology | Proprietary | 2014 | [DBDB](https://dbdb.io/db/rapidsdb) |
| 191 | RavenDB | [RavenDB](./RavenDB/) | [官网](https://ravendb.net) | [repo](https://github.com/ravendb/ravendb) | 文档、图、时序、空间 | Hibernating Rhinos | AGPL v3 | 2010 | [DB-Engines](https://db-engines.com/en/system/RavenDB) [DBDB](https://dbdb.io/db/ravendb) |
| 192 | Realm | [Realm](./Realm/) | [官网](https://realm.io/) | [repo](https://github.com/realm/realm-core) | 文档 | Realm, acquired by MongoDB in May 2019 | Apache v2 | 2014 | [DB-Engines](https://db-engines.com/en/system/Realm) [DBDB](https://dbdb.io/db/realm) |
| 193 | Redis | [Redis](./Redis/) | [官网](https://redis.com/) | [repo](https://github.com/redis) | 文档、KV、图、时序、向量、搜索、空间 | Redis project core team, inspired by Salvatore Sanfilippo Development sponsored by Redis Inc. | BSD License | 2009 | [DB-Engines](https://db-engines.com/en/system/Redis) [DBDB](https://dbdb.io/db/redis) |
| 194 | RefineDB | [RefineDB](./RefineDB/) | [官网](https://github.com/losfair/RefineDB) | [repo](https://github.com/losfair/RefineDB) | 文档 | Heyang Zhou | MIT License | 2021 | [DBDB](https://dbdb.io/db/refinedb) |
| 195 | RethinkDB | [RethinkDB](./RethinkDB/) | [官网](https://rethinkdb.com/) | [repo](https://github.com/rethinkdb/rethinkdb) | 文档、空间 | The Linux Foundation since July 2017 | Apache v2 | 2009 | [DB-Engines](https://db-engines.com/en/system/RethinkDB) [DBDB](https://dbdb.io/db/rethinkdb) |
| 196 | Riak KV | [Riak KV](./Riak KV/) | — | — | KV | OpenSource, formerly Basho Technologies | 商业或开源（DB-Engines 未给出具体许可证） | 2009 | [DB-Engines](https://db-engines.com/en/system/Riak+KV) |
| 197 | RocksDB | [RocksDB](./RocksDB/) | [官网](https://rocksdb.org) | [repo](https://github.com/facebook/rocksdb) | KV | Facebook, Inc. | Apache v2 | 2013 | [DB-Engines](https://db-engines.com/en/system/RocksDB) [DBDB](https://dbdb.io/db/rocksdb) |
| 198 | Rockset | [Rockset](./Rockset/) | [官网](https://openai.com/index/openai-acquires-rockset) | [repo](https://github.com/rocksetinc/rockset) | SQL、OLAP、文档、搜索 | Rockset | Proprietary | 2019 | [DB-Engines](https://db-engines.com/en/system/Rockset) [DBDB](https://dbdb.io/db/rockset) |
| 199 | RoseDB | [RoseDB](./RoseDB/) | [官网](https://rosedblabs.github.io) | [repo](https://github.com/rosedblabs/rosedb) | KV | RoseDB Labs | MIT License | 2020 | [DBDB](https://dbdb.io/db/rosedb) |
| 200 | SAP Adaptive Server | [SAP Adaptive Server](./SAP Adaptive Server/) | [官网](https://www.sap.com/products/technology-platform/sybase-ase.html) | — | SQL、空间 | SAP, Sybase | 商业或开源（DB-Engines 未给出具体许可证） | 1987 | [DB-Engines](https://db-engines.com/en/system/SAP+Adaptive+Server) |
| 201 | SAP HANA | [SAP HANA](./SAP HANA/) | [官网](https://www.sap.com/products/hana.html) | — | SQL、文档、图、空间 | SAP | 商业或开源（DB-Engines 未给出具体许可证） | 2010 | [DB-Engines](https://db-engines.com/en/system/SAP+HANA) |
| 202 | SAP IQ | [SAP IQ](./SAP IQ/) | [官网](https://www.sap.com/products/technology-platform/sybase-iq-big-data-management.html) | — | SQL | SAP, formerly Sybase | 商业或开源（DB-Engines 未给出具体许可证） | 1994 | [DB-Engines](https://db-engines.com/en/system/SAP+IQ) |
| 203 | SAP SQL Anywhere | [SAP SQL Anywhere](./SAP SQL Anywhere/) | [官网](https://www.sap.com/products/technology-platform/sql-anywhere.html) | — | SQL | SAP formerly Sybase | 商业或开源（DB-Engines 未给出具体许可证） | 1992 | [DB-Engines](https://db-engines.com/en/system/SAP+SQL+Anywhere) |
| 204 | sboxdb | [sboxdb](./sboxdb/) | [官网](https://github.com/maxnilz/sboxdb) | [repo](https://github.com/maxnilz/sboxdb) | SQL | — | — | 2024 | [DBDB](https://dbdb.io/db/sboxdb) |
| 205 | ScopeDB | [ScopeDB](./ScopeDB/) | [官网](https://www.scopedb.io) | — | SQL | ScopeDB | Proprietary | 2024 | [DBDB](https://dbdb.io/db/scopedb) |
| 206 | ScyllaDB | [ScyllaDB](./ScyllaDB/) | [官网](https://www.scylladb.com) | [repo](https://github.com/scylladb/scylla) | KV、宽列 | ScyllaDB | AGPL v3 | 2015 | [DB-Engines](https://db-engines.com/en/system/ScyllaDB) [DBDB](https://dbdb.io/db/scylla) |
| 207 | SeekDB | [SeekDB](./SeekDB/) | [官网](https://seekdb.ai) | [repo](https://github.com/oceanbase/seekdb) | SQL、文档、向量、空间、嵌入式 | Beijing OceanBase Technology Co., Ltd. | Apache v2 | 2025 | [DBDB](https://dbdb.io/db/seekdb) |
| 208 | SequoiaDB | [SequoiaDB](./SequoiaDB/) | [官网](http://www.sequoiadb.com/) | [repo](https://github.com/SequoiaDB/SequoiaDB) | SQL、文档 | Sequoiadb Ltd. | AGPL v3 | 2013 | [DB-Engines](https://db-engines.com/en/system/Sequoiadb) [DBDB](https://dbdb.io/db/sequoiadb) |
| 209 | ShannonBase | [ShannonBase](./ShannonBase/) | [官网](https://www.shannonbase.org) | [repo](https://github.com/Shannon-Data/ShannonBase) | OLAP | ShannonAI, Inc. | GPL v2 | 2024 | [DBDB](https://dbdb.io/db/shannonbase) |
| 210 | ShardingSphere | [ShardingSphere](./ShardingSphere/) | [官网](https://shardingsphere.apache.org) | [repo](https://github.com/apache/shardingsphere) | 多模型 | Apache Software Foundation | Apache v2 | 2016 | [DBDB](https://dbdb.io/db/shardingsphere) |
| 211 | SingleStore | [SingleStore](./SingleStore/) | [官网](https://www.singlestore.com) | [repo](https://github.com/memlabs/singlestore) | SQL、OLAP、文档、时序、向量、空间 | SingleStore Inc. | Proprietary | 2013 | [DB-Engines](https://db-engines.com/en/system/SingleStore) [DBDB](https://dbdb.io/db/singlestore) |
| 212 | Snowflake | [Snowflake](./Snowflake/) | [官网](https://www.snowflake.com) | — | SQL、OLAP | Snowflake Computing Inc. | Proprietary | 2014 | [DB-Engines](https://db-engines.com/en/system/Snowflake) [DBDB](https://dbdb.io/db/snowflake) |
| 213 | SpatiaLite | [SpatiaLite](./SpatiaLite/) | [官网](https://www.gaia-gis.it/fossil/libspatialite/index) | [repo](https://github.com/gaia-gis/spatialite) | SQL、空间 | Alessandro Furieri | 商业或开源（DB-Engines 未给出具体许可证） | 2008 | [DB-Engines](https://db-engines.com/en/system/SpatiaLite) |
| 214 | Sphinx | [Sphinx](./Sphinx/) | [官网](http://sphinxsearch.com) | [repo](https://github.com/sphinxsearch/sphinx) | 搜索 | Sphinx Technologies Inc. | 商业或开源（DB-Engines 未给出具体许可证） | 2001 | [DB-Engines](https://db-engines.com/en/system/Sphinx) [DBDB](https://dbdb.io/db/sphinx) |
| 215 | Splunk | [Splunk](./Splunk/) | [官网](https://www.splunk.com) | — | 搜索 | Splunk Inc. | Proprietary | 2003 | [DB-Engines](https://db-engines.com/en/system/Splunk) [DBDB](https://dbdb.io/db/splunk) |
| 216 | SQLite | [SQLite](./SQLite/) | [官网](https://sqlite.org) | [repo](https://github.com/sqlite/sqlite) | SQL | Dwayne Richard Hipp | Public Domain | 2000 | [DB-Engines](https://db-engines.com/en/system/SQLite) [DBDB](https://dbdb.io/db/sqlite) |
| 217 | SSDB | [SSDB](./SSDB/) | [官网](http://ssdb.io) | [repo](https://github.com/ideawu/ssdb) | KV | Zuyang Wu | BSD License | 2013 | [DBDB](https://dbdb.io/db/ssdb) |
| 218 | Stardog | [Stardog](./Stardog/) | [官网](https://www.stardog.com) | — | 图 | Stardog-Union | Proprietary | 2010 | [DB-Engines](https://db-engines.com/en/system/Stardog) [DBDB](https://dbdb.io/db/stardog) |
| 219 | StarRocks | [StarRocks](./StarRocks/) | [官网](https://www.starrocks.io) | [repo](https://github.com/StarRocks/starrocks) | SQL、OLAP | The Linux Foundation since Feb 2023 | Apache v2 | 2020 | [DB-Engines](https://db-engines.com/en/system/StarRocks) [DBDB](https://dbdb.io/db/starrocks) |
| 220 | StoneDB | [StoneDB](./StoneDB/) | [官网](https://stonedb.io) | [repo](https://github.com/StoneAtom/stonedb) | OLAP | StoneAtom | — | 2022 | [DBDB](https://dbdb.io/db/stonedb) |
| 221 | TDengine | [TDengine](./TDengine/) | [官网](https://github.com/taosdata/TDengine) | [repo](https://github.com/taosdata/TDengine) | SQL、时序 | TDEngine, previously Taos Data | AGPL v3 | 2019 | [DB-Engines](https://db-engines.com/en/system/TDengine) [DBDB](https://dbdb.io/db/tdengine) |
| 222 | Tencent TDSQL | [TDSQL](./TDSQL/) | [官网](http://tdsql.org)  ⚠️HTTP 502 | [repo](https://github.com/Tencent/TencentDB) | SQL | Tencent | — | 2012 | [DBDB](https://dbdb.io/db/tdsql) |
| 223 | Tendis | [Tendis](./Tendis/) | [官网](http://tendis.cn) | [repo](https://github.com/Tencent/Tendis) | KV | Tencent | GPL v3 | 2018 | [DBDB](https://dbdb.io/db/tendis) |
| 224 | TensorBase | [TensorBase](./TensorBase/) | [官网](https://tensorbase.io) | [repo](https://github.com/tensorbase/tensorbase) | OLAP | TensorBase | Apache v2 | 2020 | [DBDB](https://dbdb.io/db/tensorbase) |
| 225 | Tera | [Tera](./Tera/) | [官网](https://github.com/baidu/tera) | [repo](https://github.com/baidu/tera) | KV | Baidu, Inc. | BSD License | 2014 | [DBDB](https://dbdb.io/db/tera) |
| 226 | Teradata | [Teradata](./Teradata/) | [官网](https://www.teradata.com) | — | SQL、文档、图、时序、空间 | Teradata | Proprietary | 1984 | [DB-Engines](https://db-engines.com/en/system/Teradata) [DBDB](https://dbdb.io/db/teradata) |
| 227 | TerarkDB | [TerarkDB](./TerarkDB/) | [官网](https://github.com/bytedance/terarkdb) | [repo](https://github.com/bytedance/terarkdb) | KV | ByteDance, originally Terark | Apache v2 | 2016 | [DB-Engines](https://db-engines.com/en/system/TerarkDB) [DBDB](https://dbdb.io/db/terarkdb) |
| 228 | TiDB | [TiDB](./TiDB/) | [官网](https://pingcap.com/) | [repo](https://github.com/pingcap/tidb) | SQL、OLAP、向量 | PingCAP, Inc. | Apache v2 | 2016 | [DB-Engines](https://db-engines.com/en/system/TiDB) [DBDB](https://dbdb.io/db/tidb) |
| 229 | TigerGraph | [TigerGraph](./TigerGraph/) | [官网](https://www.tigergraph.com) | [repo](https://github.com/tigergraph/tigergraph) | 图 | TigerGraph | Proprietary | 2017 | [DB-Engines](https://db-engines.com/en/system/TigerGraph) [DBDB](https://dbdb.io/db/tigergraph) |
| 230 | TiKV | [TiKV](./TiKV/) | [官网](https://tikv.org) | [repo](https://github.com/tikv/tikv) | KV | PingCAP | Apache v2 | 2016 | [DBDB](https://dbdb.io/db/tikv) |
| 231 | Titan | [Titan](./Titan/) | [官网](http://titandb.io) | [repo](https://github.com/thinkaurelius/titan) | 图 | Aurelius | Apache v2 | 2012 | [DBDB](https://dbdb.io/db/titan) |
| 232 | Tonbo | [Tonbo](./Tonbo/) | [官网](https://tonbo.io) | [repo](https://github.com/tonbo-io/tonbo) | SQL | Tzu Gwo | Apache v2 | 2024 | [DBDB](https://dbdb.io/db/tonbo) |
| 233 | ToplingDB | [ToplingDB](./ToplingDB/) | [官网](https://topling.cn) | [repo](https://github.com/topling/toplingdb) | KV | Topling | Apache v2 | 2021 | [DBDB](https://dbdb.io/db/toplingdb) |
| 234 | Trino | [Trino](./Trino/) | [官网](https://trino.io) | [repo](https://github.com/trinodb/trino) | SQL、文档、KV、宽列、时序、搜索、空间 | Trino Software Foundation | Apache v2 | 2012 | [DB-Engines](https://db-engines.com/en/system/Trino) [DBDB](https://dbdb.io/db/trino) |
| 235 | TuGraph | [TuGraph](./TuGraph/) | [官网](https://www.tugraph.org) | [repo](https://github.com/TuGraph-family/tugraph-db) | 图 | — | Apache v2 | 2021 | [DBDB](https://dbdb.io/db/tugraph) |
| 236 | UniData,UniVerse | [UniData,UniVerse](./UniData,UniVerse/) | [官网](https://www.rocketsoftware.com/products/rocket-multivalue-application-development-platform/rocket-unidata) | — | 多值 | Rocket Software | 商业或开源（DB-Engines 未给出具体许可证） | 1985 | [DB-Engines](https://db-engines.com/en/system/UniData%2CUniVerse) |
| 237 | Valkey | [Valkey](./Valkey/) | [官网](https://valkey.io) | [repo](https://github.com/valkey-io/valkey) | KV | The Linux Foundation | BSD License | 2024 | [DB-Engines](https://db-engines.com/en/system/Valkey) [DBDB](https://dbdb.io/db/valkey) |
| 238 | Vearch | [Vearch](./Vearch/) | [官网](https://vearch.github.io) | [repo](https://github.com/vearch/vearch) | 向量、搜索 | JD.com | Apache v2 | 2019 | [DBDB](https://dbdb.io/db/vearch) |
| 239 | VectorSQL | [VectorSQL](./VectorSQL/) | [官网](https://github.com/vectorengine/vectorsql) | [repo](https://github.com/vectorengine/vectorsql) | OLAP | Bohu Tang | Apache v2 | 2020 | [DBDB](https://dbdb.io/db/vectorsql) |
| 240 | VeloDB | [VeloDB](./VeloDB/) | [官网](https://www.velodb.io) | — | OLAP、搜索 | VeloDB Inc. | Proprietary | 2023 | [DBDB](https://dbdb.io/db/velodb) |
| 241 | Vertica | [Vertica](./Vertica/) | [官网](https://www.rocketsoftware.com/en-us/products/vertica?o=vert) | [repo](https://github.com/vertica/vertica) | SQL、OLAP、时序、空间 | OpenText previously Micro Focus and Hewlett Packard | Proprietary | 2005 | [DB-Engines](https://db-engines.com/en/system/Vertica) [DBDB](https://dbdb.io/db/vertica) |
| 242 | VictoriaMetrics | [VictoriaMetrics](./VictoriaMetrics/) | [官网](https://victoriametrics.com) | [repo](https://github.com/VictoriaMetrics/VictoriaMetrics) | 时序 | VictoriaMetrics | Apache v2 | 2018 | [DB-Engines](https://db-engines.com/en/system/VictoriaMetrics) [DBDB](https://dbdb.io/db/victoriametrics) |
| 243 | Virtuoso | [Virtuoso](./Virtuoso/) | [官网](https://virtuoso.openlinksw.com) | — | SQL、文档、图、搜索、空间 | OpenLink Software | 商业或开源（DB-Engines 未给出具体许可证） | 1998 | [DB-Engines](https://db-engines.com/en/system/Virtuoso) [DBDB](https://dbdb.io/db/virtuoso) |
| 244 | Vitess | [Vitess](./Vitess/) | [官网](https://vitess.io) | [repo](https://github.com/vitessio/vitess) | SQL、文档、空间 | The Linux Foundation, PlanetScale | Apache v2 | 2013 | [DB-Engines](https://db-engines.com/en/system/Vitess) [DBDB](https://dbdb.io/db/vitess) |
| 245 | VoltDB | [VoltDB](./VoltDB/) | [官网](https://www.voltactivedata.com) | [repo](https://github.com/voltdb/voltdb) | SQL | VoltDB Inc. | 商业或开源（DB-Engines 未给出具体许可证） | 2010 | [DB-Engines](https://db-engines.com/en/system/VoltDB) [DBDB](https://dbdb.io/db/voltdb) |
| 246 | Weaviate | [Weaviate](./Weaviate/) | [官网](https://github.com/weaviate/weaviate) | [repo](https://github.com/weaviate/weaviate) | 向量、搜索 | Weaviate B.V. | BSD License | 2019 | [DB-Engines](https://db-engines.com/en/system/Weaviate) [DBDB](https://dbdb.io/db/weaviate) |
| 247 | WebScaleSQL | [WebScaleSQL](./WebScaleSQL/) | [官网](http://webscalesql.org) | [repo](https://github.com/facebookarchive/webscalesql-5.6) | SQL | — | GPL v2 | 2014 | [DBDB](https://dbdb.io/db/webscalesql) |
| 248 | WiredTiger | [WiredTiger](./WiredTiger/) | [官网](https://www.mongodb.com) | [repo](https://github.com/mongodb/wiredtiger) | KV | WiredTiger | — | 2008 | [DBDB](https://dbdb.io/db/wiredtiger) |
| 249 | YugabyteDB | [YugabyteDB](./YugabyteDB/) | [官网](https://www.yugabyte.com) | [repo](https://github.com/yugabyte/yugabyte-db) | SQL、文档、宽列 | Yugabyte Inc. | Apache v2 | 2017 | [DB-Engines](https://db-engines.com/en/system/YugabyteDB) [DBDB](https://dbdb.io/db/yugabytedb) |
| 250 | Zvec | [Zvec](./Zvec/) | [官网](https://zvec.org) | [repo](https://github.com/alibaba/zvec) | 向量 | — | Apache v2 | 2023 | [DBDB](https://dbdb.io/db/zvec) |

## 已收录文献

| 数据库 | 论文 | 官方文档/白皮书 | 合计 |
| --- | ---: | ---: | ---: |
| 4D | 0 | 1 | 1 |
| Aerospike | 1 | 1 | 2 |
| Algolia | 0 | 1 | 1 |
| Alibaba Cloud PolarDB | 4 | 1 | 5 |
| Amazon Aurora | 5 | 1 | 6 |
| Amazon CloudSearch | 0 | 1 | 1 |
| Amazon DocumentDB | 1 | 1 | 2 |
| Amazon DynamoDB | 2 | 1 | 3 |
| Amazon Neptune | 0 | 1 | 1 |
| Amazon Redshift | 4 | 1 | 5 |
| Amazon SimpleDB | 0 | 1 | 1 |
| Apache Cassandra | 5 | 1 | 6 |
| Apache CouchDB | 0 | 1 | 1 |
| Apache Derby | 0 | 1 | 1 |
| Apache Drill | 1 | 1 | 2 |
| Apache Druid | 0 | 1 | 1 |
| Apache Flink | 5 | 1 | 6 |
| Apache HBase | 0 | 1 | 1 |
| Apache Hive | 3 | 0 | 3 |
| Apache Ignite | 0 | 1 | 1 |
| Apache Impala | 0 | 1 | 1 |
| Apache IoTDB | 6 | 1 | 7 |
| Apache Jena TDB | 0 | 1 | 1 |
| Apache Phoenix | 0 | 1 | 1 |
| Apache Solr | 0 | 1 | 1 |
| Apache Spark | 6 | 0 | 6 |
| Apache ZooKeeper | 1 | 1 | 2 |
| BaseX | 0 | 1 | 1 |
| Calvin | 1 | 0 | 1 |
| Chroma | 0 | 1 | 1 |
| Citus | 0 | 1 | 1 |
| ClickHouse | 1 | 1 | 2 |
| CloudKit | 1 | 0 | 1 |
| CockroachDB | 3 | 1 | 4 |
| Coherence | 2 | 1 | 3 |
| Couchbase | 2 | 1 | 3 |
| Coveo | 0 | 1 | 1 |
| Databricks | 2 | 1 | 3 |
| Datastax Enterprise | 6 | 1 | 7 |
| Datomic | 0 | 1 | 1 |
| Dgraph | 3 | 0 | 3 |
| DuckDB | 6 | 1 | 7 |
| EDB Postgres | 0 | 1 | 1 |
| Ehcache | 0 | 1 | 1 |
| Elasticsearch | 0 | 1 | 1 |
| Essbase | 0 | 1 | 1 |
| etcd | 0 | 1 | 1 |
| EXASOL | 0 | 1 | 1 |
| Fauna | 1 | 0 | 1 |
| FileMaker | 0 | 1 | 1 |
| Firebase Realtime Database | 5 | 0 | 5 |
| Firebird | 0 | 1 | 1 |
| FoundationDB | 1 | 1 | 2 |
| Galaxybase | 1 | 0 | 1 |
| GBase | 0 | 1 | 1 |
| GemFire | 0 | 1 | 1 |
| Google Cloud Datastore | 2 | 0 | 2 |
| Google Cloud Firestore | 1 | 0 | 1 |
| Google F1 | 2 | 0 | 2 |
| Google Spanner | 1 | 0 | 1 |
| GraphDB | 1 | 1 | 2 |
| Graphite | 1 | 1 | 2 |
| Greenplum | 1 | 0 | 1 |
| H2 | 0 | 1 | 1 |
| Hazelcast | 1 | 1 | 2 |
| IBM Cloudant | 0 | 1 | 1 |
| IBM Db2 | 6 | 1 | 7 |
| Infinispan | 0 | 1 | 1 |
| Infinity | 1 | 0 | 1 |
| InfluxDB | 0 | 1 | 1 |
| Informix | 0 | 1 | 1 |
| Ingres | 1 | 1 | 2 |
| Interbase | 0 | 1 | 1 |
| InterSystems IRIS | 0 | 1 | 1 |
| JanusGraph | 0 | 1 | 1 |
| Kdb | 0 | 1 | 1 |
| LevelDB | 0 | 1 | 1 |
| LinDB | 1 | 0 | 1 |
| LMDB | 0 | 1 | 1 |
| MariaDB | 0 | 1 | 1 |
| MarkLogic | 0 | 1 | 1 |
| MaxDB | 0 | 1 | 1 |
| Meilisearch | 0 | 1 | 1 |
| Memcached | 0 | 1 | 1 |
| Memgraph | 2 | 1 | 3 |
| Microsoft Access | 5 | 1 | 6 |
| Microsoft Azure AI Search | 3 | 1 | 4 |
| Microsoft Azure Cosmos DB | 2 | 1 | 3 |
| Microsoft Azure Data Explorer | 6 | 1 | 7 |
| Microsoft Azure SQL Database | 8 | 1 | 9 |
| Microsoft Azure Synapse Analytics | 6 | 1 | 7 |
| Microsoft Azure Table Storage | 7 | 0 | 7 |
| Microsoft Fabric | 3 | 1 | 4 |
| Microsoft SQL Server | 1 | 1 | 2 |
| MonetDB | 4 | 1 | 5 |
| MongoDB | 15 | 1 | 16 |
| MySQL | 3 | 0 | 3 |
| Nebula Graph | 6 | 0 | 6 |
| NebulaGraph | 0 | 1 | 1 |
| Neo4j | 2 | 1 | 3 |
| OceanBase | 4 | 1 | 5 |
| OpenEdge | 0 | 1 | 1 |
| openGauss / GaussDB | 6 | 1 | 7 |
| OpenSearch | 0 | 1 | 1 |
| Oracle | 1 | 1 | 2 |
| Oracle NoSQL | 7 | 1 | 8 |
| Percona Server for MySQL | 6 | 1 | 7 |
| PlanetScale | 0 | 1 | 1 |
| PostGIS | 0 | 1 | 1 |
| PostgreSQL | 9 | 1 | 10 |
| PouchDB | 0 | 1 | 1 |
| Presto | 3 | 0 | 3 |
| Prometheus | 0 | 1 | 1 |
| Qdrant | 0 | 1 | 1 |
| QuestDB | 0 | 1 | 1 |
| RavenDB | 0 | 1 | 1 |
| Realm | 0 | 1 | 1 |
| Redis | 1 | 1 | 2 |
| RethinkDB | 0 | 1 | 1 |
| Riak KV | 0 | 1 | 1 |
| RocksDB | 2 | 0 | 2 |
| SAP Adaptive Server | 8 | 1 | 9 |
| SAP HANA | 6 | 1 | 7 |
| SAP IQ | 0 | 1 | 1 |
| SAP SQL Anywhere | 0 | 1 | 1 |
| ScyllaDB | 1 | 1 | 2 |
| SingleStore | 1 | 1 | 2 |
| Snowflake | 2 | 1 | 3 |
| SpatiaLite | 0 | 1 | 1 |
| Sphinx | 2 | 1 | 3 |
| Splunk | 0 | 1 | 1 |
| SQLite | 4 | 1 | 5 |
| Stardog | 0 | 1 | 1 |
| StarRocks | 0 | 1 | 1 |
| TDengine | 0 | 1 | 1 |
| Tencent TDSQL | 6 | 1 | 7 |
| Tera | 1 | 0 | 1 |
| Teradata | 3 | 1 | 4 |
| TiDB | 2 | 1 | 3 |
| TigerGraph | 2 | 1 | 3 |
| Trino | 0 | 1 | 1 |
| UniData,UniVerse | 0 | 1 | 1 |
| Valkey | 0 | 1 | 1 |
| Vertica | 1 | 1 | 2 |
| VictoriaMetrics | 0 | 1 | 1 |
| Virtuoso | 0 | 1 | 1 |
| Vitess | 0 | 1 | 1 |
| VoltDB | 4 | 1 | 5 |
| Weaviate | 0 | 1 | 1 |
| WiredTiger | 0 | 1 | 1 |
| YugabyteDB | 1 | 1 | 2 |

已下载论文 **254** 篇，官方文档/白皮书 **130** 份。

### 论文清单

| 数据库 | 文件 | 发表 | 标题 | 来源 |
| --- | --- | --- | --- | --- |
| Aerospike | VLDB2016-AerospikeArchitectureofaRealTimeOperationalDBMS.pdf | VLDB 2016 | Aerospike: Architecture of a Real-Time Operational DBMS | [来源](https://vldb.org/pvldb/vol9/p1389-srinivasan.pdf) |
| Alibaba Cloud PolarDB | FAST2020-POLARDBMeetsComputationalStorageEfficientlySupportAnalyticalWorkloadsinCloudNativeRelationalDatabase.pdf | — | POLARDBMeetsComputationalStorageEfficientlySupportAnalyticalWorkloadsinCloudNativeRelationalDatabase | [来源]() |
| Alibaba Cloud PolarDB | VLDB2018-PolarFSAnUltralowLatencyandFailureResilientDistributedFileSystemforSharedStorageCloudDatabase.pdf | VLDB 2018 | PolarFS: An Ultra-low Latency and Failure Resilient Distributed File System for Shared Storage Cloud Database | [来源](https://vldb.org/pvldb/vol11/p1849-cao.pdf) |
| Alibaba Cloud PolarDB | VLDB2023-PolarDBSCCACloudNativeDatabaseEnsuringLowLatencyforStronglyConsistentReads.pdf | VLDB 2023 | PolarDB-SCC: A Cloud-Native Database Ensuring Low Latency for Strongly Consistent Reads | [来源](https://www.vldb.org/pvldb/vol16/p3754-chen.pdf) |
| Alibaba Cloud PolarDB | VLDB2025-FromScaleUptoScaleOutPolarDBsJourneytoAchieving2BilliontpmC.pdf | VLDB 2025 | From Scale-Up to Scale-Out: PolarDB’s Journey to Achieving 2 Billion tpmC | [来源](https://www.vldb.org/pvldb/vol18/p5059-chen.pdf) |
| Amazon Aurora | SIGMOD2017-AmazonAuroraDesignConsiderationsforHighThroughputCloudNativeRelationalDatabases.pdf | — | AmazonAuroraDesignConsiderationsforHighThroughputCloudNativeRelationalDatabases | [来源]() |
| Amazon Aurora | SIGMOD2018-AmazonAuroraOnAvoidingDistributedConsensusforIOsCommits.pdf | — | AmazonAuroraOnAvoidingDistributedConsensusforIOsCommits | [来源]() |
| Amazon Aurora | SIGMOD2018-AmazonAuroraOnAvoidingDistributedConsensusforIOsCommitsandMembershipChanges.pdf | — | AmazonAuroraOnAvoidingDistributedConsensusforIOsCommitsandMembershipChanges | [来源]() |
| Amazon Aurora | VLDB2024-ResourceManagementinAuroraServerless.pdf | VLDB 2024 | Resource Management in Aurora Serverless | [来源](https://www.vldb.org/pvldb/vol17/p4038-urgaonkar.pdf) |
| Amazon Aurora | VLDB2025-SunStormGeographicallydistributedtransactionsoverAurorastylesystems.pdf | VLDB 2025 | SunStorm: Geographically distributed transactions over Aurora-style systems | [来源](https://www.vldb.org/pvldb/vol18/p5555-nilangekar.pdf) |
| Amazon DocumentDB | VLDB2015-SchemaAgnosticIndexingwithAzureDocumentDB.pdf | VLDB 2015 | Schema-Agnostic Indexing with Azure DocumentDB | [来源](https://vldb.org/pvldb/vol8/p1668-shukla.pdf) |
| Amazon DynamoDB | Paper-AmazonDynamoDBDeveloperGuide.pdf | — | AmazonDynamoDBDeveloperGuide | [来源]() |
| Amazon DynamoDB | Paper-MicrosoftWordsosp067decandia1doc.pdf | — | MicrosoftWordsosp067decandia1doc | [来源]() |
| Amazon Redshift | VLDB2020-FastandEffectiveDistributionKeyRecommendationforAmazonRedshift.pdf | VLDB 2020 | Fast and Effective Distribution-Key Recommendation for Amazon Redshift | [来源](https://www.vldb.org/pvldb/vol13/p2411-parchas.pdf) |
| Amazon Redshift | VLDB2021-TheevolutionofAmazonRedshift.pdf | VLDB 2021 | The evolution of Amazon Redshift | [来源](https://www.vldb.org/pvldb/vol14/p3162-pandis.pdf) |
| Amazon Redshift | VLDB2024-WhyTPCIsNotEnoughAnAnalysisoftheAmazonRedshiftFleet.pdf | VLDB 2024 | Why TPC Is Not Enough: An Analysis of the Amazon Redshift Fleet | [来源](https://www.vldb.org/pvldb/vol17/p3694-saxena.pdf) |
| Amazon Redshift | VLDB2026-IncrementalQueryOptimizerStatisticsinAmazonRedshift.pdf | VLDB 2026 | Incremental Query Optimizer Statistics in Amazon Redshift | [来源](https://www.vldb.org/pvldb/vol19/p3941-pfeil.pdf) |
| Apache Cassandra | SIGMOD2014-ScalableAtomicVisibilitywithRAMPTransactions.pdf | — | ScalableAtomicVisibilitywithRAMPTransactions | [来源]() |
| Apache Cassandra | VLDB2015-UnderstandingtheCausesofConsistencyAnomaliesinApacheCassandra.pdf | VLDB 2015 | Understanding the Causes of Consistency Anomalies in Apache Cassandra | [来源](https://vldb.org/pvldb/vol8/p810-fan.pdf) |
| Apache Cassandra | VLDB2022-TriememtablesinCassandra.pdf | VLDB 2022 | Trie memtables in Cassandra | [来源](https://www.vldb.org/pvldb/vol15/p3359-lambov.pdf) |
| Apache Cassandra | arXiv2013-13092772APracticalDistributedUniversalConstructionwithUnknownParticipants.pdf | — | 13092772APracticalDistributedUniversalConstructionwithUnknownParticipants | [来源]() |
| Apache Cassandra | arXiv2021-210314701ExtendingClassicPaxosforHighperformanceReadModifyWriteRegisters.pdf | — | 210314701ExtendingClassicPaxosforHighperformanceReadModifyWriteRegisters | [来源]() |
| Apache Drill | VLDB2015-SmartDrillDownANewDataExplorationOperator.pdf | VLDB 2015 | Smart Drill-Down: A New Data Exploration Operator | [来源](https://vldb.org/pvldb/vol8/p1928-joglekar.pdf) |
| Apache Flink | VLDB2017-StateManagementinApacheFlinkÆConsistentStatefulDistributedStreamProcessing.pdf | VLDB 2017 | State Management in Apache Flink¬Æ: Consistent Stateful Distributed Stream Processing | [来源](https://vldb.org/pvldb/vol10/p1718-carbone.pdf) |
| Apache Flink | VLDB2021-WatermarksinStreamProcessingSystemsSemanticsandComparativeAnalysisofApacheFlinkandGoogleCloudDataflow.pdf | VLDB 2021 | Watermarks in Stream Processing Systems: Semantics and Comparative Analysis of Apache Flink and Google Cloud Dataflow | [来源](https://www.vldb.org/pvldb/vol14/p3135-begoli.pdf) |
| Apache Flink | VLDB2025-DisaggregatedStateManagementinApacheFlink20.pdf | VLDB 2025 | Disaggregated State Management in Apache Flink 2.0 | [来源](https://www.vldb.org/pvldb/vol18/p4846-mei.pdf) |
| Apache Flink | VLDB2025-NoiseMattersCrossContrastiveLearningforFlinkAnomalyDetection.pdf | VLDB 2025 | Noise Matters: Cross Contrastive Learning for Flink Anomaly Detection | [来源](https://www.vldb.org/pvldb/vol18/p1159-zhuang.pdf) |
| Apache Flink | VLDB2026-ScarfSelfAdaptiveTuningviaMultiObjectiveReinforcementLearningforApacheFlink.pdf | VLDB 2026 | Scarf: Self-Adaptive Tuning via Multi-Objective Reinforcement Learning for Apache Flink | [来源](https://www.vldb.org/pvldb/vol19/p1516-gao.pdf) |
| Apache Hive | VLDB2009-HiveAWarehousingSolutionOveraMapReduceFramework.pdf | VLDB 2009 | Hive - A Warehousing Solution Over a Map-Reduce Framework | [来源](https://vldb.org/pvldb/vol2/vldb09-938.pdf) |
| Apache Hive | VLDB2014-DGFIndexforSmartGridEnhancingHivewithaCostEffectiveMultidimensionalRangeIndex.pdf | VLDB 2014 | DGFIndex for Smart Grid: Enhancing Hive with a Cost-Effective Multidimensional Range Index | [来源](https://vldb.org/pvldb/vol7/p1496-liu.pdf) |
| Apache Hive | VLDB2023-DHiveQueryExecutionPerformanceAnalysisviaDataflowinApacheHive.pdf | VLDB 2023 | DHive: Query Execution Performance Analysis via Dataflow in Apache Hive | [来源](https://www.vldb.org/pvldb/vol16/p3998-zhang.pdf) |
| Apache IoTDB | VLDB2020-ApacheIoTDBTimeseriesdatabaseforInternetofThings.pdf | VLDB 2020 | Apache IoTDB: Time-series database for Internet of Things | [来源](https://www.vldb.org/pvldb/vol13/p2901-wang.pdf) |
| Apache IoTDB | VLDB2023-FrequencyDomainDataEncodinginApacheIoTDB.pdf | VLDB 2023 | Frequency Domain Data Encoding in Apache IoTDB | [来源](https://www.vldb.org/pvldb/vol16/p282-song.pdf) |
| Apache IoTDB | VLDB2023-TsQualityMeasuringTimeSeriesDataQualityinApacheIoTDB.pdf | VLDB 2023 | TsQuality: Measuring Time Series Data Quality in Apache IoTDB | [来源](https://www.vldb.org/pvldb/vol16/p3982-song.pdf) |
| Apache IoTDB | VLDB2024-DistancebasedOutlierQueryOptimizationinApacheIoTDB.pdf | VLDB 2024 | Distance-based Outlier Query Optimization in Apache IoTDB | [来源](https://www.vldb.org/pvldb/vol17/p2778-song.pdf) |
| Apache IoTDB | VLDB2024-OnReducingSpaceAmplificationwithMultiColumnCompactioninApacheIoTDB.pdf | VLDB 2024 | On Reducing Space Amplification with Multi-Column Compaction in Apache IoTDB | [来源](https://www.vldb.org/pvldb/vol17/p2974-song.pdf) |
| Apache IoTDB | VLDB2025-MigrationFreeElasticStorageofTimeSeriesinApacheIoTDB.pdf | VLDB 2025 | Migration-Free Elastic Storage of Time Series in Apache IoTDB | [来源](https://www.vldb.org/pvldb/vol18/p1784-song.pdf) |
| Apache Spark | VLDB2019-SparkCruiseHandsfreeComputationReuseinSpark.pdf | VLDB 2019 | SparkCruise: Handsfree Computation Reuse in Spark | [来源](https://vldb.org/pvldb/vol12/p1850-roy.pdf) |
| Apache Spark | VLDB2020-DynamicSpeculativeOptimizationsforSQLCompilationinApacheSpark.pdf | VLDB 2020 | Dynamic Speculative Optimizations for SQL Compilation in Apache Spark | [来源](https://vldb.org/pvldb/vol13/p754-schiavio.pdf) |
| Apache Spark | VLDB2021-AutoExecutorPredictiveParallelismforSparkSQLQueries.pdf | VLDB 2021 | AutoExecutor: Predictive Parallelism for Spark SQL Queries | [来源](https://www.vldb.org/pvldb/vol14/p2855-sen.pdf) |
| Apache Spark | VLDB2021-DebuggingMissingAnswersforSparkQueriesoverNestedDatawithBreadcrumb.pdf | VLDB 2021 | Debugging Missing Answers for Spark Queries over Nested Data with Breadcrumb | [来源](https://www.vldb.org/pvldb/vol14/p2731-diestelkamper.pdf) |
| Apache Spark | VLDB2021-SparkCruiseWorkloadOptimizationinManagedSparkClustersatMicrosoft.pdf | VLDB 2021 | SparkCruise: Workload Optimization in Managed Spark Clusters at Microsoft | [来源](https://www.vldb.org/pvldb/vol14/p3122-roy.pdf) |
| Apache Spark | VLDB2023-TowardsGeneralandEfficientOnlineTuningforSpark.pdf | VLDB 2023 | Towards General and Efficient Online Tuning for Spark | [来源](https://www.vldb.org/pvldb/vol16/p3570-li.pdf) |
| Apache ZooKeeper | USENIX-Huntpdf.pdf | — | Huntpdf | [来源]() |
| Calvin | FAST-CalvinFastDistributedTransactionsforPartitionedDatabaseSystems.pdf | — | CalvinFastDistributedTransactionsforPartitionedDatabaseSystems | [来源]() |
| ClickHouse | VLDB2024-ClickHouseLightningFastAnalyticsforEveryone.pdf | VLDB 2024 | ClickHouse - Lightning Fast Analytics for Everyone | [来源](https://www.vldb.org/pvldb/vol17/p3731-schulze.pdf) |
| CloudKit | VLDB2018-CloudKitStructuredStorageforMobileApplications.pdf | VLDB 2018 | CloudKit: Structured Storage for Mobile Applications | [来源](https://vldb.org/pvldb/vol11/p540-shraer.pdf) |
| CockroachDB | 2019-TheDefinitiveGuidetoCockroachDB.pdf | — | TheDefinitiveGuidetoCockroachDB | [来源]() |
| CockroachDB | SIGMOD2020-CockroachDBTheResilientGeoDistributedSQLDatabase.pdf | — | CockroachDBTheResilientGeoDistributedSQLDatabase | [来源]() |
| CockroachDB | VLDB2022-ADemonstrationofMultiRegionCockroachDB.pdf | VLDB 2022 | A Demonstration of Multi-Region CockroachDB | [来源](https://www.vldb.org/pvldb/vol15/p3610-taft.pdf) |
| Coherence | VLDB2025-CacheCoherenceOverDisaggregatedMemory.pdf | VLDB 2025 | Cache Coherence Over Disaggregated Memory | [来源](https://www.vldb.org/pvldb/vol18/p2978-wang.pdf) |
| Coherence | VLDB2025-OpenMELUnsupervisedMultimodalEntityLinkingUsingNoiseFreeExpandedQueriesandGlobalCoherence.pdf | VLDB 2025 | OpenMEL: Unsupervised Multimodal Entity Linking Using Noise-Free Expanded Queries and Global Coherence | [来源](https://www.vldb.org/pvldb/vol18/p2454-zhu.pdf) |
| Couchbase | VLDB2019-CouchbaseAnalyticsNoETLforScalableNoSQLDataAnalysis.pdf | VLDB 2019 | Couchbase Analytics: NoETL for Scalable NoSQL Data Analysis | [来源](https://vldb.org/pvldb/vol12/p2275-hubail.pdf) |
| Couchbase | VLDB2022-MagmaAhighdatadensitystorageengineusedinCouchbase.pdf | VLDB 2022 | Magma: A high data density storage engine used in Couchbase | [来源](https://www.vldb.org/pvldb/vol15/p3496-lakshman.pdf) |
| Databricks | VLDB2026-AutoLiquidAutonomicDataLayoutOptimizationfortheDatabricksLakehouse.pdf | VLDB 2026 | AutoLiquid: Autonomic Data Layout Optimization for the Databricks Lakehouse | [来源](https://www.vldb.org/pvldb/vol19/p4023-liang.pdf) |
| Databricks | VLDB2026-UltronHistoryBasedQueryOptimizationatDatabricks.pdf | VLDB 2026 | Ultron: History-Based Query Optimization at Databricks | [来源](https://www.vldb.org/pvldb/vol19/p4358-marcus.pdf) |
| Datastax Enterprise | VLDB2014-EnterpriseSearchintheBigDataEraRecentDevelopmentsandOpenChallenges.pdf | VLDB 2014 | Enterprise Search in the Big Data Era: Recent Developments and Open Challenges | [来源](https://vldb.org/pvldb/vol7/p1717-li.pdf) |
| Datastax Enterprise | VLDB2014-TheImpactofColumnarInMemoryDatabasesonEnterpriseSystems.pdf | VLDB 2014 | The Impact of Columnar In-Memory Databases on Enterprise Systems | [来源](https://vldb.org/pvldb/vol7/p1722-plattner.pdf) |
| Datastax Enterprise | VLDB2019-AQuerySystemforEfficientlyInvestigatingComplexAttackBehaviorsforEnterpriseSecurity.pdf | VLDB 2019 | A Query System for Efficiently Investigating Complex Attack Behaviors for Enterprise Security | [来源](https://vldb.org/pvldb/vol12/p1802-gao.pdf) |
| Datastax Enterprise | VLDB2021-TaniumRevealAFederatedSearchEngineforQueryingUnstructuredFileDataonLargeEnterpriseNetworks.pdf | VLDB 2021 | Tanium Reveal: A Federated Search Engine for Querying Unstructured File Data on Large Enterprise Networks | [来源](https://www.vldb.org/pvldb/vol14/p3096-stoddard.pdf) |
| Datastax Enterprise | VLDB2024-AutomatingtheEnterprisewithFoundationModels.pdf | VLDB 2024 | Automating the Enterprise with Foundation Models | [来源](https://www.vldb.org/pvldb/vol17/p2805-wornow.pdf) |
| Datastax Enterprise | VLDB2024-KGFabricAScalableKnowledgeGraphWarehouseforEnterpriseDataInterconnection.pdf | VLDB 2024 | KGFabric: A Scalable Knowledge Graph Warehouse for Enterprise Data Interconnection | [来源](https://www.vldb.org/pvldb/vol17/p3841-yi.pdf) |
| Dgraph | ICDE2019-DgraphALargeScaleGraphDatabase.pdf | — | DgraphALargeScaleGraphDatabase | [来源]() |
| Dgraph | SIGMOD2017-DGraphADistributedGraphDatabase.pdf | — | DGraphADistributedGraphDatabase | [来源]() |
| Dgraph | TechnicalReport2020-DgraphSynchronouslyReplicatedTransactionalandDistributedGraph.pdf | — | DgraphSynchronouslyReplicatedTransactionalandDistributedGraph | [来源]() |
| DuckDB | Paper-CIDR2020raasveldtmuehleisenduckdbpdf.pdf | — | CIDR2020raasveldtmuehleisenduckdbpdf | [来源]() |
| DuckDB | Paper-DuckDBanEmbeddableAnalyticalDatabase.pdf | — | DuckDBanEmbeddableAnalyticalDatabase | [来源]() |
| DuckDB | Paper2023-DuckDBFOSDEM.pdf | — | DuckDBFOSDEM | [来源]() |
| DuckDB | VLDB2022-DuckDBWasmFastAnalyticalProcessingfortheWeb.pdf | VLDB 2022 | DuckDB-Wasm: Fast Analytical Processing for the Web | [来源](https://www.vldb.org/pvldb/vol15/p3574-kohn.pdf) |
| DuckDB | VLDB2023-DuckPGQBringingSQLPGQtoDuckDB.pdf | VLDB 2023 | DuckPGQ: Bringing SQL/PGQ to DuckDB | [来源](https://www.vldb.org/pvldb/vol16/p4034-wolde.pdf) |
| DuckDB | VLDB2025-BeyondQuackingDeepIntegrationofLanguageModelsandRAGintoDuckDB.pdf | VLDB 2025 | Beyond Quacking: Deep Integration of Language Models and RAG into DuckDB | [来源](https://www.vldb.org/pvldb/vol18/p5415-mhedhbi.pdf) |
| Fauna | VLDB2021-FaunaTemporalGraphDatabase.pdf | — | FaunaTemporalGraphDatabase | [来源]() |
| Firebase Realtime Database | VLDB2011-AnalyticsfortheRealTimeWeb.pdf | VLDB 2011 | Analytics for the RealTime Web | [来源](https://vldb.org/pvldb/vol4/p1391-grinev.pdf) |
| Firebase Realtime Database | VLDB2013-RealtimeAnalysisofInformationDiffusioninSocialMedia.pdf | VLDB 2013 | Realtime Analysis of Information Diffusion in Social Media | [来源](https://vldb.org/pvldb/vol6/p1416-taxidou.pdf) |
| Firebase Realtime Database | VLDB2020-RealtimeIndexFreeSingleSourceSimRankProcessingonWebScaleGraphs.pdf | VLDB 2020 | Realtime Index-Free Single Source SimRank Processing on Web-Scale Graphs | [来源](https://vldb.org/pvldb/vol13/p966-shi.pdf) |
| Firebase Realtime Database | VLDB2020-RealtimeTopkPersonalizedPageRankoverLargeGraphsonGPUs.pdf | VLDB 2020 | Realtime Top-k Personalized PageRank over Large Graphs on GPUs | [来源](https://vldb.org/pvldb/vol13/p15-shi.pdf) |
| Firebase Realtime Database | VLDB2022-MetasNextgenerationRealtimeMonitoringandAnalyticsPlatform.pdf | VLDB 2022 | Meta's Next-generation Realtime Monitoring and Analytics Platform | [来源](https://www.vldb.org/pvldb/vol15/p3522-mo.pdf) |
| FoundationDB | SIGMOD2021-FoundationDBADistributedUnbundledTransactionalKeyValueStore.pdf | — | FoundationDBADistributedUnbundledTransactionalKeyValueStore | [来源]() |
| Galaxybase | VLDB2024-GalaxybaseAHighPerformanceNativeDistributedGraphDatabaseforHTAP.pdf | VLDB 2024 | Galaxybase: A High Performance Native Distributed Graph Database for HTAP | [来源](https://www.vldb.org/pvldb/vol17/p3893-tong.pdf) |
| Google Cloud Datastore | VLDB2011-UsingPaxostoBuildaScalableConsistentandHighlyAvailableDatastore.pdf | VLDB 2011 | Using Paxos to Build a Scalable, Consistent, and Highly Available Datastore | [来源](https://vldb.org/pvldb/vol4/p243-rao.pdf) |
| Google Cloud Datastore | VLDB2024-TransparentMigrationfromDatastoretoFirestore.pdf | VLDB 2024 | Transparent Migration from Datastore to Firestore | [来源](https://www.vldb.org/pvldb/vol17/p3960-davisson.pdf) |
| Google Cloud Firestore | VLDB2026-TheLiveDatabaseFirestoresScalableandConsistentRealtimeQueries.pdf | VLDB 2026 | The Live Database: Firestore’s Scalable and Consistent Realtime Queries | [来源](https://www.vldb.org/pvldb/vol19/p4130-jacobsson.pdf) |
| Google F1 | VLDB2013-F1ADistributedSQLDatabaseThatScales.pdf | VLDB 2013 | F1: A Distributed SQL Database That Scales | [来源](https://vldb.org/pvldb/vol6/p1068-shute.pdf) |
| Google F1 | VLDB2018-F1QueryDeclarativeQueryingatScale.pdf | VLDB 2018 | F1 Query: Declarative Querying at Scale | [来源](https://vldb.org/pvldb/vol11/p1835-samwel.pdf) |
| Google Spanner | OSDI2012-SpannerGooglesGloballyDistributedDatabase.pdf | — | SpannerGooglesGloballyDistributedDatabase | [来源]() |
| GraphDB | Paper-lecture07pdf.pdf | — | lecture07pdf | [来源]() |
| Graphite | VLDB2020-GraphiteANUMAawareHPCSystemforGraphAnalyticsBasedonanewMPIXParallelismModel.pdf | VLDB 2020 | Graphite: A NUMA-aware HPC System for Graph Analytics Based on a new MPI * X Parallelism Model | [来源](https://vldb.org/pvldb/vol13/p783-mofrad.pdf) |
| Greenplum | Paper2017-CMUSCS15721Spring2017QueryCompilation.pdf | — | CMUSCS15721Spring2017QueryCompilation | [来源]() |
| Hazelcast | VLDB2021-HazelcastJetLowlatencyStreamProcessingatthe9999thPercentile.pdf | VLDB 2021 | Hazelcast Jet: Low-latency Stream Processing at the 99.99th Percentile | [来源](https://www.vldb.org/pvldb/vol14/p3110-katsifodimos.pdf) |
| IBM Db2 | VLDB2009-AnObjectPlacementAdvisorforDB2UsingSolidStateStorage.pdf | VLDB 2009 | An Object Placement Advisor for DB2 Using Solid State Storage | [来源](https://vldb.org/pvldb/vol2/vldb09-853.pdf) |
| IBM Db2 | VLDB2009-EfficientIndexCompressioninDB2LUW.pdf | VLDB 2009 | Efficient Index Compression in DB2 LUW | [来源](https://vldb.org/pvldb/vol2/vldb09-798.pdf) |
| IBM Db2 | VLDB2010-MEETDB2AutomatedDatabaseMigrationEvaluation.pdf | VLDB 2010 | MEET DB2: Automated Database Migration Evaluation | [来源](https://vldb.org/pvldb/vol3/I05.pdf) |
| IBM Db2 | VLDB2013-DB2withBLUAccelerationSoMuchMorethanJustaColumnStore.pdf | VLDB 2013 | DB2 with BLU Acceleration: So Much More than Just a Column Store | [来源](https://vldb.org/pvldb/vol6/p1080-barber.pdf) |
| IBM Db2 | VLDB2019-SynergisticGraphandSQLAnalyticsInsideIBMDb2.pdf | VLDB 2019 | Synergistic Graph and SQL Analytics Inside IBM Db2 | [来源](https://vldb.org/pvldb/vol12/p1782-tian.pdf) |
| IBM Db2 | VLDB2020-Db2EventStoreAPurposeBuiltIoTDatabaseEngine.pdf | VLDB 2020 | Db2 Event Store: A Purpose-Built IoT Database Engine | [来源](https://www.vldb.org/pvldb/vol13/p3299-garcia-arellano.pdf) |
| Infinity | VLDB2024-AlephFilterToInfinityinConstantTime.pdf | VLDB 2024 | Aleph Filter: To Infinity in Constant Time | [来源](https://www.vldb.org/pvldb/vol17/p3644-dayan.pdf) |
| Ingres | Paper2023-DS21ActianX_04Apdf.pdf | — | DS21ActianX_04Apdf | [来源]() |
| LinDB | VLDB-p1816tellerpdf.pdf | — | p1816tellerpdf | [来源]() |
| Memgraph | 2020-Memgraph.pdf | — | Memgraph | [来源]() |
| Memgraph | arXiv2021-MemgraphAHighPerformanceGraphDatabase.pdf | — | MemgraphAHighPerformanceGraphDatabase | [来源]() |
| Microsoft Access | VLDB2009-CorrelationMapsACompressedAccessMethodforExploitingSoftFunctionalDependencies.pdf | VLDB 2009 | Correlation Maps: A Compressed Access Method for Exploiting Soft Functional Dependencies | [来源](https://vldb.org/pvldb/vol2/vldb09-199.pdf) |
| Microsoft Access | VLDB2009-FullFidelityFlexibleObjectOrientedXMLAccess.pdf | VLDB 2009 | Full-Fidelity Flexible Object-Oriented XML Access | [来源](https://vldb.org/pvldb/vol2/vldb09-216.pdf) |
| Microsoft Access | VLDB2020-RDFFramesKnowledgeGraphAccessforMachineLearningTools.pdf | VLDB 2020 | RDFFrames: Knowledge Graph Access for Machine Learning Tools | [来源](https://www.vldb.org/pvldb/vol13/p2889-mohamed.pdf) |
| Microsoft Access | VLDB2020-SieveAMiddlewareApproachtoScalableAccessControlforDatabaseManagementSystems.pdf | VLDB 2020 | Sieve: A Middleware Approach to Scalable Access Control for Database Management Systems | [来源](https://www.vldb.org/pvldb/vol13/p2424-pappachan.pdf) |
| Microsoft Access | VLDB2021-ApproachingDRAMperformancebyusingmicrosecondlatencyflashmemoryforsmallsizedrandomreadaccessesanewaccessmethoda.pdf | VLDB 2021 | Approaching DRAM performance by using microsecond-latency flash memory for small-sized random read accesses: a new access method and its graph applications | [来源](https://www.vldb.org/pvldb/vol14/p1311-suzuki.pdf) |
| Microsoft Azure AI Search | VLDB2009-HAMSTERUsingSearchClicklogsforSchemaandTaxonomyMatching.pdf | VLDB 2009 | HAMSTER: Using Search Clicklogs for Schema and Taxonomy Matching | [来源](https://vldb.org/pvldb/vol2/vldb09-124.pdf) |
| Microsoft Azure AI Search | VLDB2009-SimilaritySearchonBregmanDivergenceTowardsNonMetricIndexing.pdf | VLDB 2009 | Similarity Search on Bregman Divergence: Towards Non-Metric Indexing | [来源](https://vldb.org/pvldb/vol2/vldb09-468.pdf) |
| Microsoft Azure AI Search | VLDB2026-HighlyScalableSQLAzureMVCCVersionCleaner.pdf | VLDB 2026 | Highly Scalable SQL Azure MVCC Version Cleaner | [来源](https://www.vldb.org/pvldb/vol19/p3916-gandikota.pdf) |
| Microsoft Azure Cosmos DB | VLDB2021-TheCosmosBigDataPlatformatMicrosoftOveraDecadeofProgressandaDecadetoLookForward.pdf | VLDB 2021 | The Cosmos Big Data Platform at Microsoft: Over a Decade of Progress and a Decade to Look Forward | [来源](https://www.vldb.org/pvldb/vol14/p3148-jindal.pdf) |
| Microsoft Azure Cosmos DB | VLDB2025-CostEffectiveLowLatencyVectorSearchwithAzureCosmosDB.pdf | VLDB 2025 | Cost-Effective, Low Latency Vector Search with Azure Cosmos DB | [来源](https://www.vldb.org/pvldb/vol18/p5166-upreti.pdf) |
| Microsoft Azure Data Explorer | VLDB2017-FlashViewAnInteractiveVisualExplorerforRawData.pdf | VLDB 2017 | FlashView: An Interactive Visual Explorer for Raw Data | [来源](https://vldb.org/pvldb/vol10/p1869-pang.pdf) |
| Microsoft Azure Data Explorer | VLDB2018-MustaCHEAMultipleClusteringHierarchiesExplorer.pdf | VLDB 2018 | MustaCHE: A Multiple Clustering Hierarchies Explorer | [来源](https://vldb.org/pvldb/vol11/p2058-neto.pdf) |
| Microsoft Azure Data Explorer | VLDB2018-X2QYourPersonalExamplebasedGraphExplorer.pdf | VLDB 2018 | X2Q: Your Personal Example-based Graph Explorer | [来源](https://vldb.org/pvldb/vol11/p2026-lissandrini.pdf) |
| Microsoft Azure Data Explorer | VLDB2020-HDAGExplorerASystemforHierarchicalDAGSummarizationandExploration.pdf | VLDB 2020 | HDAG-Explorer: A System for Hierarchical DAG Summarization and Exploration | [来源](https://www.vldb.org/pvldb/vol13/p2973-zhu.pdf) |
| Microsoft Azure Data Explorer | VLDB2021-KDVExplorerANearRealTimeKernelDensityVisualizationSystemforSpatialAnalysis.pdf | VLDB 2021 | KDV-Explorer: A Near Real-Time Kernel Density Visualization System for Spatial Analysis | [来源](https://www.vldb.org/pvldb/vol14/p2655-chan.pdf) |
| Microsoft Azure Data Explorer | VLDB2023-CMExplorerDissectingDataIngestionProblems.pdf | VLDB 2023 | CM-Explorer: Dissecting Data Ingestion Problems | [来源](https://www.vldb.org/pvldb/vol16/p3958-bylois.pdf) |
| Microsoft Azure SQL Database | VLDB2009-DBToasterASQLCompilerforHighPerformanceDeltaProcessinginMainMemoryDatabases.pdf | VLDB 2009 | DBToaster: A SQL Compiler for High-Performance Delta Processing in Main-Memory Databases | [来源](https://vldb.org/pvldb/vol2/vldb09-1042.pdf) |
| Microsoft Azure SQL Database | VLDB2009-LaconicSchemaMappingsComputingtheCorewithSQLQueries.pdf | VLDB 2009 | Laconic Schema Mappings: Computing the Core with SQL Queries | [来源](https://vldb.org/pvldb/vol2/vldb09-595.pdf) |
| Microsoft Azure SQL Database | VLDB2009-SQLMapReduceApracticalapproachtoselfdescribingpolymorphicandparallelizableuserdefinedfunctions.pdf | VLDB 2009 | SQL/MapReduce: A practical approach to self-describing, polymorphic, and parallelizable user-defined functions | [来源](https://vldb.org/pvldb/vol2/vldb09-464.pdf) |
| Microsoft Azure SQL Database | VLDB2014-SQLAAExecutingSQLonanAsymmetricArchitecture.pdf | VLDB 2014 | SQL/AA: Executing SQL on an Asymmetric Architecture | [来源](https://vldb.org/pvldb/vol7/p1625-to.pdf) |
| Microsoft Azure SQL Database | VLDB2014-SQLonHadoopFullCircleBacktoSharedNothingDatabaseArchitectures.pdf | VLDB 2014 | SQL-on-Hadoop: Full Circle Back to Shared-Nothing Database Architectures | [来源](https://vldb.org/pvldb/vol7/p1295-floratou.pdf) |
| Microsoft Azure SQL Database | VLDB2019-ConstantTimeRecoveryinAzureSQLDatabase.pdf | VLDB 2019 | Constant Time Recovery in Azure SQL Database | [来源](https://vldb.org/pvldb/vol12/p2143-antonopoulos.pdf) |
| Microsoft Azure SQL Database | VLDB2022-MoneyballProactiveAutoScalinginMicrosoftAzureSQLDatabaseServerless.pdf | VLDB 2022 | Moneyball: Proactive Auto-Scaling in Microsoft Azure SQL Database Serverless | [来源](https://www.vldb.org/pvldb/vol15/p1279-poppe.pdf) |
| Microsoft Azure SQL Database | VLDB2025-MDMVCCMultiversionConcurrencyControlforSchemaChangesinAzureSQLDatabase.pdf | VLDB 2025 | MD-MVCC: Multi-version Concurrency Control for Schema Changes in Azure SQL Database | [来源](https://www.vldb.org/pvldb/vol18/p4791-antonopoulos.pdf) |
| Microsoft Azure Synapse Analytics | VLDB2014-DimmWittedAStudyofMainMemoryStatisticalAnalytics.pdf | VLDB 2014 | DimmWitted: A Study of Main-Memory Statistical Analytics | [来源](https://vldb.org/pvldb/vol7/p1283-zhang.pdf) |
| Microsoft Azure Synapse Analytics | VLDB2014-ErrorboundedSamplingforAnalyticsonBigSparseData.pdf | VLDB 2014 | Error-bounded Sampling for Analytics on Big Sparse Data | [来源](https://vldb.org/pvldb/vol7/p1508-yan.pdf) |
| Microsoft Azure Synapse Analytics | VLDB2014-LargeScaleGraphAnalyticsinAster6BringingContexttoBigDataDiscovery.pdf | VLDB 2014 | Large-Scale Graph Analytics in Aster 6: Bringing Context to Big Data Discovery | [来源](https://vldb.org/pvldb/vol7/p1405-simmen.pdf) |
| Microsoft Azure Synapse Analytics | VLDB2014-VERTEXICAYourRelationalFriendforGraphAnalytics.pdf | VLDB 2014 | VERTEXICA: Your Relational Friend for Graph Analytics! | [来源](https://vldb.org/pvldb/vol7/p1669-jindal.pdf) |
| Microsoft Azure Synapse Analytics | VLDB2020-POLARISTheDistributedSQLEngineinAzureSynapse.pdf | VLDB 2020 | POLARIS: The Distributed SQL Engine in Azure Synapse | [来源](https://www.vldb.org/pvldb/vol13/p3204-saborit.pdf) |
| Microsoft Azure Synapse Analytics | VLDB2021-HyperspaceTheIndexingSubsystemofAzureSynapse.pdf | VLDB 2021 | Hyperspace: The Indexing Subsystem of Azure Synapse | [来源](https://www.vldb.org/pvldb/vol14/p3043-potharaju.pdf) |
| Microsoft Azure Table Storage | VLDB2009-AnsweringTableAugmentationQueriesfromUnstructuredListsontheWeb.pdf | VLDB 2009 | Answering Table Augmentation Queries from Unstructured Lists on the Web | [来源](https://vldb.org/pvldb/vol2/vldb09-652.pdf) |
| Microsoft Azure Table Storage | VLDB2018-TableUnionSearchonOpenData.pdf | VLDB 2018 | Table Union Search on Open Data | [来源](https://vldb.org/pvldb/vol11/p813-nargesian.pdf) |
| Microsoft Azure Table Storage | VLDB2020-TableExtractionandUnderstandingforScientificandEnterpriseApplications.pdf | VLDB 2020 | Table Extraction and Understanding for Scientific and Enterprise Applications | [来源](https://www.vldb.org/pvldb/vol13/p3433-burdick.pdf) |
| Microsoft Azure Table Storage | VLDB2024-LakeCompassAnEndtoEndSystemforTableMaintenanceSearchandAnalysisinDataLakes.pdf | VLDB 2024 | LakeCompass: An End-to-End System for Table Maintenance, Search and Analysis in Data Lakes | [来源](https://www.vldb.org/pvldb/vol17/p4381-chai.pdf) |
| Microsoft Azure Table Storage | VLDB2025-BIRDIENaturalLanguageDrivenTableDiscoveryUsingDifferentiableSearchIndex.pdf | VLDB 2025 | BIRDIE: Natural Language-Driven Table Discovery Using Differentiable Search Index | [来源](https://www.vldb.org/pvldb/vol18/p2070-gao.pdf) |
| Microsoft Azure Table Storage | VLDB2026-FedAugmentTableAugmentationSearchoverDecentralizedDataRepositories.pdf | VLDB 2026 | FedAugment: Table Augmentation Search over Decentralized Data Repositories | [来源](https://www.vldb.org/pvldb/vol19/p2672-behme.pdf) |
| Microsoft Azure Table Storage | VLDB2026-GASALightweightFrameworkforFilteredSearchoverWidetableVectors.pdf | VLDB 2026 | GAS: A Lightweight Framework for Filtered Search over Wide-table Vectors | [来源](https://www.vldb.org/pvldb/vol19/p3133-tong.pdf) |
| Microsoft Fabric | VLDB2020-ResilientDBGlobalScaleResilientBlockchainFabric.pdf | VLDB 2020 | ResilientDB: Global Scale Resilient Blockchain Fabric | [来源](https://vldb.org/pvldb/vol13/p868-gupta.pdf) |
| Microsoft Fabric | VLDB2020-ScalableResilientandConfigurablePermissionedBlockchainFabric.pdf | VLDB 2020 | Scalable, Resilient and Configurable Permissioned Blockchain Fabric | [来源](https://www.vldb.org/pvldb/vol13/p2893-rahnama.pdf) |
| Microsoft Fabric | VLDB2026-HermesatScalePoweringDistributedQuerieswithaUnifiedMemoryFabric.pdf | VLDB 2026 | Hermes at Scale: Powering Distributed Queries with a Unified Memory Fabric | [来源](https://www.vldb.org/pvldb/vol19/p3969-gubner.pdf) |
| Microsoft SQL Server | VLDB2014-FastForeignKeyDetectioninMicrosoftSQLServerPowerPivotforExcel.pdf | VLDB 2014 | Fast Foreign-Key Detection in Microsoft SQL Server PowerPivot for Excel | [来源](https://vldb.org/pvldb/vol7/p1417-chen.pdf) |
| MonetDB | Paper-Columnimprintsasecondaryindexstructure.pdf | — | Columnimprintsasecondaryindexstructure | [来源]() |
| MonetDB | Paper-P19pdf.pdf | — | P19pdf | [来源]() |
| MonetDB | VLDB-MemoryEfficientHashJoins.pdf | VLDB 2015 | Memory-Efficient Hash Joins | [来源](https://vldb.org/pvldb/vol8/p353-barber.pdf) |
| MonetDB | VLDB2012-MonetDBDataCellOnlineAnalyticsinaStreamingColumnStore.pdf | VLDB 2012 | MonetDB/DataCell: Online Analytics in a Streaming Column-Store | [来源](https://vldb.org/pvldb/vol5/p1910_eriettaliarou_vldb2012.pdf) |
| MongoDB | ACMQueue2017-MongoDBJavaScriptFuzzer.pdf | — | MongoDBJavaScriptFuzzer | [来源]() |
| MongoDB | CACM2017-MongoDBJavaScriptFuzzer.pdf | — | MongoDBJavaScriptFuzzer | [来源]() |
| MongoDB | ICDE2020-DecidingWhentoTradeDataFreshnessforPerformanceinMongoDBasaService.pdf | — | DecidingWhentoTradeDataFreshnessforPerformanceinMongoDBasaService | [来源]() |
| MongoDB | MasterThesis2017-JohannesBaumSerializabilityCheckingforMongoDBClients.pdf | — | JohannesBaumSerializabilityCheckingforMongoDBClients | [来源]() |
| MongoDB | MasterThesis2019-QuantitativePerformanceEvaluationofCloudBasedMySQLRelationalVsMongoDBNoSQLDatabasewithYCSB.pdf | — | QuantitativePerformanceEvaluationofCloudBasedMySQLRelationalVsMongoDBNoSQLDatabasewithYCSB | [来源]() |
| MongoDB | NSDI2021-FaultTolerantReplicationwithPullBasedConsensusinMongoDB.pdf | — | FaultTolerantReplicationwithPullBasedConsensusinMongoDB | [来源]() |
| MongoDB | SIGMOD2019-TyulenevImplementationofClusterwideLogicalClockandCausalConsistencyinMongoDB.pdf | — | TyulenevImplementationofClusterwideLogicalClockandCausalConsistencyinMongoDB | [来源]() |
| MongoDB | StrangeloopTLA2019-ABugLifeFixingaMongoDBReplicationProtocolBugwithTLAplus.pdf | — | ABugLifeFixingaMongoDBReplicationProtocolBugwithTLAplus | [来源]() |
| MongoDB | VLDB2019-AdaptingTPCCBenchmarktoMeasurePerformanceofMultiDocumentTransactionsinMongoDB.pdf | VLDB 2019 | Adapting TPC-C Benchmark to Measure Performance of Multi-Document Transactions in MongoDB | [来源](https://vldb.org/pvldb/vol12/p2254-kamsky.pdf) |
| MongoDB | VLDB2019-SchultzTunableConsistencyinMongoDB.pdf | — | SchultzTunableConsistencyinMongoDB | [来源]() |
| MongoDB | VLDB2020-eXtremeModellinginPractice.pdf | VLDB 2020 | eXtreme Modelling in Practice | [来源](https://vldb.org/pvldb/vol13/p1346-schvimer.pdf) |
| MongoDB | VLDB2025-DesignandModularVerificationofDistributedTransactionsinMongoDB.pdf | VLDB 2025 | Design and Modular Verification of Distributed Transactions in MongoDB | [来源](https://www.vldb.org/pvldb/vol18/p5045-schultz.pdf) |
| MongoDB | arXiv2016-160309291ExpressivityandComplexityofMongoDBExtendedVersion.pdf | — | 160309291ExpressivityandComplexityofMongoDBExtendedVersion | [来源]() |
| MongoDB | arXiv2020-200408425AutomatedSystemPerformanceTestingatMongoDB.pdf | — | 200408425AutomatedSystemPerformanceTestingatMongoDB | [来源]() |
| MongoDB | arXiv2021-210211960DesignandVerificationofaLoglessDynamicReconfigurationProtocolinMongoDBReplication.pdf | — | 210211960DesignandVerificationofaLoglessDynamicReconfigurationProtocolinMongoDBReplication | [来源]() |
| MySQL | Paper-p5sompolskipdf.pdf | — | p5sompolskipdf | [来源]() |
| MySQL | VLDB2014-RealizationoftheLowCostandHighPerformanceMySQLCloudDatabase.pdf | VLDB 2014 | Realization of the Low Cost and High Performance MySQL Cloud Database | [来源](https://vldb.org/pvldb/vol7/p1742-alibaba.pdf) |
| MySQL | VLDB2025-FreelyMovingBetweentheOLTPandOLAPWorldsHermesanHighPerformanceOLAPAcceleratorforMySQL.pdf | VLDB 2025 | Freely Moving Between the OLTP and OLAP Worlds: Hermes – an High-Performance OLAP Accelerator for MySQL | [来源](https://www.vldb.org/pvldb/vol18/p5113-gubner.pdf) |
| Nebula Graph | VLDB2009-Classbasedgraphanonymizationforsocialnetworkdata.pdf | VLDB 2009 | Class-based graph anonymization for social network data | [来源](https://vldb.org/pvldb/vol2/vldb09-pvldb26.pdf) |
| Nebula Graph | VLDB2009-ComparingStarsOnApproximatingGraphEditDistance.pdf | VLDB 2009 | Comparing Stars: On Approximating Graph Edit Distance | [来源](https://vldb.org/pvldb/vol2/vldb09-568.pdf) |
| Nebula Graph | VLDB2009-DistanceJoinPatternMatchQueryInaLargeGraphDatabase.pdf | VLDB 2009 | DistanceJoin: Pattern Match Query In a Large Graph Database | [来源](https://vldb.org/pvldb/vol2/vldb09-876.pdf) |
| Nebula Graph | VLDB2009-GraphClusteringBasedonStructuralAttributeSimilarities.pdf | VLDB 2009 | Graph Clustering Based on Structural/Attribute Similarities | [来源](https://vldb.org/pvldb/vol2/vldb09-175.pdf) |
| Nebula Graph | VLDB2009-MiningGraphPatternsEfficientlyviaRandomizedSummaries.pdf | VLDB 2009 | Mining Graph Patterns Efficiently via Randomized Summaries | [来源](https://vldb.org/pvldb/vol2/vldb09-80.pdf) |
| Nebula Graph | VLDB2009-OutputSpaceSamplingforGraphPatterns.pdf | VLDB 2009 | Output Space Sampling for Graph Patterns | [来源](https://vldb.org/pvldb/vol2/vldb09-713.pdf) |
| Neo4j | TechnicalReport2016-SnapshotIsolationforNeo4j.pdf | — | SnapshotIsolationforNeo4j | [来源]() |
| Neo4j | VLDB2026-Provlepsis4jQueryingFutureGraphsinNeo4j.pdf | VLDB 2026 | Provlepsis4j: Querying Future Graphs in Neo4j | [来源](https://www.vldb.org/pvldb/vol19/p4770-gkartzios.pdf) |
| OceanBase | VLDB2022-OceanBaseA707MilliontpmCDistributedRelationalDatabaseSystem.pdf | VLDB 2022 | OceanBase: A 707 Million tpmC Distributed Relational Database System | [来源](https://www.vldb.org/pvldb/vol15/p3385-xu.pdf) |
| OceanBase | VLDB2023-OceanBasePaeticaAHybridSharednothingSharedeverythingDatabaseforSupportingSingleMachineandDistributedCluster.pdf | VLDB 2023 | OceanBase Paetica: A Hybrid Shared-nothing/Shared-everything Database for Supporting Single Machine and Distributed Cluster | [来源](https://www.vldb.org/pvldb/vol16/p3728-xu.pdf) |
| OceanBase | VLDB2026-ATreeStructuredTwoPhaseCommitFrameworkforOceanBaseOptimizingScalabilityandConsistency.pdf | VLDB 2026 | A Tree-Structured Two-Phase Commit Framework for OceanBase: Optimizing Scalability and Consistency | [来源](https://www.vldb.org/pvldb/vol19/p4250-xu.pdf) |
| OceanBase | VLDB2026-OceanBaseBacchusaHighPerformanceandScalableCloudNativeSharedStorageArchitectureforMultiCloud.pdf | VLDB 2026 | OceanBase Bacchus: a High-Performance and Scalable Cloud-Native Shared Storage Architecture for Multi-Cloud | [来源](https://www.vldb.org/pvldb/vol19/p4089-xu.pdf) |
| openGauss / GaussDB | VLDB2021-DBMindASelfDrivingPlatforminopenGauss.pdf | VLDB 2021 | DBMind: A Self-Driving Platform in openGauss | [来源](https://www.vldb.org/pvldb/vol14/p2743-zhou.pdf) |
| openGauss / GaussDB | VLDB2021-FullEncryptionAnendtoendencryptionmechanisminGaussDB.pdf | VLDB 2021 | Full Encryption: An end to end encryption mechanism in GaussDB | [来源](https://www.vldb.org/pvldb/vol14/p2811-guo.pdf) |
| openGauss / GaussDB | VLDB2021-openGaussAnAutonomousDatabaseSystem.pdf | VLDB 2021 | openGauss: An Autonomous Database System | [来源](https://www.vldb.org/pvldb/vol14/p3028-li.pdf) |
| openGauss / GaussDB | VLDB2024-GaussDBACloudNativeMultiPrimaryDatabasewithComputeMemoryStorageDisaggregation.pdf | VLDB 2024 | GaussDB: A Cloud-Native Multi-Primary Database with Compute-Memory-Storage Disaggregation | [来源](https://www.vldb.org/pvldb/vol17/p3786-li.pdf) |
| openGauss / GaussDB | VLDB2025-GRewriterPracticalQueryRewritingwithAutomaticRuleSetExpansioninGaussDB.pdf | VLDB 2025 | GRewriter: Practical Query Rewriting with Automatic Rule Set Expansion in GaussDB | [来源](https://www.vldb.org/pvldb/vol18/p4991-jiang.pdf) |
| openGauss / GaussDB | VLDB2026-NoSilverBulletBoostingGaussDBPerformanceonthe30TBTPCHWorkload.pdf | VLDB 2026 | No Silver Bullet: Boosting GaussDB Performance on the 30TB TPC-H Workload | [来源](https://www.vldb.org/pvldb/vol19/p4036-zeyl.pdf) |
| Oracle | VLDB2009-HybridColumnarCompressioninOracleDatabase11g.pdf | — | HybridColumnarCompressioninOracleDatabase11g | [来源]() |
| Oracle NoSQL | VLDB2014-RankJoinQueriesinNoSQLDatabases.pdf | VLDB 2014 | Rank Join Queries in NoSQL Databases | [来源](https://vldb.org/pvldb/vol7/p493-ntarmos.pdf) |
| Oracle NoSQL | VLDB2019-BlockasaValueforSQLoverNoSQL.pdf | VLDB 2019 | Block as a Value for SQL over NoSQL | [来源](https://vldb.org/pvldb/vol12/p1153-cao.pdf) |
| Oracle NoSQL | VLDB2020-NativeJSONDatatypeSupportMaturingSQLandNoSQLconvergenceinOracleDatabase.pdf | VLDB 2020 | Native JSON Datatype Support: Maturing SQL and NoSQL convergence in Oracle Database | [来源](https://www.vldb.org/pvldb/vol13/p3059-liu.pdf) |
| Oracle NoSQL | VLDB2021-ADemonstrationofNoDAUnifiedAccesstoNoSQLStores.pdf | VLDB 2021 | A Demonstration of NoDA: Unified Access to NoSQL Stores | [来源](https://www.vldb.org/pvldb/vol14/p2851-koutroumanis.pdf) |
| Oracle NoSQL | VLDB2024-XStorACloudnativeNoSQLDatabaseServicewithMultimodelSupport.pdf | VLDB 2024 | X-Stor: A Cloud-native NoSQL Database Service with Multi-model Support | [来源](https://www.vldb.org/pvldb/vol17/p4025-lei.pdf) |
| Oracle NoSQL | VLDB2026-AResourcecentricAnalysisandOptimizationofNoSQLWorkloadsusingDistressedResourceVolumeMetric.pdf | VLDB 2026 | A Resource-centric Analysis and Optimization of NoSQL Workloads using Distressed Resource Volume Metric | [来源](https://www.vldb.org/pvldb/vol19/p1867-simmhan.pdf) |
| Oracle NoSQL | VLDB2026-QueryCraftANaturalLanguageDrivenNoSQLDatabaseQueryingSystemPoweredbyLargeLanguageModels.pdf | VLDB 2026 | QueryCraft: A Natural Language-Driven NoSQL Database Querying System Powered by Large Language Models | [来源](https://www.vldb.org/pvldb/vol19/p4754-song.pdf) |
| Percona Server for MySQL | VLDB2009-AScalablePredictableJoinOperatorforHighlyConcurrentDataWarehouses.pdf | VLDB 2009 | A Scalable, Predictable Join Operator for Highly Concurrent Data Warehouses | [来源](https://vldb.org/pvldb/vol2/vldb09-553.pdf) |
| Percona Server for MySQL | VLDB2009-AWaveletTransformforEfficientConsolidationofSensorRelationswithQualityGuarantees.pdf | VLDB 2009 | A Wavelet Transform for Efficient Consolidation of Sensor Relations with Quality Guarantees | [来源](https://vldb.org/pvldb/vol2/vldb09-612.pdf) |
| Percona Server for MySQL | VLDB2009-SchemaBasedIndependenceAnalysisforXMLUpdates.pdf | VLDB 2009 | Schema-Based Independence Analysis for XML Updates | [来源](https://vldb.org/pvldb/vol2/vldb09-684.pdf) |
| Percona Server for MySQL | VLDB2009-StreamsonWiresAQueryCompilerforFPGAs.pdf | VLDB 2009 | Streams on Wires - A Query Compiler for FPGAs | [来源](https://vldb.org/pvldb/vol2/vldb09-622.pdf) |
| Percona Server for MySQL | VLDB2009-TaggingStreamDataforRichRealTimeServices.pdf | VLDB 2009 | Tagging Stream Data for Rich Real-Time Services | [来源](https://vldb.org/pvldb/vol2/vldb09-24.pdf) |
| Percona Server for MySQL | VLDB2009-ThreadCooperationinMulticoreArchitecturesforFrequencyCountingoverMultipleDataStreams.pdf | VLDB 2009 | Thread Cooperation in Multicore Architectures for Frequency Counting over Multiple Data Streams | [来源](https://vldb.org/pvldb/vol2/vldb09-401.pdf) |
| PostgreSQL | PPT2020-ExtendingPostgreSQLtoGoogleSpannerArchitecture.pdf | — | ExtendingPostgreSQLtoGoogleSpannerArchitecture | [来源]() |
| PostgreSQL | VLDB2012-SerializableSnapshotIsolationinPostgreSQL.pdf | VLDB 2012 | Serializable Snapshot Isolation in PostgreSQL | [来源](https://vldb.org/pvldb/vol5/p1850_danrkports_vldb2012.pdf) |
| PostgreSQL | VLDB2013-PAQOAPreferenceAwareQueryOptimizerforPostgreSQL.pdf | VLDB 2013 | PAQO: A Preference-Aware Query Optimizer for PostgreSQL | [来源](https://vldb.org/pvldb/vol6/p1334-farnan.pdf) |
| PostgreSQL | VLDB2016-PrecisionPerformanceSurgeryforPostgreSQLLLVMbasedExpressionCompilationJustinTime.pdf | VLDB 2016 | Precision Performance Surgery for PostgreSQL: LLVM-based Expression Compilation, Just in Time | [来源](https://vldb.org/pvldb/vol9/p1517-butterstein.pdf) |
| PostgreSQL | VLDB2018-ProvSQLProvenanceandProbabilityManagementinPostgreSQL.pdf | VLDB 2018 | ProvSQL:Provenance and Probability Management in PostgreSQL | [来源](https://vldb.org/pvldb/vol11/p2034-senellart.pdf) |
| PostgreSQL | VLDB2021-PostCENNPostgreSQLwithMachineLearningModelsforCardinalityEstimation.pdf | VLDB 2021 | PostCENN: PostgreSQL with Machine Learning Models for Cardinality Estimation | [来源](https://www.vldb.org/pvldb/vol14/p2715-woltmann.pdf) |
| PostgreSQL | VLDB2023-DeepVQLDeepVideoQueriesonPostgreSQL.pdf | VLDB 2023 | DeepVQL: Deep Video Queries on PostgreSQL | [来源](https://www.vldb.org/pvldb/vol16/p3910-nam.pdf) |
| PostgreSQL | VLDB2026-LakebaseServerlessPostgresoverOpenLakeStorage.pdf | VLDB 2026 | Lakebase: Serverless Postgres over Open Lake Storage | [来源](https://www.vldb.org/pvldb/vol19/p4385-pandis.pdf) |
| PostgreSQL | VLDB2026-TuningtheLookaheadDistanceforPostgreSQLAsynchronousIO.pdf | VLDB 2026 | Tuning the Lookahead Distance for PostgreSQL Asynchronous IO | [来源](https://www.vldb.org/pvldb/vol19/p3982-wu.pdf) |
| Presto | VLDB2024-PrestosHistorybasedQueryOptimizer.pdf | VLDB 2024 | Presto’s History-based Query Optimizer | [来源](https://www.vldb.org/pvldb/vol17/p4077-shankhdhar.pdf) |
| Presto | VLDB2026-FromPrestotoPrestissimoAVeloxPoweredModernizationJourney.pdf | VLDB 2026 | From Presto to Prestissimo: A Velox-Powered Modernization Journey | [来源](https://www.vldb.org/pvldb/vol19/p4399-dutta.pdf) |
| Presto | VLDB2026-SQLNativeVectorSearchatBillionScaleinPresto.pdf | VLDB 2026 | SQL-Native Vector Search at Billion Scale in Presto | [来源](https://www.vldb.org/pvldb/vol19/p4182-xu.pdf) |
| Redis | arXiv2024-RedisAHighPerformanceInMemoryDatabase.pdf | — | RedisAHighPerformanceInMemoryDatabase | [来源]() |
| RocksDB | VLDB2025-AreJoinsoverLSMtreesReadyTakeRocksDBasanExample.pdf | VLDB 2025 | Are Joins over LSM-trees Ready: Take RocksDB as an Example | [来源](https://www.vldb.org/pvldb/vol18/p1077-luo.pdf) |
| RocksDB | VLDB2026-HowMuchCanRocksDBChewAchievingNearZeroWriteStallswithSustainableRocksDB.pdf | VLDB 2026 | How Much Can RocksDB Chew? Achieving Near-Zero Write Stalls with Sustainable RocksDB | [来源](https://www.vldb.org/pvldb/vol19/p3202-shin.pdf) |
| SAP Adaptive Server | VLDB2014-AdaptiveQueryProcessingonRAWData.pdf | VLDB 2014 | Adaptive Query Processing on RAW Data | [来源](https://vldb.org/pvldb/vol7/p1119-karpathiotakis.pdf) |
| SAP Adaptive Server | VLDB2014-ScalableandAdaptiveOnlineJoins.pdf | VLDB 2014 | Scalable and Adaptive Online Joins | [来源](https://vldb.org/pvldb/vol7/p441-elseidy.pdf) |
| SAP Adaptive Server | VLDB2020-ParallelGraphAlgorithmsinConstantAdaptiveRoundsTheorymeetsPractice.pdf | VLDB 2020 | Parallel Graph Algorithms in Constant Adaptive Rounds: Theory meets Practice | [来源](https://www.vldb.org/pvldb/vol13/p3588-behnezhad.pdf) |
| SAP Adaptive Server | VLDB2021-AdaptiveCodeGenerationforDataIntensiveAnalytics.pdf | VLDB 2021 | Adaptive Code Generation for Data-Intensive Analytics | [来源](https://www.vldb.org/pvldb/vol14/p929-zhang.pdf) |
| SAP Adaptive Server | VLDB2021-BreakingDownMemoryWallsAdaptiveMemoryManagementinLSMbasedStorageSystems.pdf | VLDB 2021 | Breaking Down Memory Walls: Adaptive Memory Management in LSM-based Storage Systems | [来源](https://www.vldb.org/pvldb/vol14/p241-luo.pdf) |
| SAP Adaptive Server | VLDB2026-BreakingtheIsolationFreshnessTradeoffJointAdaptiveStorageOptimizationforHTAPSystems.pdf | VLDB 2026 | Breaking the Isolation-Freshness Trade-off: Joint Adaptive Storage Optimization for HTAP Systems | [来源](https://www.vldb.org/pvldb/vol19/p1142-ding.pdf) |
| SAP Adaptive Server | VLDB2026-ReStoreinActionAdaptiveMultiTierStorageManagementviaIntelligentDataMigrationPolicy.pdf | VLDB 2026 | ReStore-in-Action: Adaptive Multi-Tier Storage Management via Intelligent Data Migration Policy | [来源](https://www.vldb.org/pvldb/vol19/p4702-zhang.pdf) |
| SAP Adaptive Server | VLDB2026-SankofaOnlineQueryadaptiveDynamicGraphSummaries.pdf | VLDB 2026 | Sankofa: Online Query-adaptive Dynamic Graph Summaries | [来源](https://www.vldb.org/pvldb/vol19/p2908-karras.pdf) |
| SAP HANA | VLDB2013-SAPHANATheEvolutionfromaModernMainMemoryDataPlatformtoanEnterpriseApplicationPlatform.pdf | VLDB 2013 | SAP HANA: The Evolution from a Modern Main-Memory Data Platform to an Enterprise Application Platform | [来源](https://vldb.org/pvldb/vol6/p1184-sikka.pdf) |
| SAP HANA | VLDB2017-ParallelReplicationacrossFormatsinSAPHANAforScalingOutMixedOLTPOLAPWorkloads.pdf | VLDB 2017 | Parallel Replication across Formats in SAP HANA for Scaling Out Mixed OLTP/OLAP Workloads | [来源](https://vldb.org/pvldb/vol10/p1598-han.pdf) |
| SAP HANA | VLDB2019-NativeStoreExtensionforSAPHANA.pdf | VLDB 2019 | Native Store Extension for SAP HANA | [来源](https://vldb.org/pvldb/vol12/p2047-sherkat.pdf) |
| SAP HANA | VLDB2019-SAPHANAgoesprivateFromPrivacyResearchtoPrivacyAwareEnterpriseAnalytics.pdf | VLDB 2019 | SAP HANA goes private - From Privacy Research to Privacy Aware Enterprise Analytics | [来源](https://vldb.org/pvldb/vol12/p1998-kessler.pdf) |
| SAP HANA | VLDB2024-AnExaminationofCXLMemoryUseCasesforInMemoryDatabaseManagementSystemsusingSAPHANA.pdf | VLDB 2024 | An Examination of CXL Memory Use Cases for In-Memory Database Management Systems using SAP HANA | [来源](https://www.vldb.org/pvldb/vol17/p3827-ahn.pdf) |
| SAP HANA | VLDB2025-TheHANANativeQueryEngineforLakehouseSystems.pdf | VLDB 2025 | The HANA Native Query Engine for Lakehouse Systems | [来源](https://www.vldb.org/pvldb/vol18/p4831-ritter.pdf) |
| ScyllaDB | arXiv2023-ScyllaDBAShardperCoreNoSQLDatabase.pdf | — | ScyllaDBAShardperCoreNoSQLDatabase | [来源]() |
| SingleStore | VLDB2024-SingleStoreVAnIntegratedVectorDatabaseSysteminSingleStore.pdf | VLDB 2024 | SingleStore-V: An Integrated Vector Database System in SingleStore | [来源](https://www.vldb.org/pvldb/vol17/p3772-chen.pdf) |
| Snowflake | Paper-Snowflake_SIGMODpdf.pdf | — | Snowflake_SIGMODpdf | [来源]() |
| Snowflake | VLDB2025-WorkloadInsightsFromtheSnowflakeDataCloudWhatDoProductionAnalyticQueriesReallyLookLike.pdf | VLDB 2025 | Workload Insights From the Snowflake Data Cloud: What Do Production Analytic Queries Really Look Like? | [来源](https://www.vldb.org/pvldb/vol18/p5126-bress.pdf) |
| Sphinx | VLDB2020-SPHINXASystemforMetapathbasedEntityExplorationinHeterogeneousInformationNetworks.pdf | VLDB 2020 | SPHINX: A System for Metapath-based Entity Exploration in Heterogeneous Information Networks | [来源](https://www.vldb.org/pvldb/vol13/p2913-chatzopoulos.pdf) |
| Sphinx | VLDB2025-SphinxASuccinctPerfectHashIndexforx86.pdf | VLDB 2025 | Sphinx: A Succinct Perfect Hash Index for x86 | [来源](https://www.vldb.org/pvldb/vol18/p4424-maghrebi.pdf) |
| SQLite | Paper2015-AJITforSQLite.pdf | — | AJITforSQLite | [来源]() |
| SQLite | VLDB2015-SQLiteOptimizationwithPhaseChangeMemoryforMobileApplications.pdf | VLDB 2015 | SQLite Optimization with Phase Change Memory for Mobile Applications | [来源](https://vldb.org/pvldb/vol8/p1454-oh.pdf) |
| SQLite | VLDB2018-SQLStatementLoggingforMakingSQLiteTrulyLite.pdf | VLDB 2018 | SQL Statement Logging for Making SQLite Truly Lite | [来源](https://vldb.org/pvldb/vol11/p513-park.pdf) |
| SQLite | VLDB2022-SQLitePastPresentandFuture.pdf | VLDB 2022 | SQLite: Past, Present, and Future | [来源](https://www.vldb.org/pvldb/vol15/p3535-gaffney.pdf) |
| Tencent TDSQL | PPT2019-ConceptualModelingonTencentDistributedDatabaseSystems.pdf | — | ConceptualModelingonTencentDistributedDatabaseSystems | [来源]() |
| Tencent TDSQL | Paper-腾讯云.pdf | VLDB 2009 | Believe It or Not: Adding Belief Annotations to Databases | [来源](https://vldb.org/pvldb/vol2/vldb09-115.pdf) |
| Tencent TDSQL | VLDB2019-ALightweightandEfficientTemporalDatabaseManagementSysteminTDSQL.pdf | VLDB 2019 | A Lightweight and Efficient Temporal Database Management System in TDSQL | [来源](https://vldb.org/pvldb/vol12/p2035-lu.pdf) |
| Tencent TDSQL | VLDB2024-TDSQLTencentDistributedDatabaseSystem.pdf | VLDB 2024 | TDSQL: Tencent Distributed Database System | [来源](https://www.vldb.org/pvldb/vol17/p3869-chen.pdf) |
| Tencent TDSQL | VLDB2026-ReachingthePinnacleofTPCDSCodesignofArchitectureExecutorandStorageinTDSQL.pdf | VLDB 2026 | Reaching the Pinnacle of TPC-DS: Co-design of Architecture, Executor, and Storage in TDSQL | [来源](https://www.vldb.org/pvldb/vol19/p4009-chu.pdf) |
| Tencent TDSQL | WWW2019-EfficientTimeintervalDataExtractioninMVCCbasedRDBMS.pdf | — | EfficientTimeintervalDataExtractioninMVCCbasedRDBMS | [来源]() |
| Tera | Paper-PowerPoint演示文稿.pdf | — | PowerPoint演示文稿 | [来源]() |
| Teradata | VLDB2016-HybridRowColumnPartitioninginTeradata.pdf | VLDB 2016 | Hybrid Row-Column Partitioning in Teradata | [来源](https://vldb.org/pvldb/vol9/p1353-alKateb.pdf) |
| Teradata | VLDB2019-IndatabaseDistributedMachineLearningDemonstrationusingTeradataSQLEngine.pdf | VLDB 2019 | In-database Distributed Machine Learning: Demonstration using Teradata SQL Engine | [来源](https://vldb.org/pvldb/vol12/p1854-sandha.pdf) |
| Teradata | VLDB2021-NotBlackBoxAnymoreEnablingAnalyticsAwareOptimizationsinTeradataVantage.pdf | VLDB 2021 | Not Black-Box Anymore! Enabling Analytics-Aware Optimizations in Teradata Vantage | [来源](https://www.vldb.org/pvldb/vol14/p2959-eltabakh.pdf) |
| TiDB | PPT2020-ADanceonRaft.pdf | — | ADanceonRaft | [来源]() |
| TiDB | VLDB2020-TiDBARaftbasedHTAPDatabase.pdf | VLDB 2020 | TiDB: A Raft-based HTAP Database | [来源](https://www.vldb.org/pvldb/vol13/p3072-huang.pdf) |
| TigerGraph | 2021-ForresterTEITigerGraphROIReport.pdf | — | ForresterTEITigerGraphROIReport | [来源]() |
| TigerGraph | VLDB2017-TigerGraphAFastandScalableGraphDatabase.pdf | — | TigerGraphAFastandScalableGraphDatabase | [来源]() |
| Vertica | VLDB2012-TheVerticaAnalyticDatabaseCStore7YearsLater.pdf | VLDB 2012 | The Vertica Analytic Database: C-Store 7 Years Later | [来源](https://vldb.org/pvldb/vol5/p1790_andrewlamb_vldb2012.pdf) |
| VoltDB | Paper-GuidetoPerformanceandCustomization.pdf | — | GuidetoPerformanceandCustomization | [来源]() |
| VoltDB | Paper-UsingVoltDB.pdf | — | UsingVoltDB | [来源]() |
| VoltDB | Paper2016-WhatsReallyNewwithNewSQL.pdf | — | WhatsReallyNewwithNewSQL | [来源]() |
| VoltDB | Paper2017-hvwhitepapervoltdbtechnicaloverviewpdf.pdf | — | hvwhitepapervoltdbtechnicaloverviewpdf | [来源]() |
| YugabyteDB | arXiv2020-YugabyteDBDistributedSQLatPlanetScale.pdf | — | YugabyteDBDistributedSQLatPlanetScale | [来源]() |
