# Apache Ignite Documentation

- 来源: https://ignite.apache.org/docs/latest/index.html
- 归档时间: 2026-10-29
- 说明: 官方技术白皮书 / 架构文档的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

[](/)
2.18.0
- [APIs](#)
- [Java](/releases/ignite2/2.18.0/javadoc/index.html)
- [C#/.NET](/releases/ignite2/2.18.0/dotnetdoc/api/)
- [C++](/releases/ignite2/2.18.0/cppdoc/index.html)
- [Examples](#)
- [Java](https://github.com/apache/ignite/tree/master/examples)
- [C#/.NET](https://github.com/apache/ignite/tree/master/modules/platforms/dotnet/examples)
- [C++](https://github.com/apache/ignite/tree/master/modules/platforms/cpp/examples)
- [Python](https://github.com/apache/ignite/tree/master/modules/platforms/python/examples)
- [NodeJS](https://github.com/apache/ignite/tree/master/modules/platforms/nodejs/examples)
- [PHP](https://github.com/apache/ignite/tree/master/modules/platforms/php/examples)
[Ignite 3](https://ignite.apache.org/docs/ignite3/latest/)
- [▼](#)
- [English](/docs/ignite2/latest/)
- [Chinese](https://www.ignite-service.cn/doc/java/)
⋮
-
-
[Documentation Overview](/docs/ignite2/latest/)
-
Quick Start Guides
-
[Java](/docs/ignite2/latest/quick-start/java)
-
[.NET/C#](/docs/ignite2/latest/quick-start/dotnet)
-
[C++](/docs/ignite2/latest/quick-start/cpp)
-
[Python](/docs/ignite2/latest/quick-start/python)
-
[Node.JS](/docs/ignite2/latest/quick-start/nodejs)
-
[SQL](/docs/ignite2/latest/quick-start/sql)
-
[PHP](/docs/ignite2/latest/quick-start/php)
-
[REST API](/docs/ignite2/latest/quick-start/restapi)
-
Installation
-
[Installing Using ZIP Archive](/docs/ignite2/latest/installation/installing-using-zip)
-
[Installing Using Docker](/docs/ignite2/latest/installation/installing-using-docker)
-
[Installing DEB or RPM package](/docs/ignite2/latest/installation/deb-rpm)
-
Kubernetes
- [Amazon EKS](/docs/ignite2/latest/installation/kubernetes/amazon-eks-deployment)
- [Azure Kubernetes Service](/docs/ignite2/latest/installation/kubernetes/azure-deployment)
- [Google Kubernetes Engine](/docs/ignite2/latest/installation/kubernetes/gke-deployment)
-
[VMWare](/docs/ignite2/latest/installation/vmware-installation)
-
[Version Upgrade](/docs/ignite2/latest/installation/upgrades)
-
Setting Up
-
[Understanding Configuration](/docs/ignite2/latest/understanding-configuration)
-
[Setting Up](/docs/ignite2/latest/setup)
-
[Configuring Logging](/docs/ignite2/latest/logging)
-
[Resources Injection](/docs/ignite2/latest/resources-injection)
-
[Starting and Stopping Nodes](/docs/ignite2/latest/starting-nodes)
-
Clustering
-
[Overview](/docs/ignite2/latest/clustering/clustering)
-
[TCP/IP Discovery](/docs/ignite2/latest/clustering/tcp-ip-discovery)
-
[ZooKeeper Discovery](/docs/ignite2/latest/clustering/zookeeper-discovery)
-
[Discovery in the Cloud](/docs/ignite2/latest/clustering/discovery-in-the-cloud)
-
[Network Configuration](/docs/ignite2/latest/clustering/network-configuration)
-
[Connecting Client Nodes](/docs/ignite2/latest/clustering/connect-client-nodes)
-
[Baseline Topology](/docs/ignite2/latest/clustering/baseline-topology)
-
[Running Client Nodes Behind NAT](/docs/ignite2/latest/clustering/running-client-nodes-behind-nat)
-
Thin Clients
-
[Thin Clients Overview](/docs/ignite2/latest/thin-clients/getting-started-with-thin-clients)
-
[Java Thin Client](/docs/ignite2/latest/thin-clients/java-thin-client)
-
[.NET Thin Client](/docs/ignite2/latest/thin-clients/dotnet-thin-client)
-
[C++ Thin Client](/docs/ignite2/latest/thin-clients/cpp-thin-client)
-
[Python Thin Client](/docs/ignite2/latest/thin-clients/python-thin-client)
-
[PHP Thin Client](/docs/ignite2/latest/thin-clients/php-thin-client)
-
[Node.js Thin Client](/docs/ignite2/latest/thin-clients/nodejs-thin-client)
-
Binary Client Protocol
- [Binary Client Protocol](/docs/ignite2/latest/binary-client-protocol/binary-client-protocol)
- [Data Format](/docs/ignite2/latest/binary-client-protocol/data-format)
- [Key-Value Queries](/docs/ignite2/latest/binary-client-protocol/key-value-queries)
- [SQL and Scan Queries](/docs/ignite2/latest/binary-client-protocol/sql-and-scan-queries)
- [Binary Types Metadata](/docs/ignite2/latest/binary-client-protocol/binary-type-metadata)
- [Cache Configuration](/docs/ignite2/latest/binary-client-protocol/cache-configuration)
-
Data Modeling
-
[Introduction](/docs/ignite2/latest/data-modeling/data-modeling)
-
[Data Partitioning](/docs/ignite2/latest/data-modeling/data-partitioning)
-
[Affinity Colocation](/docs/ignite2/latest/data-modeling/affinity-collocation)
-
[Binary Marshaller](/docs/ignite2/latest/data-modeling/binary-marshaller)
-
Configuring Memory
-
[Memory Architecture](/docs/ignite2/latest/memory-architecture)
-
[Configuring Data Regions](/docs/ignite2/latest/memory-configuration/data-regions)
-
[Eviction Policies](/docs/ignite2/latest/memory-configuration/eviction-policies)
-
[Replacement Policies](/docs/ignite2/latest/memory-configuration/replacement-policies)
-
Configuring Persistence
-
[Ignite Persistence](/docs/ignite2/latest/persistence/native-persistence)
-
[External Storage](/docs/ignite2/latest/persistence/external-storage)
-
[Swapping](/docs/ignite2/latest/persistence/swap)
-
[Implementing Custom Cache Store](/docs/ignite2/latest/persistence/custom-cache-store)
-
[Configuring Snapshot Directory](/docs/ignite2/latest/persistence/snapshot-directory)
-
[Disk Compression](/docs/ignite2/latest/persistence/disk-compression)
-
[Tuning Persistence](/docs/ignite2/latest/persistence/persistence-tuning)
-
[Change Data Capture](/docs/ignite2/latest/persistence/change-data-capture)
-
[Cluster Snapshots](/docs/ignite2/latest/snapshots/snapshots)
-
Configuring Caches
-
[Cache Configuration](/docs/ignite2/latest/configuring-caches/configuration-overview)
-
[Configuring Partition Backups](/docs/ignite2/latest/configuring-caches/configuring-backups)
-
[Partition Loss Policy](/docs/ignite2/latest/configuring-caches/partition-loss-policy)
-
[Atomicity Modes](/docs/ignite2/latest/configuring-caches/atomicity-modes)
-
[Expiry Policy](/docs/ignite2/latest/configuring-caches/expiry-policies)
-
[On-Heap Caching](/docs/ignite2/latest/configuring-caches/on-heap-caching)
-
[Cache Groups](/docs/ignite2/latest/configuring-caches/cache-groups)
-
[Near Caches](/docs/ignite2/latest/configuring-caches/near-cache)
-
[Data Rebalancing](/docs/ignite2/latest/data-rebalancing)
-
[Data Streaming](/docs/ignite2/latest/data-streaming)
-
Using Key-Value API
-
[Basic Cache Operations](/docs/ignite2/latest/key-value-api/basic-cache-operations)
-
[Working with Binary Objects](/docs/ignite2/latest/key-value-api/binary-objects)
-
[Using Cache Queries](/docs/ignite2/latest/key-value-api/using-cache-queries)
-
[Read Repair](/docs/ignite2/latest/key-value-api/read-repair)
-
[Performing Transactions](/docs/ignite2/latest/key-value-api/transactions)
-
Working with SQL
-
[Introduction](/docs/ignite2/latest/SQL/sql-introduction)
-
[Understanding Schemas](/docs/ignite2/latest/SQL/schemas)
-
[Defining Indexes](/docs/ignite2/latest/SQL/indexes)
-
[Using SQL API](/docs/ignite2/latest/SQL/sql-api)
-
[Distributed Joins](/docs/ignite2/latest/SQL/distributed-joins)
-
[Custom SQL Functions](/docs/ignite2/latest/SQL/custom-sql-func)
-
[JDBC Driver](/docs/ignite2/latest/SQL/JDBC/jdbc-driver)
-
[JDBC Client Driver](/docs/ignite2/latest/SQL/JDBC/jdbc-client-driver)
-
ODBC Driver
- [ODBC Driver](/docs/ignite2/latest/SQL/ODBC/odbc-driver)
- [Connection String and DSN](/docs/ignite2/latest/SQL/ODBC/connection-string-dsn)
- [Querying and Modifying Data](/docs/ignite2/latest/SQL/ODBC/querying-modifying-data)
- [Specification](/docs/ignite2/latest/SQL/ODBC/specification)
- [Data Types](/docs/ignite2/latest/SQL/ODBC/data-types)
- [Error Codes](/docs/ignite2/latest/SQL/ODBC/error-codes)
-
[SQL Statistics](/docs/ignite2/latest/SQL/sql-statistics)
-
[Calcite-based SQL Engine](/docs/ignite2/latest/SQL/sql-calcite)
-
SQL Reference
-
[SQL Conformance](/docs/ignite2/latest/sql-reference/sql-conformance)
-
[Data Definition Language (DDL)](/docs/ignite2/latest/sql-reference/ddl)
-
[Data Manipulation Language (DML)](/docs/ignite2/latest/sql-reference/dml)
-
[Transaction-aware Queries](/docs/ignite2/latest/SQL/sql-calcite#transaction-aware-queries)
-
[Operational Commands](/docs/ignite2/latest/sql-reference/operational-commands)
-
[Aggregate functions](/docs/ignite2/latest/sql-reference/aggregate-functions)
-
[Numeric Functions](/docs/ignite2/latest/sql-reference/numeric-functions)
-
[String Functions](/docs/ignite2/latest/sql-reference/string-functions)
-
[Data and Time Functions](/docs/ignite2/latest/sql-reference/date-time-functions)
-
[System Functions](/docs/ignite2/latest/sql-reference/system-functions)
-
[Data Types](/docs/ignite2/latest/sql-reference/data-types)
-
[Optimizer Hints](/docs/ignite2/latest/sql-reference/hints)
-
Distributed Computing
-
[Distributed Computing API](/docs/ignite2/latest/distributed-computing/distributed-computing)
-
[Cluster Groups](/docs/ignite2/latest/distributed-computing/cluster-groups)
-
[Executor Service](/docs/ignite2/latest/distributed-computing/executor-service)
-
[MapReduce API](/docs/ignite2/latest/distributed-computing/map-reduce)
-
[Load Balancing](/docs/ignite2/latest/distributed-computing/load-balancing)
-
[Fault Tolerance](/docs/ignite2/latest/distributed-computing/fault-tolerance)
-
[Job Scheduling](/docs/ignite2/latest/distributed-computing/job-scheduling)
-
[Colocating Computations with Data](/docs/ignite2/latest/distributed-computing/collocated-computations)
-
Code Deployment
-
[Deploying User Code](/docs/ignite2/latest/code-deployment/deploying-user-code)
-
[Peer Class Loading](/docs/ignite2/latest/code-deployment/peer-class-loading)
-
Machine Learning
-
[Machine Learning](/docs/ignite2/latest/machine-learning/machine-learning)
-
[Partition Based Dataset](/docs/ignite2/latest/machine-learning/partition-based-dataset)
-
[Updating Trained Models](/docs/ignite2/latest/machine-learning/updating-trained-models)
-
Binary Classification
- [Introduction](/docs/ignite2/latest/machine-learning/binary-classification/introduction)
- [Linear SVM (Support Vector Machine)](/docs/ignite2/latest/machine-learning/binary-classification/linear-svm)
- [Decision Trees](/docs/ignite2/latest/machine-learning/binary-classification/decision-trees)
- [Multilayer Perceptron](/docs/ignite2/latest/machine-learning/binary-classification/multilayer-perceptron)
- [Logistic Regression](/docs/ignite2/latest/machine-learning/binary-classification/logistic-regression)
- [k-NN Classification](/docs/ignite2/latest/machine-learning/binary-classification/knn-classification)
- [ANN (Approximate Nearest Neighbor)](/docs/ignite2/latest/machine-learning/binary-classification/ann)
- [Naive Bayes](/docs/ignite2/latest/machine-learning/binary-classification/naive-bayes)
-
Regression
- [Introduction](/docs/ignite2/latest/machine-learning/regression/introduction)
- [Linear Regression](/docs/ignite2/latest/machine-learning/regression/linear-regression)
- [Decision Trees Regression](/docs/ignite2/latest/machine-learning/regression/decision-trees-regression)
- [k-NN Regression](/docs/ignite2/latest/machine-learning/regression/knn-regression)
-
Clustering
- [Introduction](/docs/ignite2/latest/machine-learning/clustering/introduction)
- [K-Means Clustering](/docs/ignite2/latest/machine-learning/clustering/k-means-clustering)
- [Gaussian mixture (GMM)](/docs/ignite2/latest/machine-learning/clustering/gaussian-mixture)
-
[Preprocessing](/docs/ignite2/latest/machine-learning/preprocessing)
-
Model Selection
- [Introduction](/docs/ignite2/latest/machine-learning/model-selection/introduction)
- [Evaluator](/docs/ignite2/latest/machine-learning/model-selection/evaluator)
- [Split the dataset on test and train datasets](/docs/ignite2/latest/machine-learning/model-selection/split-the-dataset-on-test-and-train-datasets)
- [Hyper-parameter tuning](/docs/ignite2/latest/machine-learning/model-selection/hyper-parameter-tuning)
- [Pipeline API](/docs/ignite2/latest/machine-learning/model-selection/pipeline-api)
-
[Multiclass Classification](/docs/ignite2/latest/machine-learning/multiclass-classification)
-
Ensemble Methods
- [](/docs/ignite2/latest/machine-learning/ensemble-methods/introduction)
- [Stacking](/docs/ignite2/latest/machine-learning/ensemble-methods/stacking)
- [Bagging](/docs/ignite2/latest/machine-learning/ensemble-methods/bagging)
- [Random Forest](/docs/ignite2/latest/machine-learning/ensemble-methods/random-forest)
- [Gradient Boosting](/docs/ignite2/latest/machine-learning/ensemble-methods/gradient-boosting)
-
[Recommendation Systems](/docs/ignite2/latest/machine-learning/recommendation-systems)
-
Importing Model
- [Introduction](/docs/ignite2/latest/machine-learning/importing-model/introduction)
- [Import Model from XGBoost](/docs/ignite2/latest/machine-learning/importing-model/model-import-from-gxboost)
- [Import Model from Apache Spark](/docs/ignite2/latest/machine-learning/importing-model/model-import-from-apache-spark)
-
[Using Continuous Queries](/docs/ignite2/latest/key-value-api/continuous-queries)
-
[Using Ignite Services](/docs/ignite2/latest/services/services)
-
[Using Ignite Messaging](/docs/ignite2/latest/messaging)
-
Distributed Data Structures
-
[Queue and Set](/docs/ignite2/latest/data-structures/queue-and-set)
-
[Atomic Types](/docs/ignite2/latest/data-structures/atomic-types)
-
[CountDownLatch](/docs/ignite2/latest/data-structures/countdownlatch)
-
[Semaphore](/docs/ignite2/latest/data-structures/semaphore)
-
[ID Generator](/docs/ignite2/latest/data-structures/id-generator)
-
[Distributed Locks](/docs/ignite2/latest/distributed-locks)
-
[Session Context](/docs/ignite2/latest/session-context)
-
[REST API](/docs/ignite2/latest/restapi)
-
.NET Specific
-
[Configuration Options](/docs/ignite2/latest/net-specific/net-configuration-options)
-
[Deployment Options](/docs/ignite2/latest/net-specific/net-deployment-options)
-
[Standalone Nodes](/docs/ignite2/latest/net-specific/net-standalone-nodes)
-
[Asynchronous APIs](/docs/ignite2/latest/net-specific/net-async)
-
[Logging](/docs/ignite2/latest/net-specific/net-logging)
-
[LINQ](/docs/ignite2/latest/net-specific/net-linq)
-
[Java Services Execution](/docs/ignite2/latest/net-specific/net-java-services-execution)
-
[.NET Platform Cache](/docs/ignite2/latest/net-specific/net-platform-cache)
-
[Plugins](/docs/ignite2/latest/net-specific/net-plugins)
-
[Serialization](/docs/ignite2/latest/net-specific/net-serialization)
-
[Cross-Platform Support](/docs/ignite2/latest/net-specific/net-cross-platform-support)
-
[Platform Interoperability](/docs/ignite2/latest/net-specific/net-platform-interoperability)
-
[Remote Assembly Loading](/docs/ignite2/latest/net-specific/net-remote-assembly-loading)
-
[Troubleshooting](/docs/ignite2/latest/net-specific/net-troubleshooting)
-
Integrations
- [ASP.NET Output Caching](/docs/ignite2/latest/net-specific/asp-net-output-caching)
- [ASP.NET Session State Caching](/docs/ignite2/latest/net-specific/asp-net-session-state-caching)
- [Entity Framework 2nd Level Cache](/docs/ignite2/latest/net-specific/net-entity-framework-cache)
-
C++ Specific
-
[Serialization](/docs/ignite2/latest/cpp-specific/cpp-serialization)
-
[Platform Interoperability](/docs/ignite2/latest/cpp-specific/cpp-platform-interoperability)
-
[Objects Lifetime](/docs/ignite2/latest/cpp-specific/cpp-objects-lifetime)
-
Monitoring
-
[Introduction](/docs/ignite2/latest/monitoring-metrics/intro)
-
[Cluster ID and Tag](/docs/ignite2/latest/monitoring-metrics/cluster-id)
-
[Cluster States](/docs/ignite2/latest/monitoring-metrics/cluster-states)
-
Metrics System
- [Introduction](/docs/ignite2/latest/monitoring-metrics/new-metrics-system)
- [Configuring Metrics](/docs/ignite2/latest/monitoring-metrics/configuring-metrics)
- [Metrics](/docs/ignite2/latest/monitoring-metrics/new-metrics)
- [Custom Metrics](/docs/ignite2/latest/monitoring-metrics/custom-metrics)
-
[System Views](/docs/ignite2/latest/monitoring-metrics/system-views)
-
[Performance Statistics](/docs/ignite2/latest/monitoring-metrics/performance-statistics)
-
[Tracing](/docs/ignite2/latest/monitoring-metrics/tracing)
-
Working with Events
-
[Enabling and Listenting to Events](/docs/ignite2/latest/events/listening-to-events)
-
[Events](/docs/ignite2/latest/events/events)
-
Tools
-
[Control Script](/docs/ignite2/latest/tools/control-script)
-
[GridGain Control Center](/docs/ignite2/latest/tools/gg-control-center)
-
[Platform V Grid Center](/docs/ignite2/latest/tools/grid-center)
-
[SQLLine](/docs/ignite2/latest/tools/sqlline)
-
[Tableau](/docs/ignite2/latest/tools/tableau)
-
[Informatica](/docs/ignite2/latest/tools/informatica)
-
[Pentaho](/docs/ignite2/latest/tools/pentaho)
-
[Index Reader](/docs/ignite2/latest/tools/index-reader)
-
Security
-
[Security Model](/docs/ignite2/latest/security/security-model)
-
[Authentication](/docs/ignite2/latest/security/authentication)
-
[SSL/TLS](/docs/ignite2/latest/security/ssl-tls)
-
Transparent Data Encryption
- [Introduction](/docs/ignite2/latest/security/tde)
- [Master key rotation](/docs/ignite2/latest/security/master-key-rotation)
- [Cache encryption key rotation](/docs/ignite2/latest/security/cache-encryption-key-rotation)
-
[Sandbox](/docs/ignite2/latest/security/sandbox)
-
Extensions and Integrations
-
Spring
- [Spring Boot](/docs/ignite2/latest/extensions-and-integrations/spring/spring-boot)
- [Spring Data](/docs/ignite2/latest/extensions-and-integrations/spring/spring-data)
- [Spring Caching](/docs/ignite2/latest/extensions-and-integrations/spring/spring-caching)
- [Spring Transactions](/docs/ignite2/latest/extensions-and-integrations/spring/spring-tx)
-
Ignite for Spark
- [Overview](/docs/ignite2/latest/extensions-and-integrations/ignite-for-spark/overview)
- [IgniteContext and IgniteRDD](/docs/ignite2/latest/extensions-and-integrations/ignite-for-spark/ignitecontext-and-rdd)
- [Ignite DataFrame](/docs/ignite2/latest/extensions-and-integrations/ignite-for-spark/ignite-dataframe)
- [Installation](/docs/ignite2/latest/extensions-and-integrations/ignite-for-spark/installation)
- [Test Ignite with Spark-shell](/docs/ignite2/latest/extensions-and-integrations/ignite-for-spark/spark-shell)
- [Troubleshooting](/docs/ignite2/latest/extensions-and-integrations/ignite-for-spark/troubleshooting)
-
[MyBatis L2 Cache](/docs/ignite2/latest/extensions-and-integrations/mybatis-l2-cache)
-
Streaming
- [Kafka Streamer](/docs/ignite2/latest/extensions-and-integrations/streaming/kafka-streamer)
- [Camel Streamer](/docs/ignite2/latest/extensions-and-integrations/streaming/camel-streamer)
- [Flink Streamer](/docs/ignite2/latest/extensions-and-integrations/streaming/flink-streamer)
- [Flume Sink](/docs/ignite2/latest/extensions-and-integrations/streaming/flume-sink)
- [JMS Streamer](/docs/ignite2/latest/extensions-and-integrations/streaming/jms-streamer)
- [MQTT Streamer](/docs/ignite2/latest/extensions-and-integrations/streaming/mqtt-streamer)
- [RocketMQ Streamer](/docs/ignite2/latest/extensions-and-integrations/streaming/rocketmq-streamer)
- [Storm Streamer](/docs/ignite2/latest/extensions-and-integrations/streaming/storm-streamer)
- [ZeroMQ Streamer](/docs/ignite2/latest/extensions-and-integrations/streaming/zeromq-streamer)
- [Twitter Streamer](/docs/ignite2/latest/extensions-and-integrations/streaming/twitter-streamer)
-
Cassandra Integration
- [Overview](/docs/ignite2/latest/extensions-and-integrations/cassandra/overview)
- [Configuration](/docs/ignite2/latest/extensions-and-integrations/cassandra/configuration)
- [Usage Examples](/docs/ignite2/latest/extensions-and-integrations/cassandra/usage-examples)
- [DDL Generator](/docs/ignite2/latest/extensions-and-integrations/cassandra/ddl-generator)
-
Change Data Capture
- [Overview](/docs/ignite2/latest/extensions-and-integrations/change-data-capture/overview)
- [Ignite to Ignite Replication](/docs/ignite2/latest/extensions-and-integrations/change-data-capture/ignite-to-ignite)
- [Ignite to Kafka Replication](/docs/ignite2/latest/extensions-and-integrations/change-data-capture/ignite-to-kafka)
- [Ignite to PostgreSQL Replication](/docs/ignite2/latest/extensions-and-integrations/change-data-capture/ignite-to-postgresql)
-
[PHP PDO](/docs/ignite2/latest/extensions-and-integrations/php-pdo)
-
[Performance Statistics](/docs/ignite2/latest/extensions-and-integrations/performance-statistics)
-
[ZooKeeper IP Finder](/docs/ignite2/latest/extensions-and-integrations/zookeeper-ip-finder-ext)
-
[Plugins](/docs/ignite2/latest/plugins)
-
Performance and Troubleshooting
-
[General Performance Tips](/docs/ignite2/latest/perf-and-troubleshooting/general-perf-tips)
-
[Memory and JVM Tuning](/docs/ignite2/latest/perf-and-troubleshooting/memory-tuning)
-
[Persistence Tuning](/docs/ignite2/latest/perf-and-troubleshooting/persistence-tuning)
-
[SQL Tuning](/docs/ignite2/latest/perf-and-troubleshooting/sql-tuning)
-
[Thread Pools Tuning](/docs/ignite2/latest/perf-and-troubleshooting/thread-pools-tuning)
-
[Troubleshooting and Debugging](/docs/ignite2/latest/perf-and-troubleshooting/troubleshooting)
-
[Handling Exceptions](/docs/ignite2/latest/perf-and-troubleshooting/handling-exceptions)
-
[Benchmarking With Yardstick](/docs/ignite2/latest/perf-and-troubleshooting/yardstick-benchmarking)
[Edit](https://github.com/apache/ignite/tree/master/docs/_docs/index.adoc)
# Apache Ignite Documentation
Apache Ignite is a distributed database for high-performance computing with in-memory speed.
The technical documentation introduces you to the key capabilities, shows how to use certain features, or how to
approach cluster optimizations and issues troubleshooting. If you are new to Ignite, then start with our
quick start guides, and build the first application in a matter of 5-10 minutes.
Otherwise, select the topic of your interest and have your problems solved, and questions answered.
Good luck with your Ignite journey!
## Quick Start Guides
Build the first application in a matter of minutes.
-
[Java](/docs/ignite2/latest/quick-start/java)
-
[SQL](/docs/ignite2/latest/quick-start/sql)
-
[REST API](/docs/ignite2/latest/quick-start/restapi)
-
[C#/.NET](/docs/ignite2/latest/quick-start/dotnet)
-
[C++](/docs/ignite2/latest/quick-start/cpp)
-
[Python](/docs/ignite2/latest/quick-start/python)
-
[Node.JS](/docs/ignite2/latest/quick-start/nodejs)
-
[PHP](/docs/ignite2/latest/quick-start/php)
## APIs
API reference for various programming languages.
Latest Stable Version
-
[JavaDoc](/releases/latest/javadoc/)
-
[C#/.NET](/releases/latest/dotnetdoc/api/)
-
[C++](/releases/latest/cppdoc/)
Older Versions
-
With the top-level navigation menu, change an Ignite version and select a version-specific API from the APIs drop-down list.
-
Or, go to the [downloads page](/download.cgi) for a full archive of the versions.
## Examples
The Apache Ignite github repository contains a number of runnable examples that illustrate various Ignite functionality.
-
[Java](https://github.com/apache/ignite/tree/master/examples)
-
[C#/.NET](https://github.com/apache/ignite/tree/master/modules/platforms/dotnet/examples)
-
[C++](https://github.com/apache/ignite/tree/master/modules/platforms/cpp/examples)
-
[Python](https://github.com/apache/ignite/tree/master/modules/platforms/python/examples)
-
[Node.JS](https://github.com/apache/ignite/tree/master/modules/platforms/nodejs/examples)
-
[PHP](https://github.com/apache/ignite/tree/master/modules/platforms/php/examples)
## Programming Languages
Ignite is available for Java, .NET/C#, C++ and other programming languages. The Java version provides the richest API.
The .NET/C#, C++, Python, etc. languages may have limited functionality. To make the Ignite documentation intuitive for all application developers,
we adhere to the following conventions:
-
The information provided in this documentation applies to all programming languages unless noted otherwise.
-
Code samples for different languages are provided in different tabs as shown below. For example, if you are a .NET developer, click on the .NET tab in the code examples to see .NET specific code.
This is a place where an example of XML configuration is provided.
Click on other tabs to view an equivalent programmatic configuration.
Code sample in Java. Click on other tabs to view the same example in other languages.
Code sample in .NET. Click on other tabs to view the same example in other languages.
Code sample in C++. Click on other tabs to view the same example in other languages.
-
If there is no tab for a specific language, this most likely means that the functionality is not supported in that language.
© 2026 The Apache Software Foundation.
Apache, Apache Ignite, the Apache feather and the Apache Ignite logo are either registered trademarks or trademarks of The Apache Software Foundation.
- [Quick Start Guides](#quick-start-guides)
- [APIs](#apis)
- [Examples](#examples)
- [Programming Languages](#programming-languages)
-
-