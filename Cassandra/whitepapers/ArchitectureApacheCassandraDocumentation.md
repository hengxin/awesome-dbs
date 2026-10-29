# Architecture | Apache Cassandra Documentation

- 来源: https://cassandra.apache.org/doc/latest/architecture/
- 归档时间: 2026-10-29
- 说明: 官方技术白皮书 / 架构文档的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

[](https://bsky.app/profile/cassandra.apache.org)
[](https://www.linkedin.com/company/apache-cassandra/)
[](https://www.youtube.com/c/PlanetCassandra)
[](/)
-
Get Started
-
[Cassandra Basics](/_/cassandra-basics.html)
-
[Quickstart](/_/quickstart.html)
-
[Ecosystem](/_/ecosystem.html)
- [Documentation](/doc/latest/)
-
[Community](/_/community.html)
-
[Welcome](/_/community.html#code-of-conduct)
-
[Discussions](/_/community.html#discussions)
-
[Governance](/_/community.html#project-governance)
-
[Contribute](/_/community.html#how-to-contribute)
-
[Meet the Community](/_/community.html#meet-the-community)
-
[Catalyst Program](/_/cassandra-catalyst-program.html)
-
[Events](/_/events.html)
-
Learn
-
[Cassandra 5.0](/_/Apache-Cassandra-5.0-Moving-Toward-an-AI-Driven-Future.html)
-
[Case Studies](/_/case-studies.html)
-
[Resources](/_/resources.html)
-
[Blog](/_/blog.html)
- [Download Now](/_/download.html)
## Cassandra Documentation
#### Version:
5.0
-
-
[website](../../../../_/index.html)
-
-
[7.0](../../../7.0/index.html)
-
[6.0](../../../6.0/index.html)
-
[6.0-alpha2](../../../6.0-alpha2/index.html)
-
[5.0.9](../../../5.0.9/index.html)
-
[5.0.8](../../../5.0.8/index.html)
-
[5.0](../../index.html)
-
[4.1](../../../4.1/index.html)
-
[4.0](../../../4.0/index.html)
-
[3.11](../../../3.11/index.html)
-
-
[Main](../../index.html)
-
[Glossary](../../../../_/glossary.html)
-
[How to report bugs](#master@_:ROOT:bugs.adoc)
-
[Contact us](../../../../_/community.html)
-
[Development](../../../../_/development/index.html)
-
[Getting started](../../../../_/development/gettingstarted.html)
-
[Building and IDE integration](../../../../_/development/ide.html)
-
[Testing](../../../../_/development/testing.html)
-
[Contributing code changes](../../../../_/development/patches.html)
-
[Code style](../../../../_/development/code_style.html)
-
[Review checklist](../../../../_/development/how_to_review.html)
-
[How to commit](../../../../_/development/how_to_commit.html)
-
[Working on documentation](../../../../_/development/documentation.html)
-
[Jenkins CI environment](../../../../_/development/ci.html)
-
[Dependency management](../../../../_/development/dependencies.html)
-
[Release process](../../../../_/development/release_process.html)
-
-
Cassandra
-
[FAQ](../overview/faq/index.html)
-
[Getting Started](../getting-started/index.html)
-
[Cassandra Quickstart](../getting-started/cassandra-quickstart.html)
-
[SAI Quickstart](../getting-started/sai-quickstart.html)
-
[Vector Search Quickstart](../getting-started/vector-search-quickstart.html)
-
[Installing Cassandra](../installing/installing.html)
-
[Configuring Cassandra](../getting-started/configuring.html)
-
[Inserting and querying](../getting-started/querying.html)
-
[Client drivers](../getting-started/drivers.html)
-
[Production recommendations](../getting-started/production.html)
-
[What’s new](../new/index.html)
-
[Support for Java](../reference/java17.html)
-
[Architecture](index.html)
-
[Overview](overview.html)
-
[Dynamo](dynamo.html)
-
[Storage Engine](storage-engine.html)
-
[Guarantees](guarantees.html)
-
[Improved Internode Messaging](messaging.html)
-
[Improved Streaming](streaming.html)
-
[Data Modeling](../developing/data-modeling/index.html)
-
[Introduction](../developing/data-modeling/intro.html)
-
[Conceptual data modeling](../developing/data-modeling/data-modeling_conceptual.html)
-
[RDBMS design](../developing/data-modeling/data-modeling_rdbms.html)
-
[Defining application queries](../developing/data-modeling/data-modeling_queries.html)
-
[Logical data modeling](../developing/data-modeling/data-modeling_logical.html)
-
[Physical data modeling](../developing/data-modeling/data-modeling_physical.html)
-
[Evaluating and refining data models](../developing/data-modeling/data-modeling_refining.html)
-
[Defining database schema](../developing/data-modeling/data-modeling_schema.html)
-
[Cassandra data modeling tools](../developing/data-modeling/data-modeling_tools.html)
-
[Cassandra Query Language (CQL)](../developing/cql/index.html)
-
[Definitions](../developing/cql/definitions.html)
-
[Data types](../developing/cql/types.html)
-
[Data definition (DDL)](../developing/cql/ddl.html)
-
[Data manipulation (DML)](../developing/cql/dml.html)
-
[Dynamic Data Masking (DDM)](../developing/cql/dynamic-data-masking.html)
-
[Operators](../developing/cql/operators.html)
-
[Indexing concepts](../developing/cql/indexing/indexing-concepts.html)
-
[SAI Overview](../developing/cql/indexing/sai/sai-overview.html)
-
[Concepts](../developing/cql/indexing/sai/sai-concepts.html)
-
[SAI Quickstart](../getting-started/sai-quickstart.html)
-
[SAI FAQ](../developing/cql/indexing/sai/sai-faq.html)
-
[Working with SAI](../developing/cql/indexing/sai/sai-working-with.html)
-
[SAI operations](../developing/cql/indexing/sai/operations/sai-operations.html)
-
[Secondary indexes (2i) overview](../developing/cql/indexing/2i/2i-overview.html)
-
[Concepts](../developing/cql/indexing/2i/2i-concepts.html)
-
[Working with 2i](../developing/cql/indexing/2i/2i-working-with.html)
-
[Rebuild 2i](../developing/cql/indexing/2i/operations/2i-build.html)
-
[Materialized views](../developing/cql/mvs.html)
-
[Functions](../developing/cql/functions.html)
-
[JSON](../developing/cql/json.html)
-
[Security](../developing/cql/security.html)
-
[Triggers](../developing/cql/triggers.html)
-
[Appendices](../developing/cql/appendices.html)
-
[Changes](../developing/cql/changes.html)
-
[SASI](../developing/cql/SASI.html)
-
[Single file of CQL information](../developing/cql/cql_singlefile.html)
-
[Vector Search overview](../vector-search/overview.html)
-
[Concepts](../vector-search/concepts.html)
-
[Vector Search : Data Modeling](../vector-search/data-modeling.html)
-
[Vector Search Quickstart](../getting-started/vector-search-quickstart.html)
-
[Working with Vector Search](../vector-search/vector-search-working-with.html)
-
[Managing](../managing/index.html)
-
[Configuring](../managing/configuration/index.html)
-
[cassandra.yaml](../managing/configuration/cass_yaml_file.html)
-
[cassandra-rackdc.properties](../managing/configuration/cass_rackdc_file.html)
-
[cassandra-env.sh](../managing/configuration/cass_env_sh_file.html)
-
[cassandra-topologies.properties](../managing/configuration/cass_topo_file.html)
-
[commitlog-archiving.properties](../managing/configuration/cass_cl_archive_file.html)
-
[logback.xml](../managing/configuration/cass_logback_xml_file.html)
-
[jvm-* files](../managing/configuration/cass_jvm_options_file.html)
-
[Liberating cassandra.yaml Parameters' Names from Their Units](../managing/configuration/configuration.html)
-
[Operating](../managing/operating/index.html)
-
[Auto Repair](../managing/operating/auto_repair.html)
-
[Backups](../managing/operating/backups.html)
-
[Bloom filters](../managing/operating/bloom_filters.html)
-
[Bulk loading](../managing/operating/bulk_loading.html)
-
[Change Data Capture (CDC)](../managing/operating/cdc.html)
-
[Compaction](../managing/operating/compaction/index.html)
-
[Compression](../managing/operating/compression.html)
-
[Hardware](../managing/operating/hardware.html)
-
[Hints](../managing/operating/hints.html)
-
[Logging](../managing/operating/logging.html)
-
[Audit logging](../managing/operating/auditlogging.html)
-
[Audit logging 2](../managing/operating/audit_logging.html)
-
[Full query logging](../managing/operating/fqllogging.html)
-
[Monitoring metrics](../managing/operating/metrics.html)
-
[Repair](../managing/operating/repair.html)
-
[Read repair](../managing/operating/read_repair.html)
-
[Security](../managing/operating/security.html)
-
[Snitches](../managing/operating/snitch.html)
-
[Topology changes](../managing/operating/topo_changes.html)
-
[Transient replication](../managing/operating/transientreplication.html)
-
[Virtual tables](../managing/operating/virtualtables.html)
-
[Tools](../managing/tools/index.html)
-
[cqlsh: the CQL shell](../managing/tools/cqlsh.html)
-
[nodetool](../managing/tools/nodetool/nodetool.html)
-
[SSTable tools](../managing/tools/sstable/index.html)
-
[cassandra-stress](../tooling/cassandra-stress.html)
-
[Troubleshooting](../troubleshooting/index.html)
-
[Finding misbehaving nodes](../troubleshooting/finding_nodes.html)
-
[Reading Cassandra logs](../troubleshooting/reading_logs.html)
-
[Using nodetool](../troubleshooting/use_nodetool.html)
-
[Using external tools to deep-dive](../troubleshooting/use_tools.html)
-
[Reference](../reference/index.html)
-
[CQL commands](../reference/cql-commands/commands-toc.html)
-
[CQL specification](../developing/cql/cql_singlefile.html)
-
[Java 17](../reference/java17.html)
-
[Native Protocol specification](../reference/native-protocol.html)
-
[SAI virtual table](../reference/sai-virtual-table-indexes.html)
-
[Static columns](../reference/static.html)
-
[Vector data type](../reference/vector-data-type.html)
-
[Plug-ins](../integrating/plugins/index.html)
You are viewing the documentation for a prerelease version.
[View Latest](../../../6.0-alpha2/cassandra/architecture/index.html)
- Cassandra
- [Architecture](index.html)
- [Edit](https://github.com/apache/cassandra/edit/cassandra-5.0/doc/modules/cassandra/pages/architecture/index.adoc)
# Architecture
This section describes the general architecture of Apache Cassandra.
-
[Overview](overview.html)
-
[Dynamo](dynamo.html)
-
[Storage Engine](storage-engine.html)
-
[Guarantees](guarantees.html)
-
[Snitches](../managing/operating/snitch.html)
## Get started with Cassandra, fast.
[Quickstart Guide](/_/quickstart.html)
Apache Cassandra powers mission-critical deployments with improved performance and unparalleled levels of scale in the cloud.
[](https://bsky.app/profile/cassandra.apache.org)
[](https://www.linkedin.com/company/apache-cassandra/)
[](https://www.youtube.com/c/PlanetCassandra)
- [Home](/)
- [Cassandra Basics](/_/cassandra-basics.html)
- [Quickstart](/_/quickstart.html)
- [Ecosystem](/_/ecosystem.html)
- [Documentation](/doc/latest/)
- [Community](/_/community.html)
- [Case Studies](/_/case-studies.html)
- [Resources](/_/resources.html)
- [Blog](/_/blog.html)
[Foundation](http://www.apache.org/)
[Events](https://www.apache.org/events/current-event.html)
[License](https://www.apache.org/licenses/)
[Thanks](https://www.apache.org/foundation/thanks)
[Security](https://www.apache.org/security)
[Privacy](https://privacy.apache.org/policies/privacy-policy-public.html)
[Sponsorship](https://www.apache.org/foundation/sponsorship)
© 2009- [The Apache Software Foundation](https://apache.org) under the terms of the Apache License 2.0. Apache, the Apache feather logo, Apache Cassandra, Cassandra, and the Cassandra logo, are either registered trademarks or trademarks of The Apache Software Foundation.