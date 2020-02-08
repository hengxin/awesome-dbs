# mongodb-jepsen-test

## [jepsen.io](https://jepsen.io/)

> Try to Read All Things on jepsen.io.

## [Jepsen Tests on MongoDB @ jepsen.io/analyses](https://jepsen.io/analyses)
- [Call Me Maybe: MongoDB 2.4.3 (2013-05-18)](https://aphyr.com/posts/284-call-me-maybe-mongodb)

> In this post, we’ll see MongoDB drop a phenomenal amount of data.

- [Jepsen: MongoDB stale reads 2.6.7 (2015-04-20)](https://aphyr.com/posts/322-jepsen-mongodb-stale-reads)

> Mongo’s consistency model is broken by design: 
not only can “strictly consistent” reads see stale versions of documents, 
but they can also return garbage data from writes that never should have occurred.

- [MongoDB 3.4.0-rc3 (2017-02-07); Kyle Kingsbury](https://jepsen.io/analyses/mongodb-3-4-0-rc3)

> In this Jepsen analysis, we develop new tests which show the MongoDB v0 replication protocol is intrinsically unsafe, 
allowing the loss of majority-committed documents. 
In addition, we show that the new v1 replication protocol has multiple bugs, 
allowing data loss in all versions up to MongoDB 3.2.11 and 3.4.0-rc4. 
While the v0 protocol remains broken, 
fixes for v1 are available in MongoDB 3.2.12 and 3.4.0, and now pass the expanded Jepsen test suite. 

- [MongoDB 3.6.4 (2018-10-23); Kit Patella](https://jepsen.io/analyses/mongodb-3-6-4)

> We'll also discuss MongoDB’s new support for causal consistency (CC) in version 3.6.4 and 4.0.0-rc1, 
and show that sessions prevent anomalies so long as user stick to majority reads and writes. 
However, with MongoDB’s default consistency levels, CC sessions fail to provide the claimed invariants.

> Finally, *there are significant limitations to our tests.* 
Our sharded tests assume a relatively uniform cluster topology, 
where all MongoDB components partition in the same way. 
Non-homogeneous topologies where we can partition configsvr 
and mongos processes separately from shardsvr processes may find unique anomalies. 
Starting and stopping and killing various component processes may also provide interesting results.

> Our causal consistency test only measures a very simple case: 
we test short time frames, on single keys, against single nodes, from single client threads. 
We suspect that writes to multiple nodes might be required to observe causal violations 
with majority writes and sub-majority reads.
We also don’t check how failures and process crashes influence causal orders.
*Ultimately, there’s still a lot we don’t know!*

## Discussions about Jepsen-Test on MongoDB
- [MongoDB 3.4.0-rc3 (jepsen.io); aphyr on Feb 7, 2017](https://news.ycombinator.com/item?id=13590385)

> Bigger news is that Jepsen tests are now part of the MongoDB continuous integration suite EverGreen.

- [MongoDB 3.4.0-rc3 (jepsen.io); kenwalger on Feb 7, 2017](https://news.ycombinator.com/item?id=13590457)

> MongoDB 3.4 passes the rigorous and tough Jepsen test. 
  Jepsen designs tests to make databases fail in terms of data consistency, correctness, and safety... 
  MongoDB 3.4 passed through their newest tests.
  I think that this really shows how mature of a Database MongoDB is. 

## Evergreen CI
- [Evergreen Continuous Integration: Why We Reinvented The Wheel; Kyle Erf, July 27, 2016](https://engineering.mongodb.com/post/evergreen-continuous-integration-why-we-reinvented-the-wheel/)

- [Testing Linearizability with Jepsen and Evergreen: "Call Me Continuously!"; Jonathan Abrahams, February 16, 2017](https://engineering.mongodb.com/post/testing-linearizability-with-jepsen-and-evergreen-call-me-continuously)

> In our case we have added linearizable reads to MongoDB 3.4 and use Jepsen to test it.
