# MongoDB Raft

## Papers
- [NSDI2021: Fault-tolerant Replication with Pull-based Consensus in MongoDB](../mongodb-papers/NSDI2021%20Fault-Tolerant%20Replication%20with%20Pull-Based%20Consensus%20in%20MongoDB.pdf)
- [arXiv2021: Design and Verification of a Logless Dynamic Reconfiguration Protocol in MongoDB Replication](../mongodb-papers/arXiv2021%202102.11960%20Design%20and%20Verification%20of%20a%20Logless%20Dynamic%20Reconfiguration%20Protocol%20in%20MongoDB%20Replication.pdf)
- [VLDB2019: Tunable Consistency in MongoDB](../mongodb-papers/VLDB2019%20Schultz%20Tunable%20Consistency%20in%20MongoDB.pdf)
  - Section 6: `Supporting a Spectrum of Consistency Levels in a Single Deployment`
- [VLDB2020: Extreme Modelling in Practice](../mongodb-papers/VLDB2020%20eXtreme%20Modelling%20in%20Practice.pdf)

## TLA+
- [Two attempts to compare a TLA+ spec with a C++ implementation; 2020](https://emptysqua.re/blog/extreme-modelling-in-practice/)
- [Fixing a MongoDB Replication Protocol Bug with TLA+ - William Schultz; 2019](https://www.youtube.com/watch?v=x9zSynTfLDE)
  - [A Bug's Life Fixing a MongoDB Replication Protocol Bug with TLA+](../mongodb-papers/A%20Bug%20Life%20Fixing%20a%20MongoDB%20Replication%20Protocol%20Bug%20with%20TLA+%20William%20Schultz%20-%20Strangeloop%20TLA+%20Conference%202019.pdf)
  - [will62794 / mongo-repl-tla](https://github.com/will62794/mongo-repl-tla)
- [visualzhou / mongo-repl-tla](https://github.com/visualzhou/mongo-repl-tla)
  - [TLA+ at MongoDB @ reddit](https://www.reddit.com/r/tlaplus/comments/76zule/tla_at_mongodb/)

## Jepsen
- [Jepsen on Redis Raft](https://jepsen.io/analyses/redis-raft-1b3fbf6)