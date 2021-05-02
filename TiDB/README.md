# TiDB

- [官网 pingcap](pingcap.com)
  > TiDB 是一款定位于在线事务处理/在线分析处理
  > (HTAP: Hybrid Transactional/Analytical Processing）的融合型数据库产品，
  > 实现了一键水平伸缩，强一致性的多副本数据安全 (使用Raft协议)，分布式事务，实时 OLAP 等重要特性。
  > 同时兼容 MySQL 协议和生态，迁移便捷，运维成本极低。

## Roadmap
- 基础: [PingCAP University](https://university.pingcap.com/categories)
  > 以下两条学习路线可以交叉并行, 也可以依次学习。注意: 一定要边学边实践
  - `PCTA` => `PCTP` => `High Performance TiDB`
  - `TiDB 4.0 新手指南` => `TiDB 应用开发指南` => `TiDB 4.0 运维指南`

- 进阶: [TiDB_Robot @ bilibili](https://space.bilibili.com/86485707?from=search&seid=14267980155843203005)
  > 这里有很多最新的动态与技术介绍

- 理论:
  - [VLDB2020 paper](/TiDB/VLDB2020%20TiDB%20A%20Raft-based%20HTAP%20Database.pdf)
  - [Raft](PPT2020%20(TiDB-EdHuang)%20A%20Dance%20on%20Raft.pdf)

  - [pingcap/tla-plus @ github](https://github.com/pingcap/tla-plus)
    > TLA+ in TiDB: Raft, Distributed Transactions (Percolator)