# What is GraphDB? — GraphDB 11.5 documentation

- 来源: https://graphdb.ontotext.com/documentation/
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

[](index.html)
11.5
[](#)
[11.4](/documentation/11.4/)
[11.3](/documentation/11.3/)
[11.2](/documentation/11.2/)
[11.1](/documentation/11.1/)
[11.0](/documentation/11.0/)
[10.8](/documentation/10.8/)
[10.7](/documentation/10.7/)
[10.6](/documentation/10.6/)
[10.5](/documentation/10.5/)
[10.4](/documentation/10.4/)
[10.3](/documentation/10.3/)
[10.2](/documentation/10.2/)
[10.1](/documentation/10.1/)
[10.0](/documentation/10.0/)
[9.11 EE](/documentation/9.11/enterprise/)
[9.11 SE](/documentation/9.11/standard/)
[9.11 Free](/documentation/9.11/free/)
[Other versions](previous-versions.html)
[](#collapseSideNav)
Getting Started with GraphDB
- [What is GraphDB?](#)
- [Licensing](licensing.html)
- [Cloud deployments for GraphDB](cloud-deployment.html)
- [How to install GraphDB](how-to-install-graphdb.html)
- [Working with Workbench](working-with-workbench.html)
Managing Repositories
- [Overview of repositories](repositories-overview.html)
- [Creating and editing repositories](creating-a-repository.html)
- [Configuring a repository](configuring-a-repository.html)
- [Connecting to remote locations and data sources](connecting-to-remote-locations.html)
- [Using plugins](using-plugins.html)
- [Inferencing](inference.html)
- [Data storage](storage.html)
- [Monitoring and terminating queries and update requests](query-monitoring.html)
- [Accessing relational databases with data virtualization](virtualization.html)
- [Federation from multiple SPARQL endpoints with FedX](fedx-federation.html)
- [Graph replacement optimization](replace-graph.html)
- [Managing repositories and locations via the GraphDB REST API](manage-repos-with-restapi.html)
Loading and exploring data
- [Loading data](loading-data.html)
- [Updating data with SPARQL templates](updating-data.html)
- [Exploring your data](querying-and-exploring-data.html)
- [SPARQL queries](sparql-queries.html)
- [SPARQL plugins](sparql-plugins.html)
- [Visualize and explore](visualize-and-explore.html)
- [Visualize geospatially linked data](geo-plugin.html)
- [GraphQL](graphql.html)
- [GraphQL schemas and endpoint management](graphql-schema-gen.html)
- [Semantic similarity searches](semantic-similarity-searches.html)
- [Querying GPT models](gpt-queries.html)
- [Talk to Your Graph](talk-to-graph.html)
- [Graph path search](graph-path-search.html)
- [Reasoning](reasoning.html)
- [Exporting data](exporting-data.html)
Working with connectors
- [Connecting to external components and services](connectors.html)
- [General full-text search with the Connectors](general-full-text-search-with-connectors.html)
- [Lucene GraphDB Connector](lucene-graphdb-connector.html)
- [Solr GraphDB Connector](solr-graphdb-connector.html)
- [Elasticsearch GraphDB Connector](elasticsearch-graphdb-connector.html)
- [OpenSearch GraphDB Connector](opensearch-graphdb-connector.html)
- [Kafka GraphDB Connector](kafka-graphdb-connector.html)
- [Kafka Sink Connector](kafka-sink-connector.html)
- [ChatGPT Retrieval GraphDB Connector](retrieval-graphdb-connector.html)
- [MongoDB integration](mongodb-graphdb-connector.html)
- [Text mining plugin](text-mining-plugin.html)
- [Embedding model configuration for vector search](embedding-model-configuration.html)
Working with clusters
- [Overview of clusters](cluster-basics.html)
- [Creating and managing a cluster](creating-a-cluster.html)
- [Cluster states and election procedures](cluster-advanced.html)
- [Using a cluster](using-a-cluster.html)
- [Multi-region cluster deployments](multi-region-cluster-availability.html)
Administration
- [Setting up your license](set-up-your-license.html)
- [Security](security.html)
- [Backup and restore](backup-and-restore.html)
- [Monitoring and troubleshooting](monitoring-and-troubleshooting.html)
- [Docker and Helm](docker-and-helm.html)
- [Configuring GraphDB memory](configuring-graphdb-memory.html)
- [Performance optimizations](performance-optimizations.html)
- [Administration via HTTP with curl](admin-with-curl.html)
- [Migrating GraphDB configurations](migrating-graphdb-configurations.html)
- [Migrating GraphQL configurations from Semantic Objects to GraphDB](graphql-migration.html)
- [How to deploy GraphDB in AWS](aws-deployment.html)
- [How to deploy GraphDB in Azure](azure-deployment.html)
- [How to deploy GraphDB in GCP](gcp-deployment.html)
- [Using GraphDB’s LLM tools with external clients](using-graphdb-llm-tools-with-external-clients.html)
Tutorials
- [Running the interactive user guides](interactive-guides.html)
- [GraphDB Fundamentals Video Series](fundamentals.html)
- [Loading and querying data](loading-querying-data.html)
- [GraphDB and W3C standards](w3c-standards.html)
- [Customization and other advanced development](customization.html)
- [Talk to Your Graph examples](talk-to-graph-examples.html)
- [Vector search in nested fields with Elasticsearch](vector-search-nested-objects-elastic.html)
Reference
- [Architecture and components](architecture-components.html)
- [GraphDB command line tools](command-line-tools.html)
- [Directories and configuration properties](directories-and-config-properties.html)
- [RDF formats](rdf-formats.html)
- [SPARQL compliance](sparql-compliance.html)
- [SPARQL functions reference](sparql-functions-reference.html)
- [SPARQL extensions reference](sparql-ext-functions-reference.html)
- [GraphDB APIs](clients-and-apis.html)
- [OWL compliance](owl-compliance.html)
- [W3C specifications](w3c-specs.html)
- [Benchmarks](benchmark.html)
- [GraphDB system statements](system-statements.html)
- [Glossary](glossary.html)
- [JavaScript functions](javascript-functions.html)
Help
- [FAQ](faq.html)
- [Support](support.html)
- [Release notes](release-notes.html)
- [Vulnerabilities](vulnerabilities.html)
You are viewing an older version of this document. For the latest, see version [](#).
You are viewing an older version of the GraphDB documentation. For the latest, see [](#).
# What is GraphDB?[¶](#what-is-graphdb)
Good places to start for…
- [Everyone](userroles.html#role-everyone): All users, especially new ones, who can benefit from introductions to basic GraphDB capabilities.
- [Knowledge engineers](userroles.html#role-knowledge-engineer): People who focus on the technologies and standards for creating and taking advantage of knowledge graphs.
- [Data scientists](userroles.html#role-data-scientist): People who use a variety of data formats and tools, often in different combinations, to identify patterns that help to answer questions.
- [Developers](userroles.html#role-developer): People who are building an application that uses GraphDB as a backend.
- [Administrators](userroles.html#role-admin): People who are installing and maintaining a GraphDB system or an application that uses GraphDB as the backend.
Graphwise GraphDB is a highly efficient, scalable and robust [graph database](glossary.html#glossary-sr) with [RDF](introduction-to-semantic-web.html#introduction-to-semantic-web-rdf) and [SPARQL](introduction-to-semantic-web.html#introduction-to-semantic-web-sparql) support. GraphDB is one of the few triplestores that can perform real-time [semantic inferencing](introduction-to-semantic-web.html#introduction-to-semantic-web-reasoning-strategies) at scale, allowing users to derive new semantic facts from existing facts.
With excellent enterprise features, integration with external search applications, LLM Graph Retrieval-Augmented Generation (Graph RAG) capabilities, and compatibility with industry standards, GraphDB is the preferred database choice of both small independent developers and big enterprises.
Highlights of GraphDB include:
- Dedicated community and commercial support.
- Integration with Elasticsearch, OpenSearch, Lucene, Solr, and other high-performance search applications.
- Clusters and multi-region deployments support.
- [Connectors](connectors.html), which provide fast keyword and faceted searches that are typically implemented by an external component. All GraphDB editions include connectors for Lucene and ChatGPT, and the Enterprise Edition includes connectors for Solr, Elasticsearch, OpenSearch, and Kafka.
- Implementation of the [RDF4J](https://rdf4j.org/about/) framework interfaces and the [W3C SPARQL Protocol specification](https://www.w3.org/TR/sparql11-overview/). Learn more about RDF4J and the roles of its layers in the [Architecture and components](architecture-components.html) chapter of this documentation’s Reference section.
- Support for all RDF serialization formats.
- Availability as a [cloud deployment](cloud-deployment.html) on [Amazon Web Services](aws-deployment.html) and on [Microsoft Azure](azure-deployment.html).
Reasoning and query evaluation are performed over a persistent storage layer. Loading, [reasoning](reasoning.html), and query evaluation proceed extremely quickly even against huge [ontologies](glossary.html#glossary-ont) and [knowledge bases](glossary.html#glossary-kb).
GraphDB can manage billions of explicit statements on desktop hardware and handle tens of billions of statements on commodity server hardware. According to the [LDBC Semantic Publishing Benchmark](https://ldbcouncil.org/developer/spb), it is one of the most scalable OWL repositories currently available.
Graphwise [offers licenses for two editions of GraphDB:](https://graphwise.ai/components/graphdb/)
- GraphDB Free
- GraphDB Enterprise (EE)
The GraphDB Standard Edition (SE), while no longer offered, still receives legacy support.
#### We are on Stack Overflow
Get quick answers on technical questions from the community as well as Graphwise experts using the
[graphdb](https://stackoverflow.com/questions/tagged/graphdb) tag
#### Download documentation
-
[PDF](/documentation/11.5/pdf/GraphDB.pdf)
-
[ePUB](/documentation/11.5/epub/GraphDB.epub)
#### Contacts
-
[Support
· graphdb-support@graphwise.ai](mailto:graphdb-support@graphwise.ai)
-
[Sales
· sales@graphwise.ai](mailto:sales@graphwise.ai)
-
[General
· info@graphwise.ai](mailto:info@graphwise.ai)
#### More info
- [About Graphwise](https://graphwise.ai/imprint/)
- [About Ontotext](https://www.ontotext.com/about-us/)
- [Semantic web](https://www.w3.org/standards/semanticweb/)
#### Follow us
[](https://www.linkedin.com/company/graphwise)
[](https://www.youtube.com/@GraphwiseAI)
Copyright © 2015-2026, ONTOTEXT AD, doing business as Graphwise
[Graphwise](https://graphwise.ai/components/graphdb/)
| [Privacy](https://ontotext.com/privacy-policy-2/)