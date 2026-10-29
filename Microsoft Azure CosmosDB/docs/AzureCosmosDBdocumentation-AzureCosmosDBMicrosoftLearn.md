# Azure Cosmos DB documentation - Azure Cosmos DB | Microsoft Learn

- 来源: https://learn.microsoft.com/azure/cosmos-db/
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

[Skip to main content](#main)
This browser is no longer supported.
Upgrade to Microsoft Edge to take advantage of the latest features, security updates, and technical support.
[Download Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=2092881 )
[More info about Internet Explorer and Microsoft Edge](https://learn.microsoft.com/en-us/lifecycle/faq/internet-explorer-microsoft-edge)
# Azure Cosmos DB documentation
Fully managed, distributed NoSQL, relational, and vector database for modern app development. High performance, high availability, and support for open-source PostgreSQL, MongoDB, and Apache Cassandra. Build cloud-native apps effortlessly.
Overview
[Introduction to Azure Cosmos DB](introduction)
Architecture
[Vector Database in Azure Cosmos DB](vector-database)
Reference
[Pricing](https://azure.microsoft.com/pricing/details/cosmos-db/)
Training
[Certification - Azure Cosmos DB Developer Specialty](/en-us/certifications/azure-cosmos-db-developer-specialty/)
Training
[Certification - Azure Developer Associate](/en-us/certifications/azure-developer/)
Tutorial
[AI agents with Azure Cosmos DB](ai-agents)
Get started
[Azure Cosmos DB Emulator](emulator)
Get started
[Azure Cosmos DB Agent Kit](gen-ai/agent-kit)
## APIs
Choose from multiple APIs that provide compatibility with popular NoSQL and relational database models for modern applications.
### NoSQL
Build applications using native SQL queries with automatic indexing and schema flexibility for document-based workloads.
-
[SQL queries](/en-us/cosmos-db/query/overview)
-
[Model document data](modeling-data)
### MongoDB
Migrate existing MongoDB applications seamlessly with full wire protocol compatibility and familiar MongoDB tools.
-
[Supported features and syntax](mongodb/feature-support-42)
-
[Mapping consistency levels](mongodb/consistency-mapping)
-
[Extension commands](mongodb/custom-commands)
-
[See more](mongodb/)
### Apache Cassandra
Build highly scalable applications using the Cassandra Query Language (CQL) with automatic global distribution.
-
[Wire protocol support](cassandra/support)
-
[Partitioning](cassandra/partitioning)
-
[Secondary indexing](cassandra/secondary-indexing)
-
[See more](cassandra/)
### Apache Gremlin
Create graph-based applications using the Gremlin graph traversal language for complex relationship queries.
-
[Wire protocol support](gremlin/support)
-
[Graph data modeling](gremlin/modeling)
-
[Import graph data](gremlin/bulk-executor-dotnet)
-
[See more](graph/)
### Table
Modernize Azure Table Storage applications with premium capabilities and global distribution.
-
[Wire protocol support](table/support)
-
[Find request unit charge](table/find-request-unit-charge)
-
[FAQ](table/faq)
-
[See more](table/)
### PostgreSQL
Build distributed relational applications using the familiar PostgreSQL wire protocol with horizontal scaling.
-
[Distributed relational databases](distributed-relational)
-
[Connect and run SQL commands using Python](postgresql/quickstart-app-stacks-python)
-
[Distribute and modify tables](postgresql/howto-modify-distributed-tables)
-
[See more](postgresql/)
## Developer and DevOps guides
Advance your development and DevOps workflows with practical guides, tools, and best practices for building scalable applications on Azure Cosmos DB.
### Vector search and AI integration
Unlock new capabilities in your applications with Azure Cosmos DB by implementing powerful vector search and AI-driven features.
-
[Vector Database in Azure Cosmos DB](vector-database)
-
[Vector search in Azure Cosmos DB for NoSQL](nosql/vector-search)
### Infrastructure as code (IaC)
Automate deployment and management of Azure Cosmos DB resources using modern Infrastructure as Code (IaC) tools like Bicep, ARM templates, and Terraform.
-
[Azure Resource Manager templates](nosql/quickstart-template-json)
-
[Bicep templates](nosql/quickstart-template-bicep)
-
[Terraform provider](nosql/quickstart-terraform)
### Connect to your database
Learn how to connect to your Azure Cosmos DB using various tools, drivers, and popular programming languages across different APIs.
-
[Create an Azure Cosmos DB for NoSQL account](nosql/quickstart-portal)
-
[Create an Azure Cosmos DB for PostgreSQL account](postgresql/quickstart-create-portal)
-
[Create an Azure Cosmos DB for MongoDB account](mongodb/quickstart-nodejs)
### Performance optimization
Discover techniques to improve the speed, efficiency, and scalability of your Azure Cosmos DB applications across different workload patterns.
-
[Performance tips for Azure Cosmos DB for NoSQL](nosql/performance-tips-dotnet-sdk-v3)
-
[Optimize request costs](optimize-cost-reads-writes)
-
[Partitioning and horizontal scaling](partitioning)
## Build your first application
Create a console application using Azure Cosmos DB and your preferred development language and API.
[.NET (NoSQL)](nosql/quickstart-dotnet)
[Python (NoSQL)](nosql/quickstart-python)
[JavaScript (NoSQL)](nosql/quickstart-nodejs?pivots=programming-language-js)
[TypeScript (NoSQL)](nosql/quickstart-nodejs?pivots=programming-language-ts)
[Java (NoSQL)](nosql/quickstart-java)
[Go (NoSQL)](nosql/quickstart-go)
[Rust (NoSQL)](nosql/quickstart-rust)
## Core concepts and architecture
Understand the fundamental concepts that power Azure Cosmos DB's global distribution, consistency, and performance capabilities.
### Explore core concepts
Learn about the essential building blocks of Azure Cosmos DB including resource models, global distribution, and consistency levels.
-
[Resource model](resource-model)
-
[Distribute data globally](distribute-data-globally)
-
[Partitioning](partitioning)
-
[Throughput & request units](request-units)
### Model your data
Design effective data models and partitioning strategies for optimal performance and cost efficiency.
-
[Data modeling and partitioning](nosql/model-partition-example)
-
[Azure Cosmos DB service quotas](concepts-limits)
-
[Distributed NoSQL databases](distributed-nosql)
### Analytics with Microsoft Fabric
Integrate Azure Cosmos DB with Microsoft Fabric for analytics.
-
[Azure Cosmos DB Mirroring](/en-us/fabric/database/mirrored-database/azure-cosmos-db?context=/azure/cosmos-db/context/context)
-
[Cosmos DB in Microsoft Fabric](/en-us/fabric/database/cosmos-db/overview?context=/azure/cosmos-db/context/context)
## Security and compliance
Protect your data and applications with comprehensive security features including encryption, access controls, and compliance certifications.
### Security overview
Comprehensive security features to protect your data at rest, in transit, and during processing.
-
[Security baseline for Azure Cosmos DB](/en-us/security/benchmark/azure/baselines/cosmos-db-security-baseline?context=/azure/cosmos-db/context/context)
-
[Database encryption at rest](database-encryption-at-rest)
-
[Configure IP firewall](how-to-configure-firewall)
-
[Compliance](compliance)
### Access control and authentication
Manage user access and authentication using Microsoft Entra ID, role-based access control, and resource tokens.
-
[Access control in Azure Cosmos DB](secure-access-to-data)
-
[Configure role-based access control with Microsoft Entra ID](how-to-setup-rbac)
-
[Access Azure Key Vault using managed identities](access-key-vault-managed-identity)
### Network security
Secure your database connectivity using virtual networks, private endpoints, and firewall rules.
-
[Configure private endpoints](how-to-configure-private-endpoints)
-
[Configure virtual network service endpoint](how-to-configure-vnet-service-endpoint)
## Data migration and tools
Migrate existing data to Azure Cosmos DB using various tools and services designed for different data sources and migration scenarios.
### Migration options
Choose the right migration approach for your data source and target API using Azure native tools and services.
-
[Cassandra Query Language (CQL) shell, Spark – API for Cassandra](cassandra/migrate-data)
-
[Azure Database Migration Service – API for MongoDB](/en-us/azure/dms/tutorial-mongodb-cosmos-db)
-
[Migrate hundreds of terabytes of data](migrate)
### Migration guides
Step-by-step migration guides for specific database platforms and migration tools.
-
[Oracle Database to Azure Cosmos DB API for NoSQL using Striim](cosmosdb-sql-api-migrate-data-striim)
-
[Oracle Database to Azure Cosmos DB API for Cassandra using Striim](cassandra/migrate-data-striim)
-
[Oracle Database to Azure Cosmos DB API for Cassandra using Arcion](cassandra/oracle-migrate-cosmos-db-arcion)
## Samples and resources
Accelerate your Azure Cosmos DB development with code samples, community resources, and learning materials.
### Microsoft samples
Official Microsoft samples, galleries, and code repositories for Azure Cosmos DB development across all APIs.
-
[Azure Cosmos DB samples gallery](https://azurecosmosdb.github.io/gallery/)
-
[Microsoft Questions and Answers](/en-us/answers/tags/187/azure-cosmos-db)
### Open-source community
Community-driven samples, tools, and resources from the Azure Cosmos DB open-source ecosystem.
-
[Azure Cosmos DB GitHub organization](https://github.com/azurecosmosdb/)
-
[Published GitHub samples](https://github.com/search?q=org%3Aazure-samples+cosmos&type=repositories)
### Videos and events
Stay updated with the latest Azure Cosmos DB developments through conferences, webinars, and educational video series.
-
[Azure Cosmos DB Conf 2025](https://www.youtube.com/playlist?list=PLmamF3YkHLoLQhnFsKWhtKu_Tp0uXPFdn)
-
[Azure Cosmos DB TV](https://www.youtube.com/playlist?list=PLmamF3YkHLoKMzT3gP4oqHiJbjMaiiLEh)
-
[Azure Cosmos DB & AI Integration](https://youtube.com/playlist?list=PLmamF3YkHLoJyuoikrskPzpttybXiuFFL&si=ljM012JQu0ReuYEo)
-
[Customer Stories - Azure Cosmos DB real-world examples](https://youtube.com/playlist?list=PLmamF3YkHLoJtcbM2-_e5U3R6tL2LLbig&si=f-jDPhcUvEmvjpoj)
-
[Azure Cosmos DB Design Patterns](https://youtube.com/playlist?list=PLmamF3YkHLoI69DIwplhBqk-KYoOLEqOs&si=E6Q1NYfKgGDw279m)
Azure Cosmos DB is a fully managed NoSQL, relational, and vector database for modern app development. Build cloud-native apps with guaranteed speed at any scale, turnkey global distribution, and comprehensive SLA-backed availability.
Key capabilities:
- Single-digit millisecond response times with automatic and instant scalability
- Multi-API support - NoSQL, MongoDB, PostgreSQL, Apache Cassandra, Apache Gremlin, and Table
- AI-powered features - Vector database, Query Copilot, and seamless Foundry Tools integration
- Enterprise-grade security - Encryption at rest, role-based access control, and compliance certifications
- Global distribution - Multi-region writes and data distribution to any Azure region
Trusted by industry leaders: OpenAI relies on Azure Cosmos DB to dynamically scale ChatGPT, enabling high reliability and low maintenance for one of the fastest-growing consumer applications ever.
Get started today with the [Azure Cosmos DB Emulator](emulator) for local development.
en-us
Your Privacy Choices
Theme
-
Light
-
Dark
-
High contrast
-
-
AI Disclaimer
-
Previous Versions
-
Blog
-
Contribute
-
Privacy
-
Consumer Health Privacy
-
Terms of Use
-
Trademarks
- © Microsoft 2026