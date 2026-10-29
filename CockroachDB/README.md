# CockroachDB

- [CockroachDB](https://www.cockroachlabs.com/)
> Guarantee transactional consistency at any scale:
> In a distributed environment, competing transactions
> can come from anywhere.
> Only CockroachDB provides the highest level of isolation
> (serializable) in a distributed database.

- [CockroachDB @ SIGMOD2020](https://dl.acm.org/doi/abs/10.1145/3318464.3386134)
> CockroachDB is a scalable SQL DBMS that was built from the ground up
> to support global OLTP workloads while maintaining high availability and strong consistency.

> [CockroachDB](https://blog.yugabyte.com/implementing-distributed-transactions-the-google-way-percolator-vs-spanner),
> a PostgreSQL-compatible distributed database,
> supports global ACID transactions similar to Spanner.

CockroachDB (sometimes shortened as CRDB) is a free and open source distributed SQL database built on a transactional and strongly-consistent key-value store. It is backed by PebbleDB (a RocksDB/LevelDB-inspired KV store) and uses the Raft distributed consensus algorithm to ensure consistency.

## 基本信息

- **数据库类型**: SQL
- **所属机构**: Cockroach Labs
- **许可证**: Business Source License
- **首次发布**: 2014
- **国家/地区**: US

## 官网与文档

- [官网](https://www.cockroachlabs.com)
- [官方文档](https://www.cockroachlabs.com/docs/stable)
- [GitHub](https://github.com/cockroachdb/cockroach)

## 数据源

- [Database of Databases](https://dbdb.io/db/cockroachdb)

## 收录资料

### 论文

| 文件 | 发表 | 标题 | 来源 |
| --- | --- | --- | --- |
| [2019-TheDefinitiveGuidetoCockroachDB.pdf](papers/2019-TheDefinitiveGuidetoCockroachDB.pdf) | — |  | [来源]() |
| [SIGMOD2020-CockroachDBTheResilientGeoDistributedSQLDatabase.pdf](papers/SIGMOD2020-CockroachDBTheResilientGeoDistributedSQLDatabase.pdf) | SIGMOD 2020 |  | [来源]() |
| [VLDB2022-ADemonstrationofMultiRegionCockroachDB.pdf](papers/VLDB2022-ADemonstrationofMultiRegionCockroachDB.pdf) | VLDB 2022 | A Demonstration of Multi-Region CockroachDB | [来源](https://www.vldb.org/pvldb/vol15/p3610-taft.pdf) |

### 官方文档与白皮书

| 文件 | 标题 | 来源 |
| --- | --- | --- |
| [CockroachDBDocs-CockroachDB.md](docs/CockroachDBDocs-CockroachDB.md) | CockroachDB Docs - CockroachDB | [来源](https://www.cockroachlabs.com/docs/stable) |
