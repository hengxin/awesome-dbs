# OceanBase Meetup (20200920 Shanghai)

## 事务并发控制的思考与实现
- 分布式事务: 2PC + 2PL
- 外部一致性 串行化隔离级别
- 优化: 提前释放锁 (问题: 如何保证正确性)
- 级联回滚问题
- OceanBase 编程语言: C & C++ & 汇编 (内存管理)

## 事务故障恢复的原理与实践
### 单机数据库
- A & D: 与故障恢复相关S
- 存储模型
- 事务故障恢复
  - 回滚
  - 重做
- 落盘策略: Force & Steal
- Undo 日志
- Redo 日志
- RocksDB
  - 基于 LSM-Tree
- Oracle (Steal & No-Froce)
- 日志回收
- Checkpoint 机制
  - Pause 模型
  - Oracle
- 论文: ARIES (1992)

### 分布式数据库
- 仍然要保证 A & D
- 新的问题: 数据分区
- Sage (长事务的提交: 拆分成多个小事务)
  - 以此提交
  - 反向补偿回滚
- 2PL
  - 问题: 参与者可能阻塞
- Percolator
  - 基于 BigTable 的行级事务
  - 2PL 的变种

### OceanBase
- Sharing-nothing 架构
  - 数据分片
  - 分片: Paxos Group，有 leader
  - 单分片: 单机事务
  - 多分片: 2PL
- 单分片
  - LSM-tree, 实现 Steal & No-Force
- 多分片
  - 参与者: 内嵌 Paxos 实现的多副本机制
  - 协调者: 日志优化（无状态化; 协调者不需要写日志）; 协调者宕机: 询问参与者
  - 提交时延优化
    - 提前返回给用户

## RDS MySQL 云原生中间件在网易的实践

### MGR
- MySQL 复制架构 (MySQL Group Replication)
  - 无 shard
  - 多主
  - XCom: 借助 Paxos 实现强一致性
    - Mencius Paxos (多提交者; 无 election 过程)
  - 事务生命周期
    - certify
  - 基本特征
    - 成员节点管理
    - failover 故障修复
### 网易对 MGR 的优化 
- 内存优化 (Single-Primary 模型)
  - 冲突检测
  - Paxos 消息复杂度高
- 故障恢复优化

### 实践
- 不建议跨域部署 MGR (同城机房网络延时最好不要超过 10ms)

## 数据库高可用面临的挑战与解决之道

### 为什么要高可用
### 分布式一致性协议
### OceanBase 一致性工程实践
- 日志乱序同步