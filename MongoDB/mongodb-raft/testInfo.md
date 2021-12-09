# MongoDB Raft Testing Info

## TLA+

A complete mongodb's replication protocol **may**(only according to [MongoDB-Raft](), the implementation may have more) include the following modules(:method)   
- Leader Election: timeout, requesetVote, sync
- Log Replication: pull, updatePos, sync
- Log Commit: commitPointAdvance, commitPointLearn, sync
- Sync Source Select: rule
- Heartbeat: timeout, term, commitPointLearn
- Membership Reconfig: add, remove
- Speculative Execution: 
- Initial Sync:
- Preserve Uncommitted Log:
- Additional Replica Roles: arbiter, non-voting member

Each of the following TLA+ did different simplifications($\to$) to different modules 
- [mongo/tla_plus](https://github.com/mongodb/mongo/tree/master/src/mongo/tla_plus)
  - RaftMongo.tla
    - Leader Election $\to$ set new leader directly
    - Log Replication $\to$ push, sync
    - Log Commit $\to$ commitPointAdvance, commitPointLearn, sync
  - RaftMongoWithRaftReconfig.tla(based on RaftMongo.tla)
    - Leader Election $\to$ set new leader directly
    - Log Replication $\to$ push, sync
    - Log Commit $\to$ commitPointAdvance
    - Heartbeat: term
    - Membership Reconfig: add, remove
  - MongoReplReconfig:
    - Leader Election $\to$ set new leader directly
    - Log Replication $\to$ pull, sync
    - Log Commit $\to$ commitPointAdvance
    - Membership Reconfig $\to$ add, remove
- [visualzhou / mongo-repl-tla](https://github.com/visualzhou/mongo-repl-tla)
  - may be the origin of the mongo rep's RaftMongo*.tla, a little different with above
- [will62794 / mongo-repl-tla](https://github.com/will62794/mongo-repl-tla)
  - MongoRepl.tla
    - Leader Election $\to$ timeout, requestVote
    - Log Replication $\to$ push, updatePos, sync
    - Log Commit $\to$ commitPointAdvance, commitPointLearn
- [will62794/mongo-repl-tla-models](https://github.com/will62794/mongo-repl-tla-models)
  - RaftMongo.tla: similar to above
  - RaftMongoSyncSources.tla(based on RaftMongo.tla)
    - Leader Election $\to$ set new leader directly
    - Log Replication $\to$ push, sync
    - Log Commit $\to$ commitPointAdvance, commitPointLearn
    - Sync Source Select $\to$ random

## Model Based Trace Checking
[Two attempts to compare a TLA+ spec with a C++ implementation; 2020](https://emptysqua.re/blog/extreme-modelling-in-practice/)

[arXiv2011 1111.2826 Concurrent Development of Model and Implementation](https://arxiv.org/abs/1111.2826)

[VLDB2020: Extreme Modelling in Practice](../mongodb-papers/VLDB2020%20eXtreme%20Modelling%20in%20Practice.pdf)
	
- 工作：实践了论文 [arXiv2011](https://arxiv.org/abs/1111.2826) 中的两个案例学习，其一为使用MBTC(“model-based trace-checking")来检验MongoDB复制协议的TLA+规约 [RaftMongo.tla](https://github.com/mongodb/mongo/tree/master/src/mongo/tla_plus/RaftMongo)
- 方法：执行手写测试来获取执行trace，然后判断trace是否满足TLA+规约。
- 结果：边际成本越来越高，进行了10周的工作后放弃此方法。
- 主要原因：
  - 获取到串行 trace 需要在实现中加锁，加大工作量
  - 规约过于简化，且规约为突出重点与实现的trace不符合，重新制定规约成本高且违背规约目的
  - 目前对带有TLA+和TLC的MBTC测试支持还不完善，测试耗时太大

## Fuzzing Testing
mongodb目前为止发现bug最多的工具

[paper](../mongodb-papers/ACM%20Queue2017%20MongoDB%20JavaScript%20Fuzzer.pdf)

[src: JStest](https://github.com/mongodb/mongo/tree/master/jstests)

TODO: RUN



## Integration Testing
TODO: SEARCH & RUN


## Unit Testing
TODO: SEARCH & RUN

## Fault-Injection Testing
TODO: SEARCH & RUN

## Jepsen Testing
[MongoDB 3.4.0-rc3 (jepsen.io); kenwalger on Feb 7, 2017](https://news.ycombinator.com/item?id=13590457)

TODO: RUN