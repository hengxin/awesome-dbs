# OceanBase

- [oceanbase](https://oceanbase.alipay.com/)
> 强一致: 数据多副本通过 Paxos 协议同步事务日志，多数派成功事务才能提交。
> 缺省情况下读、写操作在主副本进行，保证强一致。

- [Oceanbase 列传](http://oceanbase.org.cn/)

## OceanBase 记录
- [支付宝背后的OceanBase: 国产自研分布式数据库这十年 (QCon; 2019)](https://www.bilibili.com/video/BV1Cb411j7mN/)

## OceanBase 团队讲座
- [深入解析OceanBase数据库 (2020-07)](https://www.bilibili.com/video/BV1DT4y1J7zw/)
  - 存储引擎、分布式事务层、SQL 引擎
  - 架构: 数据分区、每个分区有多个副本、多副本间使用 Paxos/Raft 协议
  - 分布式事务: 2PC 及其优化
  - 多种容灾部署方式, 延迟不同

## books
- [大规模分布式存储系统: 原理解析与架构实战 (杨传辉)]()

OceanBase is an open source distributed relational DBMS which is fully compatible with MySQL. It handles HTAP mixed loads with one set of computing engines at the same time.

## 基本信息

- **数据库类型**: SQL、向量、文档、宽列
- **所属机构**: OceanBase previously Alibaba and Ant Group
- **许可证**: Mulan PubL v2
- **首次发布**: 2010

## 官网与文档

- [官网](https://en.oceanbase.com/)
- [官网](https://www.oceanbase.com)
- [官方文档](https://en.oceanbase.com/docs)
- [官方文档](https://en.oceanbase.com/docs/oceanbase-database)
- [GitHub](https://github.com/oceanbase/oceanbase)

## 数据源

- [DB-Engines](https://db-engines.com/en/system/OceanBase)
- [Database of Databases](https://dbdb.io/db/oceanbase)

## 收录资料

### 论文

| 文件 | 发表 | 标题 | 来源 |
| --- | --- | --- | --- |
| [VLDB2022-OceanBaseA707MilliontpmCDistributedRelationalDatabaseSystem.pdf](papers/VLDB2022-OceanBaseA707MilliontpmCDistributedRelationalDatabaseSystem.pdf) | VLDB 2022 | OceanBase: A 707 Million tpmC Distributed Relational Database System | [来源](https://www.vldb.org/pvldb/vol15/p3385-xu.pdf) |
| [VLDB2023-OceanBasePaeticaAHybridSharednothingSharedeverythingDatabaseforSupportingSingleMachineandDistributedCluster.pdf](papers/VLDB2023-OceanBasePaeticaAHybridSharednothingSharedeverythingDatabaseforSupportingSingleMachineandDistributedCluster.pdf) | VLDB 2023 | OceanBase Paetica: A Hybrid Shared-nothing/Shared-everything Database for Supporting Single Machine and Distributed Cluster | [来源](https://www.vldb.org/pvldb/vol16/p3728-xu.pdf) |
| [VLDB2026-ATreeStructuredTwoPhaseCommitFrameworkforOceanBaseOptimizingScalabilityandConsistency.pdf](papers/VLDB2026-ATreeStructuredTwoPhaseCommitFrameworkforOceanBaseOptimizingScalabilityandConsistency.pdf) | VLDB 2026 | A Tree-Structured Two-Phase Commit Framework for OceanBase: Optimizing Scalability and Consistency | [来源](https://www.vldb.org/pvldb/vol19/p4250-xu.pdf) |
| [VLDB2026-OceanBaseBacchusaHighPerformanceandScalableCloudNativeSharedStorageArchitectureforMultiCloud.pdf](papers/VLDB2026-OceanBaseBacchusaHighPerformanceandScalableCloudNativeSharedStorageArchitectureforMultiCloud.pdf) | VLDB 2026 | OceanBase Bacchus: a High-Performance and Scalable Cloud-Native Shared Storage Architecture for Multi-Cloud | [来源](https://www.vldb.org/pvldb/vol19/p4089-xu.pdf) |

### 官方文档与白皮书

| 文件 | 标题 | 来源 |
| --- | --- | --- |
| [OceanBaseDocumentationCenter.md](docs/OceanBaseDocumentationCenter.md) | OceanBase Documentation Center | [来源](https://en.oceanbase.com/docs) |
