# Architecture | StarRocks

- 来源: https://docs.starrocks.io/docs/introduction/Architecture/
- 归档时间: 2026-10-29
- 说明: 官方技术白皮书 / 架构文档的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

For AI agents: a machine-readable documentation index is available at [https://docs.starrocks.io/llms.txt](https://docs.starrocks.io/llms.txt). Every documentation page is also available as Markdown by appending ".md" to its URL.
- - [Skip to main content](#__docusaurus_skipToContent_fallback)
🎉️ [NEXT QUERY is coming November 4th. Join us online!](https://nextquery.phoenixdata.ai/?utm_source=website&utm_medium=website&utm_campaign=FY26_PHX_OEV_NEXT_QUERY_2026&utm_content=starrocks-doc) 🎉️
[StarRocks](https://www.starrocks.io/)[Docs](/docs/introduction/) [Latest-4.1](/docs/introduction/Architecture/) - [Latest-4.1](/docs/introduction/Architecture/)
- [4.0](/docs/4.0/introduction/Architecture/)
- [Stable-3.5](/docs/3.5/introduction/Architecture/)
-
- Archived versions
- [3.4](/docs/3.4/introduction/)
- [3.3](/docs/3.3/introduction/)
- [3.2](/docs/3.2/introduction/)
- [3.1](/docs/3.1/introduction/)
[English](#) - [English](/docs/introduction/Architecture/)
- [中文](/zh/docs/introduction/Architecture/)
- [日本語](/ja/docs/introduction/Architecture/)
[NEXT QUERY 2026](https://nextquery.phoenixdata.ai/?utm_source=website&utm_medium=website&utm_campaign=FY26_PHX_OEV_NEXT_QUERY_2026&utm_content=starrocks-doc)[Release Notes](/releasenotes/release-4.1/)[](https://github.com/StarRocks/starrocks) [Community](#) - [Slack](https://docs.starrocks.io/join/)
[Privacy policy](https://www.starrocks.io/product/privacy-policy)
Search
- [Introduction to StarRocks](/docs/introduction/)
- [Architecture](/docs/introduction/Architecture/)
- [Database Features](/docs/introduction/Features/)
- [Community Chat](/docs/introduction/slack/)
- [Quick Start](/docs/quick_start/)
- [Best Practices](/docs/best_practices/)
- [Deployment](/docs/deployment/)
- [Table Design](/docs/table_design/)
- [Data Loading](/docs/loading/)
- [Data Unloading](/docs/unloading/)
- [Data Lakes](/docs/data_source/)
- [Query Acceleration](/docs/using_starrocks/)
- [Integrations](/docs/integrations/)
- [Administration](/docs/administration/)
- [Reference](/docs/sql-reference/)
- [FAQ](/docs/faq/)
- [Benchmarks](/docs/benchmarking/)
- [Versions and Maturity](/docs/maturity/)
- [developers](/docs/developers/versions/)
- [Introduction to StarRocks](/docs/introduction/)
- Architecture
Version: Latest-4.1 On this page
Copy as Markdown - View as Markdown /docs/introduction/Architecture.md
- Open in Claude
- Open in ChatGPT
- Browse all docs as Markdown /llms.txt
# Architecture
StarRocks has a simple architecture. The entire system consists of only two types of components; frontends and backends. The frontend nodes are called FE s. There are two types of backend nodes, BE s, and CN s (Compute Nodes). BEs are deployed when local storage for data is used, and CNs are deployed when data is stored on object storage or HDFS. StarRocks does not rely on any external components, simplifying deployment and maintenance. Nodes can be horizontally scaled without service downtime. In addition, StarRocks has a replica mechanism for metadata and service data, which increases data reliability and efficiently prevents single points of failure (SPOFs).
StarRocks is compatible with MySQL protocols and supports standard SQL. Users can easily connect to StarRocks from MySQL clients to gain instant and valuable insights.
## Architecture choices[​](#architecture-choices)
StarRocks supports shared-nothing (Each BE has a portion of the data on its local storage) and shared-data (all data on object storage or HDFS and each CN has only cache on local storage). You can decide where the data is stored based on your needs.
### Shared-nothing[​](#shared-nothing)
Local storage provides improved query latency for real-time queries.
As a typical massively parallel processing (MPP) database StarRocks supports the shared-nothing architecture. In this architecture, BEs are responsible for both data storage and computation. Direct access to local data on the BE mode allows for local computation, avoiding data transfer and data copying, and providing ultra-fast query and analytics performance. This architecture supports multi-replica data storage, enhancing the cluster's ability to handle high concurrency queries and ensuring data reliability. It is well-suited for scenarios that pursue optimal query performance.
#### Nodes[​](#nodes)
In the shared-nothing architecture, StarRocks consists of two types of nodes: FEs and BEs.
- FEs are responsible for metadata management and constructing execution plans.
- BEs execute query plans and store data. BEs utilize local storage to accelerate queries and the multi-replica mechanism to ensure high data availability.
##### FE[​](#fe)
FEs are responsible for metadata management, client connection management, query planning, and query scheduling. Each FE uses BDB JE (Berkeley DB Java Edition) to store and maintain a complete copy of the metadata in its memory, ensuring consistent services across all FEs. FEs can work as the leader, followers, and observers. If the leader node crashes, with followers electing a leader based on the Raft protocol.
FE Role Metadata management Leader election
Leader The leader FE reads and writes metadata. Follower and observer FEs can only read metadata. They route metadata write requests to the leader FE. The leader FE updates the metadata and then uses the Raft protocol to synchronize the metadata changes to the follower and observer FEs. Data writes are considered successful only after the metadata changes are synchronized to more than half of the follower FEs. The leader FE, technically speaking, is also a follower node and is elected from follower FEs. To perform leader election, more than half of the follower FEs in the cluster must be active. When the leader FE fails, follower FEs will start another round of leader election.
Follower Followers can only read metadata. They synchronize and replay logs from the leader FE to update metadata. Followers participate in leader election, which requires more than half of the followers in the cluster be active.
Observer Observers synchronize and replay logs from the leader FE to update metadata. Observers are mainly used to increase the query concurrency of the cluster. Observers do not participate in leader election and therefore, will not add leader selection pressure to the cluster.
##### BE[​](#be)
BEs are responsible for data storage and SQL execution.
-
Data storage: BEs have equivalent data storage capabilities. FEs distribute data to BEs based on predefined rules. BEs transform the ingested data, write the data into the required format, and generate indexes for the data.
-
SQL execution: FEs parse each SQL query into a logical execution plan according to the semantics of the query, and then transform the logical plan into physical execution plans that can be executed on BEs. BEs that store the destination data execute the query. This eliminates the need for data transmission and copy, achieving high query performance.
### Shared-data[​](#shared-data)
Object storage and HDFS provide cost, reliability, and scalability benefits. In addition to the scalability of storage, CN nodes can be added and removed without the need to rebalance data since storage and compute are separate.
In the shared-data architecture, BEs are replaced with "compute nodes (CNs)" which are responsible only for data compute tasks and caching hot data. Data is stored in low-cost and reliable remote storage systems such as Amazon S3, Google Cloud Storage, Azure Blob Storage, MinIO, etc. When the cache is hit, query performance is comparable to that of the shared-nothing architecture. CN nodes can be added or removed on demand within seconds. This architecture reduces storage cost, ensures better resource isolation, and high elasticity and scalability.
The shared-data architecture maintains as simple an architecture as its shared-nothing counterpart. It consists of only two types of nodes: FE and CN. The only difference is users have to provision backend object storage.
#### Nodes[​](#nodes-1)
FEs in the shared-data architecture provide the same functions as in the shared-nothing architecture.
BEs are replaced with CNs (Compute Nodes), and the storage function is offloaded to object storage or HDFS. CNs are stateless compute nodes that perform all the functions of BEs, except for the storage of data.
#### Storage[​](#storage)
StarRocks shared-data clusters support two storage solutions: object storage (for example, AWS S3, Google GCS, Azure Blob Storage, or MinIO) and HDFS.
In a shared-data cluster, the data file format remains consistent with that of a shared-nothing cluster (featuring coupled storage and compute). Data is organized into segment files, and various indexing technologies are reused in cloud-native tables, which are tables used specifically in shared-data clusters.
#### Cache[​](#cache)
StarRocks shared-data clusters decouple data storage and computation, allowing each to scale independently, thereby reducing costs and enhancing elasticity. However, this architecture can affect query performance.
To mitigate the impact, StarRocks establishes a multi-tiered data access system encompassing memory, local disk, and remote storage to better meet various business needs.
Queries against hot data scan the cache directly and then the local disk, while cold data needs to be loaded from the object storage into the local cache to accelerate subsequent queries. By keeping hot data close to compute units, StarRocks achieves truly high-performance computation and cost-effective storage. Moreover, access to cold data has been optimized with data prefetch strategies, effectively eliminating performance limits for queries.
Caching can be enabled when creating tables. If caching is enabled, data will be written to both the local disk and backend object storage. During queries, the CN nodes first read data from the local disk. If the data is not found, it will be retrieved from the backend object storage and simultaneously cached on the local disk.
## Feature Differences between Shared-nothing and Shared-data Clusters[​](#feature-differences-between-shared-nothing-and-shared-data-clusters)
This section lists the differences of features supported in shared-nothing and shared-data clusters.
### Real-time Analytics and Primary Key Tables[​](#real-time-analytics-and-primary-key-tables)
Feature Shared-nothing Shared-data
Conditional Update v2.5+ v3.1+
Partial Update Column mode v3.1 To be supported
Partial Update Row mode v2.3+ v3.1+
Partial update with Conditional Update v3.1+ v3.4.1+
Primary Key Index Persistence v2.3+ v3.2+
Decoupled ORDER BY columns from Primary Keys v3.0+ v3.1+
Rich UPDATE and DELETE syntax for Primary Key tables v3.0+ v3.1+
### Storage Engine[​](#storage-engine)
Feature Shared-nothing Shared-data
Fast Schema Evolution v3.2+ v4.0+
File Bundling Not applicable v4.0+
Inverted Index v3.3+ v4.1+
Manual Compaction v3.1+ v3.3+
Row Store v3.2+ To be supported
Adding/dropping STRUCT fields v3.3.2+ v3.3.5+
Vector index v3.4+ To be supported
### Data Distribution[​](#data-distribution)
Feature Shared-nothing Shared-data
Expression Partitioning v3.0+ v3.1.1+
List Partitioning v3.1+ v3.1.1+
Random Bucketing v3.1+ v3.2+
Random Bucketing Optimization (with Sub-partition) v3.2+ v3.2+
Unified Syntax for Multi-level Expression Partition v3.4+ v3.4+
Optimize Table: Change Bucketing v3.2+ v3.3+
Optimize Table: Change Bucketing Online v3.3.3+ Not applicable
Range-based Distribution v4.1+ v4.1+
### Query Performance[​](#query-performance)
Feature Shared-nothing Shared-data
Cross-node Data Cache Sharing Not applicable v3.5.1+
Generated Column v3.1+ v3.5+
Query Cache v2.5+ v3.4+
Rollup and Synchronous Materialized view v1.x+ v3.3+
### Disaster Recovery[​](#disaster-recovery)
Feature Shared-nothing Shared-data
Backup & Restore v1.x+ Not applicable
BE/CN Blacklist v3.3+ v4.0+
Cross-cluster Data Migration Tool v3.3+ Not applicable
Cluster Snapshot Not applicable v3.4.2+
### Security and Authentication[​](#security-and-authentication)
Feature Shared-nothing Shared-data
Kerberos Support on HDFS Not applicable v3.2+
## Learn by doing[​](#learn-by-doing)
Try the [Quick Starts](/docs/quick_start/) to get an overview of using StarRocks with realistic scenarios.
[Edit this page](https://github.com/StarRocks/starrocks/edit/main/docs/en/introduction/Architecture.md)
[Previous
What is StarRocks?](/docs/introduction/)[Next
Database Features](/docs/introduction/Features/)
- [Architecture choices](#architecture-choices) - [Shared-nothing](#shared-nothing)
- [Shared-data](#shared-data)
- [Feature Differences between Shared-nothing and Shared-data Clusters](#feature-differences-between-shared-nothing-and-shared-data-clusters) - [Real-time Analytics and Primary Key Tables](#real-time-analytics-and-primary-key-tables)
- [Storage Engine](#storage-engine)
- [Data Distribution](#data-distribution)
- [Query Performance](#query-performance)
- [Disaster Recovery](#disaster-recovery)
- [Security and Authentication](#security-and-authentication)
- [Learn by doing](#learn-by-doing)
- [StarRocks.io](https://www.starrocks.io/)
- [Privacy policy](https://www.starrocks.io/product/privacy-policy)
Docs built with Docusaurus.
StarRocks Assistant
×
AI generated answers are based on docs and other sources. Please test answers in non-production environments.
Send Reset