# DataStax Docs | DataStax Docs

- 来源: https://docs.datastax.com/
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

[svg]:w-[110px] sm:[&>svg]:w-[140px] md:[&>svg]:w-[172px]">](https://docs.datastax.com/en)
[home
Docs Home](index.html)
Astra
expand_more
-
[Astra DB Serverless](../astra-db-serverless/index.html)
-
[Astra Streaming](../astra-streaming/index.html)
-
[Astra CLI](../astra-cli/index.html)
Langflow
expand_more
-
[Langflow Open Source
open_in_new](https://docs.langflow.org/)
HCD
expand_more
-
[HCD 2.0](../hyper-converged-database/2.0/get-started/get-started-hcd.html)
-
[HCD 1.2](../hyper-converged-database/1.2/get-started/get-started-hcd.html)
-
[HCD 1.1](../hyper-converged-database/1.1/get-started/get-started-hcd.html)
DSE
expand_more
-
[DSE 6.9](../dse/6.9/get-started/get-started-dse.html)
-
[DSE 6.8](../dse/6.8/get-started/get-started-dse.html)
-
[DSE 5.1](../dse/5.1/getting-started/get-started-dse.html)
-
[Capacity planning and supported platforms](../dse/6.9/planning/plan-guide.html)
-
[OpsCenter 6.8](../opscenter/6.8/overview/opscenter-about.html)
-
[Third-party software](3rd-party-software/third-party-software.html)
Open Source
expand_more
-
[Apache Cassandra
open_in_new](https://cassandra.apache.org/doc/latest/)
-
[Apache Cassandra planning and upgrade guides](../luna-cassandra/index.html)
-
[DataStax Apache Pulsar Connector](../pulsar-connector/index.html)
-
[CDC for Apache Cassandra](../cdc-for-cassandra/index.html)
-
[K8ssandra
open_in_new](https://docs.k8ssandra.io/)
-
[Kubernetes Autoscaling for Apache Pulsar](../kaap-operator/0.2.0/index.html)
-
[Kubernetes Operator for Apache Cassandra](../cassandra-operator/index.html)
-
[Stargate
open_in_new](https://stargate.io/docs/)
-
[Starlight for JMS](../starlight-for-jms/index.html)
-
[Starlight for Kafka](../starlight-for-kafka/index.html)
-
[Starlight for Rabbit MQ](../starlight-for-rabbitmq/index.html)
Support Services
expand_more
-
[Support for Apache Pulsar](../luna-streaming/4.0-7.x/index.html)
-
[Support for Langflow
open_in_new](https://docs.langflow.org/luna-for-langflow)
Tools
expand_more
-
[Mission Control](../mission-control/index.html)
-
[Migrate to Astra](../astra-db-serverless/databases/migration-path-serverless.html)
-
[Migrate to DSE](../dse/6.9/managing/operations/migrate-data.html)
-
[Migrate to HCD](../hyper-converged-database/2.0/migrate/migration-path.html)
-
[CQL for Astra](../astra-db-serverless/cql/develop-with-cql.html)
-
[CQL for DSE](../dse/6.9/cql/reference/cql-syntax.html)
-
[CQL for HCD](../hyper-converged-database/2.0/cql/reference/cql-syntax.html)
-
[Drivers for Astra](../astra-db-serverless/drivers/cassandra-drivers-overview.html)
-
[Drivers for DSE](../dse/6.9/drivers/cassandra-drivers-overview.html)
-
[Drivers for HCD](../hyper-converged-database/2.0/drivers/cassandra-drivers-overview.html)
-
[DataStax Bulk Loader](../dsbulk/overview/dsbulk-about.html)
-
[DataStax Studio](../studio/overview/studio-about.html)
# DataStax Docs
h2]:!hidden">
## [](#)[](#)
## Astra DB Serverless
DataStax Astra DB Serverless provides the tools developers need to create robust AI applications, featuring strong APIs, real-time data processing, and easy integration with other systems.
Vector Search
Modern APIs
Native Integrations
[Get Started](../astra-db-serverless/get-started/quickstart-python.html)
[Sign up for Astra DB](https://astra.datastax.com)
from astrapy import DataAPIClient
# connect to a database
database = DataAPIClient( TOKEN ).get_database( API_ENDPOINT )
# Ingest vectors into your collection
collection = database.test_collection
collection.insert_many(documents= DOCUMENTS )
# Find the closest vectors
collection.find(sort={"$vector": [0.15, 0.1, 0.1, 0.35, 0.55]})
### Popular Products
[#### Astra DB Serverless
Scale with cloud-native databases](../astra-db-serverless/index.html)
[#### Langflow
Build gen AI apps and get to production fast](https://docs.langflow.org/)
[#### Hyper-Converged Database with Vector
Supports new AI and advanced workloads](../hyper-converged-database/2.0/get-started/get-started-hcd.html)
[#### DSE
Enterprise scalability and performance](../dse/6.9/get-started/get-started-dse.html)
[#### Mission Control
Manage your data ecosystem](../mission-control/index.html)
[#### Astra Streaming
Efficient data streaming](../astra-streaming/getting-started/index.html)
### Latest Additions
[#### Migrate with Astra DB Sideloader Astra DB
Migrate your data and applications with little or no downtime.
Read About Astra DB Sideloader](../astra-db-serverless/sideloader/sideloader-overview.html)
[#### Find data with hybrid search Astra DB
Combine vector search and reranking for highly relevant search results.
Read Find data with hybrid search](../astra-db-serverless/databases/hybrid-search.html)
[#### Hyper-Converged Database tutorial HCD
HCD 2.0
Try the new major version of HCDarrow_forward](../hyper-converged-database/2.0/get-started/get-started-hcd.html)
### Work with AI
[#### Introduction to vector databases Astra DB
Learn about terminology, best practices, and use cases for vector databases.
Read What are vector databases](../astra-db-serverless/get-started/vector-concepts.html)
[#### Vector database quickstart Astra DB
Go from database creation to similarity search in 15 minutes.
Try Astra DB Serverless collections quickstart](../astra-db-serverless/get-started/quickstart-python.html)
[#### Langflow quickstart Langflow
Build a RAG application in DataStax Langflow.
Try Langflow quickstart](https://docs.langflow.org/get-started-quickstart)
[#### DataStax Home
Go to the DataStax home page](https://www.ibm.com/products/datastax)
[#### Glossary
Review common terms](../glossary/index.html)
[#### Support
Access support resources](https://www.ibm.com/mysupport/s/)
[#### Downloads
Install files and drivers](https://downloads.datastax.com/#enterprise)
[](https://www.ibm.com/products/datastax)
© Copyright IBM Corporation
2026
|
[Privacy policy](https://www.ibm.com/privacy)
|
[Terms of use](https://www.ibm.com/legal/terms)
|
[Manage Privacy Choices](#)
Apache, Apache
Cassandra, Cassandra, Apache Tomcat, Tomcat, Apache Lucene, Apache Solr,
Apache Hadoop, Hadoop, Apache Pulsar, Pulsar, Apache Spark, Spark, Apache
TinkerPop, TinkerPop, Apache Kafka and Kafka are either registered
trademarks or trademarks of the Apache Software Foundation or its
subsidiaries in Canada, the United States and/or other countries.
Kubernetes is the registered trademark of the Linux Foundation.
[](https://github.com/datastax)
[](https://www.youtube.com/@DataStaxDevs)
General Inquiries:
[Contact IBM](https://www.ibm.com/contact/global)