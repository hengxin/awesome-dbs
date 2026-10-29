# TiDB

- [官网 pingcap](pingcap.com)
  > TiDB 是一款定位于在线事务处理/在线分析处理
  > (HTAP: Hybrid Transactional/Analytical Processing）的融合型数据库产品，
  > 实现了一键水平伸缩，强一致性的多副本数据安全 (使用Raft协议)，分布式事务，实时 OLAP 等重要特性。
  > 同时兼容 MySQL 协议和生态，迁移便捷，运维成本极低。
- [pingcap@github](https://github.com/pingcap)
  - [pingcap/tidb](https://github.com/pingcap/tidb)
  - [pingcap/tla-plus @ github](https://github.com/pingcap/tla-plus)
    > TLA+ in TiDB: Raft, Distributed Transactions (Percolator)
  - [pingcap/tipocket](https://github.com/pingcap/tipocket)
    > Jepsen-inspired testing tools

## Roadmap
### TiDB Basics
- [PingCAP University](https://university.pingcap.com/categories)
  > 以下两条学习路线可以交叉并行, 也可以依次学习。注意: 一定要边学边实践
  - `PCTA` => `PCTP` => `High Performance TiDB`
  - `TiDB 4.0 新手指南` => `TiDB 应用开发指南` => `TiDB 4.0 运维指南`
- [Book: TiDB in Action](https://book.tidb.io/)

### Advanced
- [TiDB_Robot @ bilibili](https://space.bilibili.com/86485707?from=search&seid=14267980155843203005)
  > 这里有很多最新的动态与技术介绍

### Dive into TiDB
- ***Highly Recommended:*** [TiDB Talent Plan](https://tidb.net/talent-plan)

### More Theory
  - [VLDB2020 paper](/TiDB/VLDB2020%20TiDB%20A%20Raft-based%20HTAP%20Database.pdf)
  - [Raft](PPT2020-ADanceonRaft.pdf)

TiDB is an open-source distributed SQL database that supports Hybrid Transactional and Analytical Processing (HTAP) workloads. It is MySQL compatible and features horizontal scalability, strong consistency, and high availability.

## 基本信息

- **数据库类型**: SQL、向量、OLAP
- **所属机构**: PingCAP, Inc.
- **许可证**: Apache v2
- **首次发布**: 2016

## 官网与文档

- [官网](https://pingcap.com/)
- [官网](https://www.pingcap.com)
- [官方文档](https://docs.pingcap.com)
- [官方文档](https://docs.pingcap.com/tidb/stable/)
- [GitHub](https://github.com/pingcap/tidb)

## 数据源

- [DB-Engines](https://db-engines.com/en/system/TiDB)
- [Database of Databases](https://dbdb.io/db/tidb)

## 收录资料

### 论文

| 文件 | 发表 | 标题 | 来源 |
| --- | --- | --- | --- |
| [PPT2020-ADanceonRaft.pdf](tidb-papers/PPT2020-ADanceonRaft.pdf) | PPT 2020 |  | [来源]() |
| [VLDB2020-TiDBARaftbasedHTAPDatabase.pdf](tidb-papers/VLDB2020-TiDBARaftbasedHTAPDatabase.pdf) | VLDB 2020 | TiDB: A Raft-based HTAP Database | [来源](https://www.vldb.org/pvldb/vol13/p3072-huang.pdf) |

### 官方文档与白皮书

| 文件 | 标题 | 来源 |
| --- | --- | --- |
| [HomeTiDBDocs.md](docs/HomeTiDBDocs.md) | Home \| TiDB Docs | [来源](https://docs.pingcap.com) |
