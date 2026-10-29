# JanusGraph

- 来源: https://docs.janusgraph.org/
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

[Skip to content](#the-benefits-of-janusgraph)
[](.)
JanusGraph
Introduction
Initializing search
[JanusGraph](https://github.com/janusgraph/janusgraph)
[](.)
JanusGraph
[JanusGraph](https://github.com/janusgraph/janusgraph)
-
Introduction
[Introduction](.)
Table of contents
-
[The Benefits of JanusGraph](#the-benefits-of-janusgraph)
-
[General JanusGraph Benefits](#general-janusgraph-benefits)
-
[Benefits of JanusGraph with Apache Cassandra](#benefits-of-janusgraph-with-apache-cassandra)
-
[Benefits of JanusGraph with HBase](#benefits-of-janusgraph-with-hbase)
-
[JanusGraph and the CAP Theorem](#janusgraph-and-the-cap-theorem)
-
Getting Started
Getting Started
-
[Installation](getting-started/installation/)
-
[Basic Usage](getting-started/basic-usage/)
-
[Gremlin Query Language](getting-started/gremlin/)
-
[Architectural Overview](getting-started/architecture/)
-
JanusGraph Basics
JanusGraph Basics
-
[Transactions](basics/transactions/)
-
[Search Predicates and Mixed Index Data Types](basics/search-predicates/)
-
Connecting to JanusGraph
Connecting to JanusGraph
-
[Introduction](basics/connecting/)
-
[Using Java](basics/connecting/java/)
-
[Using Python](basics/connecting/python/)
-
[Using .NET](basics/connecting/dotnet/)
-
Configuration
Configuration
-
[Introduction](configs/)
-
[Configuration Reference](configs/configuration-reference/)
-
[Config Example](configs/example-config/)
-
Schema Management
Schema Management
-
[Schema and Data Modeling](schema/)
-
[Advanced Schema](schema/advschema/)
-
Index Management
Index Management
-
[Indexing for Better Performance](schema/index-management/index-performance/)
-
[Index Lifecycle](schema/index-management/index-lifecycle/)
-
[Reindexing](schema/index-management/index-reindexing/)
-
[Removal](schema/index-management/index-removal/)
-
[Schema Initialization](schema/schema-init-strategies/)
-
Operations
Operations
-
[JanusGraph Server](operations/server/)
-
[Deployment Scenarios](operations/deployment/)
-
[JanusGraph Container](operations/container/)
-
[ConfiguredGraphFactory](operations/configured-graph-factory/)
-
[Dynamic Graphs](operations/dynamic-graphs/)
-
[Batch Processing](operations/batch-processing/)
-
[Bulk Loading](operations/bulk-loading/)
-
[JanusGraph Cache](operations/cache/)
-
[Monitoring](operations/monitoring/)
-
[Migrating from Titan](operations/migrating-titan/)
-
[Migrating from Thrift](operations/migrating-thrift/)
-
[Failure & Recovery](operations/recovery/)
-
[Management System](operations/management/)
-
Storage Backends
Storage Backends
-
[Introduction](storage-backend/)
-
[Apache Cassandra](storage-backend/cassandra/)
-
[Apache HBase](storage-backend/hbase/)
-
[Google Cloud Bigtable](storage-backend/bigtable/)
-
[ScyllaDB](storage-backend/scylladb/)
-
[Oracle Berkeley DB Java Edition](storage-backend/bdb/)
-
[InMemory Storage Backend](storage-backend/inmemorybackend/)
-
Mixed Index Backends
Mixed Index Backends
-
[Introduction](index-backend/)
-
[Index Parameters and Full-Text Search](index-backend/text-search/)
-
[Field Mapping](index-backend/field-mapping/)
-
[Direct Index Query](index-backend/direct-index-query/)
-
[Elasticsearch](index-backend/elasticsearch/)
-
[Apache Solr](index-backend/solr/)
-
[Apache Lucene](index-backend/lucene/)
-
Advanced Topics
Advanced Topics
-
[Eventually-Consistent Storage Backends](advanced-topics/eventual-consistency/)
-
[Custom Vertex ID](advanced-topics/custom-vertex-id/)
-
[Graph Partitioning](advanced-topics/partitioning/)
-
[Datatype and Attribute Serializer Configuration](advanced-topics/serializer/)
-
[JanusGraph with TinkerPop’s Hadoop-Gremlin](advanced-topics/hadoop/)
-
[Transaction Log](advanced-topics/transaction-log/)
-
[CDC Mixed Index Synchronization](advanced-topics/cdc-mixed-index/)
-
[JanusGraph Data model](advanced-topics/data-model/)
-
[JanusGraph Bus](advanced-topics/janusgraph-bus/)
-
[ExecutorService](advanced-topics/executor-service/)
-
[Permanent stale index inconsistency](advanced-topics/stale-index/)
-
[Technical Limitations](advanced-topics/technical-limitations/)
-
[Snapshot Releases](advanced-topics/commit-releases/)
-
[Common Questions](common-questions/)
-
[Development](development/)
-
[Changelog](changelog/)
Table of contents
-
[The Benefits of JanusGraph](#the-benefits-of-janusgraph)
-
[General JanusGraph Benefits](#general-janusgraph-benefits)
-
[Benefits of JanusGraph with Apache Cassandra](#benefits-of-janusgraph-with-apache-cassandra)
-
[Benefits of JanusGraph with HBase](#benefits-of-janusgraph-with-hbase)
-
[JanusGraph and the CAP Theorem](#janusgraph-and-the-cap-theorem)
# Introduction
## The Benefits of JanusGraph
JanusGraph is designed to support the processing of graphs so large that
they require storage and computational capacities beyond what a single
machine can provide. Scaling graph data processing for real time
traversals and analytical queries is JanusGraph’s foundational benefit.
This section will discuss the various specific benefits of JanusGraph
and its underlying, supported persistence solutions.
### General JanusGraph Benefits
- Support for very large graphs. JanusGraph graphs scale with the
number of machines in the cluster.
- Support for very many concurrent transactions and operational graph
processing. JanusGraph’s transactional capacity scales with the
number of machines in the cluster and answers complex traversal
queries on huge graphs in milliseconds.
- Support for global graph analytics and batch graph processing
through the Hadoop framework.
- Support for geo, numeric range, and full text search for vertices
and edges on very large graphs.
- Native support for the popular property graph data model exposed by
[Apache TinkerPop](https://tinkerpop.apache.org/).
- Native support for the graph traversal language
[Gremlin](https://tinkerpop.apache.org/gremlin.html).
- Numerous graph-level configurations provide knobs for tuning
performance.
- Vertex-centric indices provide vertex-level querying to alleviate
issues with the infamous [super node problem](https://www.datastax.com/blog/2012/10/solution-supernode-problem).
- Provides an optimized disk representation to allow for efficient use
of storage and speed of access.
- Open source under the liberal [Apache 2 license](https://en.wikipedia.org/wiki/Apache_License).
### Benefits of JanusGraph with Apache Cassandra
- [Continuously available](https://en.wikipedia.org/wiki/Continuous_availability)
with no single point of failure.
-
No read/write bottlenecks to the graph as there is no master/slave
architecture.
-
[Elastic scalability](https://en.wikipedia.org/wiki/Elastic_computing) allows
for the introduction and removal of machines.
- Caching layer ensures that continuously accessed data is available
in memory.
- Increase the size of the cache by adding more machines to the
cluster.
- Integration with [Apache Hadoop](https://hadoop.apache.org/).
- Open source under the liberal Apache 2 license.
### Benefits of JanusGraph with HBase
- Tight integration with the [Apache Hadoop](https://hadoop.apache.org/) ecosystem.
- Native support for [strong consistency](https://en.wikipedia.org/wiki/Strong_consistency).
- Linear scalability with the addition of more machines.
- [Strictly consistent](https://en.wikipedia.org/wiki/Strict_consistency) reads and writes.
- Convenient base classes for backing Hadoop
[MapReduce](https://en.wikipedia.org/wiki/MapReduce) jobs with HBase
tables.
- Support for exporting metrics via
[JMX](https://en.wikipedia.org/wiki/Java_Management_Extensions).
- Open source under the liberal Apache 2 license.
### JanusGraph and the CAP Theorem
Despite your best efforts, your system will experience enough faults
that it will have to make a choice between reducing yield (i.e., stop
answering requests) and reducing harvest (i.e., giving answers based
on incomplete data). This decision should be based on business
requirements.
— [Coda Hale](https://codahale.com/you-cant-sacrifice-partition-tolerance)
When using a database, the [CAP theorem](https://en.wikipedia.org/wiki/CAP_theorem) should be thoroughly
considered (C=Consistency, A=Availability, P=Partition tolerance).
JanusGraph is distributed with 3 supporting backends: [Apache Cassandra](https://cassandra.apache.org/),
[Apache HBase](https://hbase.apache.org/), and [Oracle Berkeley DB Java Edition](https://www.oracle.com/technetwork/database/berkeleydb/overview/index-093405.html).
Note that BerkeleyDB JE is a non-distributed database and is typically
only used with JanusGraph for testing and exploration purposes.
HBase gives preference to consistency at the expense of yield, i.e. the
probability of completing a request. Cassandra gives preference to
availability at the expense of harvest, i.e. the completeness of the
answer to the query (data available/complete data).
[Next
Installation](getting-started/installation/)
Copyright © 2025 JanusGraph Authors. All rights reserved.
The Linux Foundation has registered trademarks and uses trademarks. For a list of
trademarks of The Linux Foundation, please see our [Trademark Usage](https://www.linuxfoundation.org/trademark-usage) page.
Cassandra, Groovy, HBase, Hadoop, Lucene, Solr, and TinkerPop are trademarks of the Apache Software Foundation.
Berkeley DB and Berkeley DB Java Edition are trademarks of Oracle.
Made with
[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)
[](https://github.com/janusgraph)
[](https://discord.gg/5n4fjv4QAf)
[](https://twitter.com/janusgraph)
[](https://www.linkedin.com/company/janusgraph)
[](https://lists.lfaidata.foundation/g/janusgraph-users)
[](https://lists.lfaidata.foundation/g/janusgraph-dev)