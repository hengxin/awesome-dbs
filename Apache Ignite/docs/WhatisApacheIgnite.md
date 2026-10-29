# What is Apache Ignite?

- 来源: https://apacheignite.readme.io/docs
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

For AI agents: the docs index is at https://apacheignite.readme.io/llms.txt. Append .md to any documentation page URL to get its markdown version.
[Jump to Content](#content)
[](https://ignite.apache.org/)[Java*](https://apacheignite.readme.io/docs/)[C#/.NET](https://apacheignite-net.readme.io/docs/)[C++](https://apacheignite-cpp.readme.io)[SQL](https://apacheignite-sql.readme.io/)[Integrations](https://apacheignite-mix.readme.io/docs)[Ignite for Spark](https://apacheignite-fs.readme.io/docs)[Tools](https://apacheignite-tools.readme.io/docs)
[Home](/docs) v2.7.0 v2.8 [Java*](https://apacheignite.readme.io/docs/)[C#/.NET](https://apacheignite-net.readme.io/docs/)[C++](https://apacheignite-cpp.readme.io)[SQL](https://apacheignite-sql.readme.io/)[Integrations](https://apacheignite-mix.readme.io/docs)[Ignite for Spark](https://apacheignite-fs.readme.io/docs)[Tools](https://apacheignite-tools.readme.io/docs)[Log In](/login?redirect_uri=/docs/what-is-ignite)[Javadoc](https://ignite.apache.org/releases/latest/javadoc/index.html)[Examples](https://github.com/apache/ignite/tree/master/examples)[Ask a Question](https://ignite.apache.org/community/resources.html#ask)[](https://ignite.apache.org/)
Home
[Log In](/login?redirect_uri=/docs/what-is-ignite)[Javadoc](https://ignite.apache.org/releases/latest/javadoc/index.html)[Examples](https://github.com/apache/ignite/tree/master/examples)[Ask a Question](https://ignite.apache.org/community/resources.html#ask)
v2.8
Home
What is Apache Ignite? What is Apache Ignite?
## Basic Concepts
- [What is Apache Ignite?](/docs/what-is-ignite)
- [Getting Started](/docs/getting-started)
- [Exception Handling](/docs/exception-handling)
- [Asynchronous Support](/docs/async-support)
- [Thread Pools](/docs/thread-pools)
- [FAQ](/docs/faq)
- [Ignite Life Cycle](/docs/ignite-life-cycle)
- [Logging](/docs/logging)
- [Ignite Facts](/docs/ignite-facts)
- [Resource Injection](/docs/resource-injection)
- [Binary Marshaller](/docs/binary-marshaller)
## Installation and Deployment
- [Installing With ZIP Archive](/docs/installing-with-zip-archive)
- [Google Compute Deployment](/docs/google-compute-deployment)
- [Mesos Deployment](/docs/mesos-deployment)
- [VMWare Deployment](/docs/vmware-deployment)
- [AWS Deployment](/docs/aws-deployment)
- [RPM and DEB Setup](/docs/rpm-and-deb-setup)
- [Maven Setup](/docs/maven-setup)
- [Installation and Deployment](/docs/deployment)
- [YARN Deployment](/docs/yarn-deployment)
- [Docker Deployment](/docs/docker-deployment)
## Kubernetes Deployments
- [Generic Configuration](/docs/generic-configuration) - [Kubernetes IP Finder](/docs/kubernetes-ip-finder)
- [Stateless Deployment](/docs/stateless-deployment)
- [Stateful Deployment](/docs/stateful-deployment)
- [Ignite Service](/docs/ignite-service)
- [RBAC Authorization](/docs/rbac-authorization)
- [Google Cloud Deployment](/docs/google-cloud-deployment)
- [Kubernetes Deployment](/docs/kubernetes-deployment)
- [AWS EKS Deployment](/docs/amazon-web-services-eks-deployment)
- [Microsoft Azure Deployment](/docs/microsoft-azure-deployment)
## Multi-Tier Storage
- [Memory Defragmentation](/docs/memory-defragmentation)
- [Durable Memory](/docs/durable-memory)
- [Memory Configuration](/docs/memory-configuration)
- [Memory Architecture](/docs/memory-architecture)
- [Expiry Policies](/docs/expiry-policies)
- [Eviction Policies](/docs/evictions)
## Persistence
- [Ignite Persistence](/docs/distributed-persistent-store)
- [Disk Compression](/docs/disk-page-compression)
- [3rd Party Persistence](/docs/3rd-party-store)
- [Swap Space](/docs/swap-space)
- [Checkpointing](/docs/persistence-checkpointing)
- [Baseline Topology](/docs/baseline-topology)
- [Write-Ahead Log](/docs/write-ahead-log)
## Clustering
- [Cluster APIs](/docs/cluster)
- [Network Configuration](/docs/network-config)
- [Zero Deployment](/docs/zero-deployment)
- [Leader Election](/docs/leader-election)
- [Cluster Discovery](/docs/cluster-discovery) - [TCP/IP Discovery](/docs/tcpip-discovery)
- [ZooKeeper Discovery](/docs/zookeeper-discovery)
- [Deployment Modes](/docs/deployment-modes)
- [Clients and Servers](/docs/clients-vs-servers)
- [Clustering](/docs/clustering)
- [Cluster Groups](/docs/cluster-groups)
## Key-Value Data Grid
- [Affinity Collocation](/docs/affinity-collocation)
- [Locks](/docs/distributed-locks)
- [Web Session Clustering](https://apacheignite-mix.readme.io/docs/web-session-clustering)
- [JCache and Beyond](/docs/jcache)
- [Cache Configuration](/docs/cache-configuration) - [Primary & Backup Copies](/docs/primary-and-backup-copies)
- [Cache Template](/docs/cache-template)
- [Partitioning and Replication](/docs/cache-modes)
- [Partition Loss Policies](/docs/partition-loss-policies)
- [Cache Groups](/docs/cache-groups)
- [Hibernate L2 Cache](https://apacheignite-mix.readme.io/docs/hibernate-l2-cache)
- [Read Repair](/docs/read-repair)
- [Topology Validation](/docs/topology-validation)
- [Near Caches](/docs/near-caches)
- [Data Grid](/docs/data-grid)
- [Cache Queries](/docs/cache-queries)
- [Transactions](/docs/transactions) - [Concurrency Modes and Isolation Levels](/docs/concurrency-modes-and-isolation-levels)
- [Multiversion Concurrency Control](/docs/multiversion-concurrency-control)
- [Data Rebalancing](/docs/rebalancing)
- [Continuous Queries](/docs/continuous-queries)
## Compute Grid
- [Executor Service](/docs/executor-service)
- [Collocate Compute and Data](/docs/collocate-compute-and-data)
- [Checkpointing](/docs/checkpointing)
- [Fault Tolerance](/docs/fault-tolerance)
- [Distributed Closures](/docs/distributed-closures)
- [Continuous Mapping](/docs/continuous-mapping)
- [AOP-Based Grid Enabling](/docs/aop-based-grid-enabling)
- [Ignite Compute Grid](/docs/compute-grid)
- [Cron-Based Scheduling](/docs/cron-based-scheduling)
- [Job Scheduling](/docs/job-scheduling)
- [MapReduce & ForkJoin](/docs/compute-tasks)
- [Load Balancing](/docs/load-balancing)
- [Task Deployment](/docs/deployment-spi)
- [Per-Node Shared State](/docs/node-local-map)
## Machine Learning
- [Ensemble Methods](/docs/ensemble-methods) - [Random Forest](/docs/random-forest)
- [Gradient Boosting](/docs/gradient-boosting)
- [Bagging](/docs/bagging)
- [Stacking](/docs/stacking)
- [Preprocessing](/docs/preprocessing)
- [Recommendation Systems](/docs/recommendation-systems)
- [Updating Trained Models](/docs/model-updating)
- [Multiclass classification](/docs/multiclass-classification)
- [Partition Based Dataset](/docs/ml-partition-based-dataset)
- [Regression](/docs/regression) - [Decision Trees Regression](/docs/decision-trees-regression)
- [Linear Regression](/docs/ols-multiple-linear-regression)
- [k-NN Regression](/docs/knn-regression)
- [Binary Classification](/docs/classification) - [k-NN Classification](/docs/knn-classification)
- [Logistic Regression](/docs/logistic-regression)
- [Decision Trees](/docs/decision-trees)
- [Linear SVM (Support Vector Machine)](/docs/linear-svm-support-vector-machine)
- [ANN (Approximate Nearest Neighbor)](/docs/ann-approximate-nearest-neighbor)
- [Multilayer perceptron](/docs/multilayer-perceptron)
- [Naive Bayes](/docs/naive-bayes)
- [Machine Learning](/docs/machine-learning)
- [Importing Model](/docs/model-importing) - [Import Model from Apache Spark](/docs/model-import-from-apache-spark)
- [Import Model from XGBoost](/docs/model-import-from-gxboost)
- [Model Selection](/docs/evaluation) - [Pipelines API](/docs/pipeline-api)
- [Evaluator](/docs/evaluator)
- [Cross-Validation](/docs/cross-validation)
- [Split the dataset on test and train datasets](/docs/split-the-dataset-on-test-and-train-datasets)
- [Hyper-parameter tuning](/docs/hyper-parameter-tuning)
- [Clustering](/docs/clustering-1) - [K-Means Clustering](/docs/k-means-clustering)
- [Gaussian mixture (GMM)](/docs/gaussian-mixture-gmm)
## Messaging - Events
- [Automatic Batching](/docs/automatic-batching)
- [Local and Remote Events](/docs/events)
- [Topic Based Messaging](/docs/messaging)
## Plugins
- [Plugins](/docs/plugins)
## SQL
- [Distributed SQL](/docs/distributed-sql)
## Data Loading - Streaming
- [Integrations](/docs/integrations)
- [Data Loading](/docs/data-loading)
- [Data Streamers](/docs/data-streamers)
- [Data Loading & Streaming](/docs/streaming-cep)
## Metrics
- [Metrics](/docs/new-metrics) - [cache.{cache_name}.{near}](/docs/cachecache_namenear-1)
- [cacheGroups.{group_name}](/docs/cachegroupsgroup_name)
- [io.statistics.hashIndexes.{cache_name}.{index_name}](/docs/iostatisticshashindexes)
- [io.communication](/docs/iocommunication)
- [io.statistics.cacheGroups.{group_name}](/docs/iostatisticscachegroups)
- [sys](/docs/sys)
- [io.dataregion.{data_region_name}](/docs/iodataregiondata_region_name)
- [tx](/docs/tx)
- [io.statistics.sortedIndexes.{cache_name}.{index_name}](/docs/iostatisticssortedindexes)
- [io.datastorage](/docs/iodatastorage)
- [pme](/docs/pme)
- [compute.jobs](/docs/computejobs)
- [threadPools.{thread_pool_name}](/docs/threadpoolsthread_pool_name)
- [Cache Metrics](/docs/cache-metrics)
- [Memory Metrics](/docs/memory-metrics)
- [System views](/docs/system-views) - [BASELINE_NODES](/docs/baseline_nodes)
- [TRANSACTIONS](/docs/transactions-1)
- [TABLES](/docs/tables)
- [SCAN_QUERIES](/docs/scan_queries)
- [SCHEMAS](/docs/schemas)
- [SQL_QUERIES_HISTORY](/docs/sql_queries_history)
- [PAGE_LISTS](/docs/page-lists)
- [CACHE_GROUPS](/docs/cache_groups)
- [VIEWS](/docs/views)
- [NODE_ATTRIBUTES](/docs/node_attributes)
- [STRIPED_THREADPOOL_QUEUE](/docs/striped_threadpool_queue)
- [VIEW_COLUMNS](/docs/view_columns)
- [CLIENT_CONNECTIONS](/docs/client_connections)
- [INDEXES](/docs/indexes-1)
- [NODES](/docs/nodes)
- [DATASTREAM_THREADPOOL_QUEUE](/docs/datastream_threadpool_queue)
- [NODE_METRICS](/docs/node_metrics)
- [TASKS](/docs/tasks)
- [CACHES](/docs/caches)
- [SERVICES](/docs/services)
- [CONTINUOUS_QUERIES](/docs/continuous_queries)
- [TABLE_COLUMNS](/docs/table_columns)
- [SQL_QUERIES](/docs/sql_queries)
## Security
- [Transparent Data Encryption](/docs/transparent-data-encryption)
- [Advanced Security](/docs/advanced-security)
- [Securing Data Deserialization](/docs/securing-data-deserialization)
- [SSL\TLS](/docs/ssltls)
## Tests and Benchmarking
- [Benchmarking](/docs/perfomance-benchmarking)
## Production Readiness
- [Consistency Check Facilities](/docs/consistency-check-facilities)
- [Critical Failures Handling](/docs/critical-failures-handling)
- [Virtual Environments](/docs/virtual-environments)
- [Garbage Collection Tuning](/docs/jvm-and-system-tuning)
- [Durable Memory Tuning](/docs/durable-memory-tuning)
- [Performance Tips](/docs/performance-tips)
- [Capacity Planning](/docs/capacity-planning)
- [Preparing for Production](/docs/preparing-for-production)
## Platforms - Protocols
- [Overview](/docs/overview)
- [Ignite.C++](https://apacheignite-cpp.readme.io)
- [Memcached](/docs/memcached-support)
- [Ignite.NET](https://apacheignite-net.readme.io/docs/)
- [Redis](/docs/redis)
- [PHP](https://apacheignite-mix.readme.io/docs/php-pdo)
- [REST API](/docs/rest-api)
## Distributed Data Structures
- [Data Structures](/docs/data-structures)
- [ID Generator](/docs/id-generator)
- [Semaphore](/docs/distributed-semaphore)
- [CountDownLatch](/docs/countdownlatch)
- [Atomic Types](/docs/atomic-types)
- [Queue and Set](/docs/queue-and-set)
## Migration Guides
- [Apache Ignite 2.0](/docs/apache-ignite-20)
## Service Grid
- [Cluster Singletons](/docs/cluster-singletons)
- [Service Example](/docs/service-example)
- [Service Grid](/docs/service-grid)
- [Service Configuration](/docs/service-configuration)
## Thin Clients
- [C++ Thin Client](https://apacheignite-cpp.readme.io/docs/thin-client)
- [Java Thin Client](/docs/java-thin-client) - [Security](/docs/java-thin-client-security-27)
- [SQL](/docs/java-thin-client-sql)
- [Key-Value](/docs/java-thin-client-key-value)
- [Initialization and Configuration](/docs/java-thin-client-initialization-and-configuration)
- [Binary Types](/docs/java-thin-client-binary-types)
- [Binary Client Protocol](/docs/binary-client-protocol) - [Data Format](/docs/binary-client-protocol-data-format)
- [SQL and Scan Queries](/docs/binary-client-protocol-sql-operations)
- [Binary Types Metadata](/docs/binary-client-protocol-binary-type-operations)
- [Cache Configuration](/docs/binary-client-protocol-cache-configuration-operations)
- [Key-Value Queries](/docs/binary-client-protocol-key-value-operations)
- [PHP Thin Client](/docs/php-thin-client) - [SQL](/docs/php-thin-client-sql)
- [Security](/docs/php-thin-client-security)
- [Binary Types](/docs/php-thin-client-binary-types)
- [Initialization and Configuration](/docs/php-thin-client-initialization-and-configuration)
- [Key-Value](/docs/php-thin-client-key-value)
- [Python Thin Client](/docs/python-thin-client) - [Binary Types](/docs/python-thin-client-binary-types)
- [SQL](/docs/python-thin-client-sql)
- [Security](/docs/python-thin-client-security)
- [Key-Value](/docs/python-thin-client-key-value)
- [Initialization and Configuration](/docs/python-thin-client-initialization-and-configuration)
- [Thin Clients](/docs/thin-clients)
- [Node.JS Thin Client](/docs/nodejs-thin-client) - [Security](/docs/nodejs-thin-client-security)
- [Key-Value](/docs/nodejs-thin-client-key-value)
- [Binary Types](/docs/nodejs-thin-client-binary-types)
- [Initialization and Configuration](/docs/nodejs-thin-client-initialization-and-configuration)
- [SQL](/docs/nodejs-thin-client-sql)
- [.NET Thin Client](https://apacheignite-net.readme.io/docs/thin-client)
## Legal
- [Apache License](/docs/license)
- [Copyright](/docs/copyright)
Powered by  [](https://readme.com?ref_src=hub&project=apacheignite)
- Basic Concepts
# What is Apache Ignite?
distributed database for in-memory speed and high-performance computing.
❗️
###
This is a legacy Apache Ignite documentation
[](#this-is-a-legacy-apache-ignite-documentation)
The new documentation is hosted here: [https://ignite.apache.org/docs/latest/](https://ignite.apache.org/docs/latest/)
##
Durable Memory
[](#durable-memory)
Ignite's durable memory component treats RAM not just as a caching layer but as a complete fully functional storage layer. This means that users can turn the persistence on and off as needed. If persistence is turned off, then Ignite can act as a distributed in-memory database or in-memory data grid , depending on whether you prefer to use SQL or key-value APIs. If persistence is turned on, then Ignite becomes a distributed, horizontally scalable database that guarantees full data consistency and is resilient to full cluster failures.
[Read More](https://apacheignite.readme.io/docs/durable-memory)
##
Ignite Persistence
[](#ignite-persistence)
Ignite Native Persistence is a distributed, ACID, and SQL-compliant disk store that transparently integrates with Ignite's Durable Memory as an optional disk layer storing data and indexes on SSD, Flash, 3D XPoint, and other types of non-volatile storages.
With Ignite Persistence enabled, you no longer need to keep all the data and indexes in memory or warm it up after a node or cluster restart because the Durable Memory is tightly coupled with persistence and treats it as a secondary memory tier. This implies that if a subset of data or an index is missing in RAM, the Durable Memory will take it from the disk.
[Read More](https://apacheignite.readme.io/docs/distributed-persistent-store)
##
ACID Compliance
[](#acid-compliance)
Data stored in Ignite is ACID-compliant both in memory and on disk, making Ignite a strongly consistent system. Ignite transactions work across the network and can span multiple servers.
[Read More](https://apacheignite.readme.io/docs/transactions)
##
Complete SQL Support
[](#complete-sql-support)
Ignite provides full support for SQL, DDL and DML, allowing users to interact with Ignite using pure SQL without writing any code. This means that users can create tables and indexes as well as insert, update, and query data using only SQL. Having such complete SQL support makes Ignite a one-of-a-kind distributed SQL database .
[Read More](https://apacheignite.readme.io/docs/distributed-sql)
##
Key-Value
[](#key-value)
The in-memory data grid component in Ignite is a fully transactional distributed key-value store that can scale horizontally across 100s of servers in the cluster. When persistence is enabled, Ignite can also store more data than fits in memory and survive full cluster restarts.
[Read More](https://apacheignite.readme.io/docs/data-grid)
##
Co-located Processing
[](#co-located-processing)
Most traditional databases work in a client-server fashion, meaning that data must be brought to the client side for processing. This approach requires lots of data movement from servers to clients and generally does not scale. Ignite, on the other hand, allows for sending light-weight computations to the data, i.e. collocating computations with data. As a result, Ignite scales better and minimizes data movement.
[Read More](https://apacheignite.readme.io/docs/collocate-compute-and-data)
##
Scalability and Durability
[](#scalability-and-durability)
Ignite is an elastic, horizontally scalable distributed system that supports adding and removing cluster nodes on demand. Ignite also allows for storing multiple copies of the data, making it resilient to partial cluster failures. If the persistence is enabled, then data stored in Ignite will also survive full cluster failures. Cluster restarts in Ignite can be very fast, as the data becomes operational instantaneously directly from disk. As a result, the data does not need to be preloaded in-memory to begin processing, and Ignite caches will lazily warm up resuming the in memory performance.
[Read More](https://apacheignite.readme.io/docs/clustering)
Updated over 1 year ago
[Getting Started](/docs/getting-started) Copy Page
- - [Durable Memory](#durable-memory)
- [Ignite Persistence](#ignite-persistence)
- [ACID Compliance](#acid-compliance)
- [Complete SQL Support](#complete-sql-support)
- [Key-Value](#key-value)
- [Co-located Processing](#co-located-processing)
- [Scalability and Durability](#scalability-and-durability)