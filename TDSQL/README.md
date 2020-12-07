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