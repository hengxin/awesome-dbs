# mongodb-tx-protocol

## MongoDB Docs
- [Transactions@docs](https://docs.mongodb.com/manual/core/transactions/)
  - With distributed transactions, transactions can be used 
    across multiple operations, collections, databases, documents, and shards.

- [MongoDB Transactions: Your very First Transaction with MongoDB 4.0; 2018](https://dzone.com/articles/mongodb-transactions-your-very-first-transaction-w)
  - Wrong Claim: MongoDB 4.0 implements snapshot isolation for the transactions.
  - But, what is the correct one?

## Specifications
- [mongodb/specifications/transactions](https://github.com/mongodb/specifications/tree/master/source/transactions)
  - ***VERY IMPORTANT!!!***

## Papers (See [here](https://github.com/hengxin/2020-ccf-tencent/tree/master/2020-ccf-tencent-projects/refs))
- [Tunable Consistency in MongoDB @ VLDB2019](http://www.vldb.org/pvldb/vol12/p2071-schultz.pdf)
  - ***VERY IMPORTANT!!!***
  - [Tunable Consistency in MongoDB @ Youtube](https://www.youtube.com/watch?v=x5UuQL9rA1c)

- [GSI:SRDS2005](https://github.com/hengxin/2020-ccf-tencent/blob/master/2020-ccf-tencent-projects/refs/SRDS2005%20Database%20Replication%20Using%20Generalized%20Snapshot%20Isolation.pdf)

- [ClockSI:SRDS2013](https://github.com/hengxin/2020-ccf-tencent/blob/master/2020-ccf-tencent-projects/refs/SRDS2013%20Clock-SI%20Snapshot%20Isolation%20for%20Partitioned%20Data%20Stores%20Using%20Loosely%20Synchronized%20Clocks.pdf)

## Lectures
- [Are Transactions Right For You? (2020)](https://www.mongodb.com/presentations/are-transactions-right-for-you-)
  - In this session you'll learn about the problems that transactions solve,
    their limitations, when transactions are not the best solution,
    and the optimal use of transactions in production.
  - Q: What is the transactional model?

## Articles
- [MongoDB 事务，复制和分片的关系 (MongoDB中文社区; May 2020)](https://mongoing.com/archives/38461)
> 本文尝试对Mongo的复制和分布式事务的原理进行描述，在必要的地方，对实现的正确性进行论证。

## Source Code
> ***You are expected to fill in this section.***