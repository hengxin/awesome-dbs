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