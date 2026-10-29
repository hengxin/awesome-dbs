# Apache Solr Reference Guide :: Apache Solr Reference Guide

- 来源: https://solr.apache.org/guide/solr/latest/index.html
- 归档时间: 2026-10-29
- 说明: 官方技术白皮书 / 架构文档的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

[Apache Solr Reference Guide](https://solr.apache.org/guide)
[Solr Website](https://solr.apache.org/)
[Resources](#)
[Solr Javadocs](https://solr.apache.org/docs/10_0_0/index.html)
[Source Code](https://solr.apache.org/community.html#version-control)
[Community Links](https://solr.apache.org/community.html)
[Contribute](https://github.com/apache/solr/tree/main/dev-docs/ref-guide)
[Download](https://solr.apache.org/downloads.html)
Apache Solr
10.0
-
[Apache Solr](index.html)
-
[10.1-beta](../10_1/index.html)
-
[10.0](index.html)
-
[9.11](../9_11/index.html)
-
[9.10](../9_10/index.html)
-
[9.9](../9_9/index.html)
-
[9.8](../9_8/index.html)
-
[9.7](../9_7/index.html)
-
[9.6](../9_6/index.html)
-
[9.5](../9_5/index.html)
-
[9.4](../9_4/index.html)
-
[9.3](../9_3/index.html)
-
[9.2](../9_2/index.html)
-
[9.1](../9_1/index.html)
-
[9.0](../9_0/index.html)
-
[Apache Solr Operator](../../operator/latest/index.html)
-
[v0.9](../../operator/latest/index.html)
-
[v0.8](../../operator/0_8/index.html)
-
[v0.7](../../operator/0_7/index.html)
-
[v0.6](../../operator/0_6/index.html)
-
[v0.5](../../operator/0_5/index.html)
-
[v0.4](../../operator/0_4/index.html)
-
[v0.3](../../operator/0_3/index.html)
- [Archived Solr Reference Guides](https://solr.apache.org/guide)
-
[8.11](https://solr.apache.org/guide/8_11)
-
[7.7](https://solr.apache.org/guide/7_7)
-
[6.6](https://solr.apache.org/guide/6_6)
-
[Older](http://archive.apache.org/dist/lucene/solr/ref-guide/)
-
Getting Started
-
[Introduction to Solr](getting-started/introduction.html)
-
Solr Concepts
-
[Documents, Fields, and Schema Design](getting-started/documents-fields-schema-design.html)
-
[Solr Indexing](getting-started/solr-indexing.html)
-
[Searching in Solr](getting-started/searching-in-solr.html)
-
[Relevance](getting-started/relevance.html)
-
[Solr Glossary](getting-started/solr-glossary.html)
-
[Solr Tutorials](getting-started/solr-tutorial.html)
-
[Exercise 0: Five Minutes to Searching!](getting-started/tutorial-five-minutes.html)
-
[Exercise 1: Index Techproducts Data](getting-started/tutorial-techproducts.html)
-
[Exercise 2: Index Films Data](getting-started/tutorial-films.html)
-
[Exercise 3: Index Your Own Data](getting-started/tutorial-diy.html)
-
[Exercise 4: Using ParamSets](getting-started/tutorial-paramsets.html)
-
[Exercise 5: Using Vectors](getting-started/tutorial-vectors.html)
-
[Exercise 6: Getting Deeper with SolrCloud](getting-started/tutorial-solrcloud.html)
-
[Exercise 7: Sentiment Analysis with OpenNLP](getting-started/tutorial-opennlp.html)
-
[SolrCloud on AWS EC2](getting-started/tutorial-aws.html)
-
[Solr Admin UI](getting-started/solr-admin-ui.html)
-
[About This Guide](getting-started/about-this-guide.html)
-
Deployment Guide
-
[Solr Control Script Reference](deployment-guide/solr-control-script-reference.html)
-
Installation & Deployment
-
[System Requirements](deployment-guide/system-requirements.html)
-
[Installing Solr](deployment-guide/installing-solr.html)
-
[Taking Solr to Production](deployment-guide/taking-solr-to-production.html)
-
[JVM Settings](deployment-guide/jvm-settings.html)
-
[Upgrading a Solr Cluster](deployment-guide/upgrading-a-solr-cluster.html)
-
[Backup and Restore](deployment-guide/backup-restore.html)
-
[Solr in Docker](deployment-guide/solr-in-docker.html)
-
[Solr Docker FAQ](deployment-guide/docker-faq.html)
-
Scaling Solr
-
[Solr Cluster Types](deployment-guide/cluster-types.html)
-
SolrCloud Clusters
-
[SolrCloud Shards and Indexing](deployment-guide/solrcloud-shards-indexing.html)
-
[SolrCloud Recoveries and Write Tolerance](deployment-guide/solrcloud-recoveries-and-write-tolerance.html)
-
[SolrCloud Distributed Requests](deployment-guide/solrcloud-distributed-requests.html)
-
[Node Roles](deployment-guide/node-roles.html)
-
[Aliases](deployment-guide/aliases.html)
-
Collections API
-
[Cluster and Node Management Commands](deployment-guide/cluster-node-management.html)
-
[Collection Management Commands](deployment-guide/collection-management.html)
-
[Shard Management Commands](deployment-guide/shard-management.html)
-
[Replica Management Commands](deployment-guide/replica-management.html)
-
[Alias Management](deployment-guide/alias-management.html)
-
ZooKeeper Configuration
-
[ZooKeeper Ensemble Configuration](deployment-guide/zookeeper-ensemble.html)
-
[ZooKeeper File Management](deployment-guide/zookeeper-file-management.html)
-
[ZooKeeper Utilities](deployment-guide/zookeeper-utilities.html)
-
[SolrCloud with Legacy Configuration Files](deployment-guide/solrcloud-with-legacy-configuration-files.html)
-
Admin UI
-
[Collections / Core Admin](deployment-guide/collections-core-admin.html)
-
[Cloud Screens](deployment-guide/cloud-screens.html)
-
User-Managed Clusters
-
[User-Managed Index Replication Index Replication](deployment-guide/user-managed-index-replication.html)
-
[User-Managed Distributed Search](deployment-guide/user-managed-distributed-search.html)
-
Monitoring Solr
-
[Configuring Logging](deployment-guide/configuring-logging.html)
-
[Ping](deployment-guide/ping.html)
-
[Metrics Reporting and Monitoring](deployment-guide/metrics-reporting.html)
-
[Performance Statistics Reference](deployment-guide/performance-statistics-reference.html)
-
[Plugins & Stats Screen](deployment-guide/plugins-stats-screen.html)
-
[JMX with Solr](deployment-guide/jmx-with-solr.html)
-
[Thread Dump Screen](deployment-guide/thread-dump.html)
-
[Distributed Tracing](deployment-guide/distributed-tracing.html)
-
[Circuit Breakers](deployment-guide/circuit-breakers.html)
-
[Request Rate Limiters](deployment-guide/rate-limiters.html)
-
[Task Management](deployment-guide/task-management.html)
-
[Securing Solr](deployment-guide/securing-solr.html)
-
[Configuring Authentication and Authorization](deployment-guide/authentication-and-authorization-plugins.html)
-
[Basic Authentication Plugin](deployment-guide/basic-authentication-plugin.html)
-
[JWT Authentication Plugin](deployment-guide/jwt-authentication-plugin.html)
-
[Certificate Authentication Plugin](deployment-guide/cert-authentication-plugin.html)
-
[Rule-Based Authorization Plugins](deployment-guide/rule-based-authorization-plugin.html)
-
[Audit Logging](deployment-guide/audit-logging.html)
-
[Enabling SSL](deployment-guide/enabling-ssl.html)
-
[ZooKeeper Access Control](deployment-guide/zookeeper-access-control.html)
-
[Security UI](deployment-guide/security-ui.html)
-
[Client APIs](deployment-guide/client-apis.html)
-
[SolrJ](deployment-guide/solrj.html)
-
[JavaScript](deployment-guide/javascript.html)
-
[Python](deployment-guide/python.html)
-
[Ruby](deployment-guide/ruby.html)
-
Configuration Guide
-
[Solr Configuration Files](configuration-guide/configuration-files.html)
-
[Property Substitution in Configuration Files](configuration-guide/property-substitution.html)
-
[Core Discovery](configuration-guide/core-discovery.html)
-
[Configuring solr.xml](configuration-guide/configuring-solr-xml.html)
-
[Solr Properties Reference](configuration-guide/solr-properties.html)
-
[Configuring solrconfig.xml](configuration-guide/configuring-solrconfig-xml.html)
-
[Index Location and Format](configuration-guide/index-location-format.html)
-
[Index Segments and Merging](configuration-guide/index-segments-merging.html)
-
[Schema Factory Configuration](configuration-guide/schema-factory.html)
-
[Commits and Transaction Logs](configuration-guide/commits-transaction-logs.html)
-
[Caches and Query Warming](configuration-guide/caches-warming.html)
-
[Request Handlers and Search Components](configuration-guide/requesthandlers-searchcomponents.html)
-
[Implicit Request Handlers](configuration-guide/implicit-requesthandlers.html)
-
[RealTime Get](configuration-guide/realtime-get.html)
-
[InitParams](configuration-guide/initparams.html)
-
[RequestDispatcher](configuration-guide/requestdispatcher.html)
-
[Update Request Processors](configuration-guide/update-request-processors.html)
-
[Script Update Processor](configuration-guide/script-update-processor.html)
-
[Codec Factory](configuration-guide/codec-factory.html)
-
Configuration APIs
-
[Config API](configuration-guide/config-api.html)
-
[Request Parameters API](configuration-guide/request-parameters-api.html)
-
[Managed Resources](configuration-guide/managed-resources.html)
-
[Collections API](configuration-guide/collections-api.html)
-
[Configsets API](configuration-guide/configsets-api.html)
-
[CoreAdmin API](configuration-guide/coreadmin-api.html)
-
[v2 API](configuration-guide/v2-api.html)
-
[Configsets](configuration-guide/config-sets.html)
-
[Resource Loading](configuration-guide/resource-loading.html)
-
[Solr Plugins](configuration-guide/solr-plugins.html)
-
[Lib Directories](configuration-guide/libs.html)
-
[Solr Modules](configuration-guide/solr-modules.html)
-
[Package Management](configuration-guide/package-manager.html)
-
[Package Manager Internals](configuration-guide/package-manager-internals.html)
-
[Cluster Plugins](configuration-guide/cluster-plugins.html)
-
[Replica Placement Plugins](configuration-guide/replica-placement-plugins.html)
-
Schema and Indexing Guide
-
Solr Schema
-
[Schema Elements](indexing-guide/schema-elements.html)
-
[Schema API](indexing-guide/schema-api.html)
-
[Schemaless Mode](indexing-guide/schemaless-mode.html)
-
[Schema Designer](indexing-guide/schema-designer.html)
-
[Schema Browser Screen](indexing-guide/schema-browser-screen.html)
-
Fields & Schema Design
-
[Fields](indexing-guide/fields.html)
-
Field Types
-
[Field Type Definitions and Properties](indexing-guide/field-type-definitions-and-properties.html)
-
[Field Types Included with Solr](indexing-guide/field-types-included-with-solr.html)
-
[Currencies and Exchange Rates](indexing-guide/currencies-exchange-rates.html)
-
[Date Formatting and Date Math](indexing-guide/date-formatting-math.html)
-
[Enum Fields](indexing-guide/enum-fields.html)
-
[Field Properties by Use Case](indexing-guide/field-properties-by-use-case.html)
-
[Copy Fields](indexing-guide/copy-fields.html)
-
[Dynamic Fields](indexing-guide/dynamic-fields.html)
-
[DocValues](indexing-guide/docvalues.html)
-
[Luke Request Handler](indexing-guide/luke-request-handler.html)
-
[Document Analysis in Solr](indexing-guide/document-analysis.html)
-
[Analyzers](indexing-guide/analyzers.html)
-
[Tokenizers](indexing-guide/tokenizers.html)
-
[Filters](indexing-guide/filters.html)
-
[CharFilters](indexing-guide/charfilters.html)
-
[Language Analysis](indexing-guide/language-analysis.html)
-
[Phonetic Matching](indexing-guide/phonetic-matching.html)
-
[Analysis Screen](indexing-guide/analysis-screen.html)
-
Indexing & Data Operations
-
[Indexing with Update Handlers](indexing-guide/indexing-with-update-handlers.html)
-
[Transforming and Indexing Custom JSON](indexing-guide/transforming-and-indexing-custom-json.html)
-
[Indexing with Update CBOR data format](indexing-guide/indexing-with-cbor.html)
-
[Indexing with Solr Cell and Apache Tika](indexing-guide/indexing-with-tika.html)
-
[Indexing Nested Documents](indexing-guide/indexing-nested-documents.html)
-
[Post Tool](indexing-guide/post-tool.html)
-
[Documents Screen](indexing-guide/documents-screen.html)
-
[Partial Document Updates](indexing-guide/partial-document-updates.html)
-
[Reindexing](indexing-guide/reindexing.html)
-
[Language Detection](indexing-guide/language-detection.html)
-
[De-Duplication](indexing-guide/de-duplication.html)
-
[Content Streams](indexing-guide/content-streams.html)
-
Query Guide
-
[Query Syntax and Parsers](query-guide/query-syntax-and-parsers.html)
-
[Common Query Parameters](query-guide/common-query-parameters.html)
-
[Standard Query Parser](query-guide/standard-query-parser.html)
-
[DisMax Query Parser](query-guide/dismax-query-parser.html)
-
[Extended DisMax (eDisMax) Query Parser](query-guide/edismax-query-parser.html)
-
[Function Queries](query-guide/function-queries.html)
-
[Expression Value Source Parser](query-guide/expression-value-source-parser.html)
-
[Local Params](query-guide/local-params.html)
-
[JSON Request API](query-guide/json-request-api.html)
-
[JSON Query DSL](query-guide/json-query-dsl.html)
-
[Searching Nested Child Documents](query-guide/searching-nested-documents.html)
-
[Block Join Query Parser](query-guide/block-join-query-parser.html)
-
[Join Query Parser](query-guide/join-query-parser.html)
-
[Spatial Search](query-guide/spatial-search.html)
-
[Dense Vector Search](query-guide/dense-vector-search.html)
-
[Other Query Parsers](query-guide/other-parsers.html)
-
[SQL Query Language](query-guide/sql-query.html)
-
[JDBC with DbVisualizer](query-guide/jdbc-dbvisualizer.html)
-
[JDBC with SQuirreL SQL](query-guide/jdbc-squirrel.html)
-
[JDBC with Apache Zeppelin](query-guide/jdbc-zeppelin.html)
-
[JDBC with Python/Jython](query-guide/jdbc-python-jython.html)
-
[JDBC with R](query-guide/jdbc-r.html)
-
[Query Screen](query-guide/query-screen.html)
-
[SQL Query Screen](query-guide/sql-screen.html)
-
Enhancing Queries
-
[Spell Checking](query-guide/spell-checking.html)
-
[Suggester](query-guide/suggester.html)
-
[MoreLikeThis](query-guide/morelikethis.html)
-
[Query Re-Ranking](query-guide/query-re-ranking.html)
-
[Learning To Rank](query-guide/learning-to-rank.html)
-
[Tagger Handler](query-guide/tagger-handler.html)
-
[Terms Component](query-guide/terms-component.html)
-
[Term Vector Component](query-guide/term-vector-component.html)
-
[Stats Component](query-guide/stats-component.html)
-
Controlling Results
-
[Faceting](query-guide/faceting.html)
-
[JSON Facet API](query-guide/json-facet-api.html)
-
[JSON Faceting Domain Changes](query-guide/json-faceting-domain-changes.html)
-
[Collapse and Expand Results](query-guide/collapse-and-expand-results.html)
-
[Result Grouping](query-guide/result-grouping.html)
-
[Result Clustering](query-guide/result-clustering.html)
-
[Highlighting](query-guide/highlighting.html)
-
[Query Elevation Component](query-guide/query-elevation-component.html)
-
[Document Transformers](query-guide/document-transformers.html)
-
[Response Writers](query-guide/response-writers.html)
-
[Exporting Result Sets](query-guide/exporting-result-sets.html)
-
[Pagination of Results](query-guide/pagination-of-results.html)
-
[Streaming Expressions](query-guide/streaming-expressions.html)
-
[Stream Source Reference](query-guide/stream-source-reference.html)
-
[Stream Decorator Reference](query-guide/stream-decorator-reference.html)
-
[Stream Evaluator Reference](query-guide/stream-evaluator-reference.html)
-
[Streaming Expressions and Math Expressions](query-guide/math-expressions.html)
-
[Visualization](query-guide/visualization.html)
-
[Getting Started](query-guide/math-start.html)
-
[Loading Data](query-guide/loading.html)
-
[Searching, Sampling and Aggregation](query-guide/search-sample.html)
-
[Transforming Data](query-guide/transform.html)
-
[Scalar Math](query-guide/scalar-math.html)
-
[Vector Math](query-guide/vector-math.html)
-
[Variables](query-guide/variables.html)
-
[Matrices and Matrix Math](query-guide/matrix-math.html)
-
[Text Analysis and Term Vectors](query-guide/term-vectors.html)
-
[Probability Distributions](query-guide/probability-distributions.html)
-
[Statistics](query-guide/statistics.html)
-
[Linear Regression](query-guide/regression.html)
-
[Curve Fitting](query-guide/curve-fitting.html)
-
[Time Series](query-guide/time-series.html)
-
[Interpolation, Derivatives and Integrals](query-guide/numerical-analysis.html)
-
[Digital Signal Processing](query-guide/dsp.html)
-
[Monte Carlo Simulations](query-guide/simulations.html)
-
[Machine Learning](query-guide/machine-learning.html)
-
[Graph](query-guide/graph.html)
-
[Computational Geometry](query-guide/computational-geometry.html)
-
[Log Analytics](query-guide/logs.html)
-
[Graph Traversal](query-guide/graph-traversal.html)
-
[Stream Request Handler API](query-guide/stream-api.html)
-
[Stream Screen](query-guide/stream-screen.html)
-
[Stream Tool](query-guide/stream-tool.html)
-
-
[Solr Upgrade Notes](upgrade-notes/solr-upgrade-notes.html)
-
[Major Changes in Solr 10](upgrade-notes/major-changes-in-solr-10.html)
-
[Major Changes in Solr 9](upgrade-notes/major-changes-in-solr-9.html)
-
[Major Changes in Solr 8](upgrade-notes/major-changes-in-solr-8.html)
-
[Major Changes in Solr 7](upgrade-notes/major-changes-in-solr-7.html)
-
[Major Changes in Solr 6](upgrade-notes/major-changes-in-solr-6.html)
-
-
[How To Contribute](how-to-contribute/how-to-contribute.html)
[](index.html)
- [Apache Solr](index.html)
- [Apache Solr Reference Guide](index.html)
10.0
[10.1-beta](../10_1/index.html)
[10.0](index.html)
[9.11](../9_11/index.html)
[9.10](../9_10/index.html)
[9.9](../9_9/index.html)
[9.8](../9_8/index.html)
[9.7](../9_7/index.html)
[9.6](../9_6/index.html)
[9.5](../9_5/index.html)
[9.4](../9_4/index.html)
[9.3](../9_3/index.html)
[9.2](../9_2/index.html)
[9.1](../9_1/index.html)
[9.0](../9_0/index.html)
[Edit this Page](https://github.com/apache/solr/tree/main/solr/solr-ref-guide/modules/ROOT/pages/index.adoc)
# Apache Solr Reference Guide
Welcome to Apache Solr™
Solr is the open source solution for search and analytics.
A fast open source search platform built on Apache Lucene™, Solr provides scalable indexing and search, as well as faceting, hit highlighting and advanced analysis/tokenization capabilities.
Solr is managed by the [Apache Software Foundation](http://www.apache.org/).
This Reference Guide is the official Solr documentation, written and published by Solr committers.
[Getting Started](getting-started/introduction.html)
[Deployment Guide](deployment-guide/solr-control-script-reference.html)
[Configuration Guide](configuration-guide/configuration-files.html)
Introductory concepts and tutorials.
Installation, monitoring, scaling, and deploying to production.
Tuning Solr’s configuration files for your use case.
[Indexing Guide](indexing-guide/schema-elements.html)
[Query Guide](query-guide/common-query-parameters.html)
[Upgrade Notes](upgrade-notes/solr-upgrade-notes.html)
Configuring Solr’s schema and indexing documents.
All aspects of Solr queries.
Change notes for Solr releases.
© Apache Software Foundation. All rights reserved.