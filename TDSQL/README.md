# TDSQL

## ***Papers***
- [WWW2018: Efficient time-interval data extraction in MVCC-based RDBMS](https://link.springer.com/article/10.1007/s11280-018-0552-7)
- [VLDB2019: A Lightweight and Efficient Temporal Database Management System in TDSQL](http://www.vldb.org/pvldb/vol12/p2035-lu.pdf)

## ***Haixiang Li***
- [腾讯TDSQL提出三个“数据库之问”，数据库技术未来重点在哪 (2019-10)](https://m.yisu.com/zixun/53983.html)
  - 事务一致性 + 分布式一致性
- [2019DTCC大会分享：分布式数据库全局读一致性](https://cloud.tencent.com/developer/article/1427602)

## Lectures (Official)
- [TDSQL核心技术架构原理解析 (2020-10)](https://www.bilibili.com/video/BV15V41127jU)
  - 分布式事务 (2PC)
- [TDSQL高可用技术解决方案介绍](https://www.bilibili.com/video/BV1jT4y1w7vJ)
  - 数据分区 + 主从; 强数据一致性 (强同步复制), 牺牲可用性; 容灾, 主备切换; 多种部署方案
- [腾讯云：新基建大潮下国产数据库的探索与思考](https://www.bilibili.com/video/BV1ff4y1y7Kr)
  - TDSQL: 基于主从架构的"并行多线程强同步复制方案" (Multi-thread Asynchronous Replication)

## Articles (Official)
- [腾讯分布式数据库TDSQL金融级能力的架构原理解读 (知乎专栏)](https://zhuanlan.zhihu.com/p/113954616)
  - TDSQL架构模块及其特性
  - 高性能的强同步 (接近异步性能的强同步???)
    - 线程池 (异步化???)
  - 分布式事务
    - 两阶段提交协议
    - 全局分布式死锁检测
- [腾讯会议核心数据库TDSQL，如何做到快速无损在线扩容 (知乎专栏)][https://zhuanlan.zhihu.com/p/139290689]

TDSQL is an abbreviation for TecentDistributed SQL. It is derived from MySQL and aimed at providing digital payment services for government and financial companies. TDSQL supports a strong consistency model based on Raft. Data are partitioned horizontally based on the partition key and auto sharding is enabled to facilitate data migration. TDSQL can be deployed on both private cloud and public…

## 基本信息

- **数据库类型**: SQL
- **所属机构**: Tencent
- **首次发布**: 2012
- **国家/地区**: CN

## 官网与文档

- [官网](http://tdsql.org)
- [官方文档](https://cloud.tencent.com/document/product/557)
- [GitHub](https://github.com/Tencent/TencentDB)

## 数据源

- [Database of Databases](https://dbdb.io/db/tdsql)

## 收录资料

### 论文

| 文件 | 发表 | 标题 | 来源 |
| --- | --- | --- | --- |
| [PPT2019-ConceptualModelingonTencentDistributedDatabaseSystems.pdf](papers/PPT2019-ConceptualModelingonTencentDistributedDatabaseSystems.pdf) | — |  | [来源]() |
| [Paper-腾讯云.pdf](papers/Paper-腾讯云.pdf) | — | 腾讯云 | [来源](https://main.qcloudimg.com/raw/3cc780eb2b03f8ea32878ba3eac47eb0.pdf) |
| [VLDB2019-ALightweightandEfficientTemporalDatabaseManagementSysteminTDSQL.pdf](papers/VLDB2019-ALightweightandEfficientTemporalDatabaseManagementSysteminTDSQL.pdf) | VLDB 2019 | A Lightweight and Efficient Temporal Database Management System in TDSQL | [来源](https://vldb.org/pvldb/vol12/p2035-lu.pdf) |
| [VLDB2024-TDSQLTencentDistributedDatabaseSystem.pdf](papers/VLDB2024-TDSQLTencentDistributedDatabaseSystem.pdf) | VLDB 2024 | TDSQL: Tencent Distributed Database System | [来源](https://www.vldb.org/pvldb/vol17/p3869-chen.pdf) |
| [VLDB2026-ReachingthePinnacleofTPCDSCodesignofArchitectureExecutorandStorageinTDSQL.pdf](papers/VLDB2026-ReachingthePinnacleofTPCDSCodesignofArchitectureExecutorandStorageinTDSQL.pdf) | VLDB 2026 | Reaching the Pinnacle of TPC-DS: Co-design of Architecture, Executor, and Storage in TDSQL | [来源](https://www.vldb.org/pvldb/vol19/p4009-chu.pdf) |
| [WWW2019-EfficientTimeintervalDataExtractioninMVCCbasedRDBMS.pdf](papers/WWW2019-EfficientTimeintervalDataExtractioninMVCCbasedRDBMS.pdf) | WWW 2019 |  | [来源]() |

### 官方文档与白皮书

| 文件 | 标题 | 来源 |
| --- | --- | --- |
| [TencentTDSQL.md](docs/TencentTDSQL.md) | Tencent TDSQL | [来源](https://cloud.tencent.com/document/product/557) |
