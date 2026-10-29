# Apache Phoenix

- 来源: https://phoenix.apache.org/
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

[Apache Phoenix](/) Apache Phoenix Project [Overview](/)[Downloads](/downloads)[Mailing Lists](/mailing-lists)[News](/news)[Team](/team)[Who is Using](/who-is-using)[Recent Improvements](/recent-improvements)[Roadmap](/roadmap)[Security Model](/security-model)
Apache Phoenix Project
Documentation [Reference Guide](/docs)[Reference Guide (PDF)](/books/apache-phoenix-reference-guide.pdf)[Reference Guide (Dark PDF)](/books/apache-phoenix-reference-guide-dark-mode.pdf)[Release Notes](/release-notes)[Issues Tracking](/issues-tracking)[Source Repository](/source-repository)[Tech Talks](/tech-talks)[Presentations](/presentations)
Documentation
ASF [Apache Software Foundation](http://www.apache.org/foundation/)[License](https://www.apache.org/licenses/)[How Apache Works](http://www.apache.org/foundation/how-it-works.html)[Foundation Program](http://www.apache.org/foundation/sponsorship.html)[Sponsors](https://www.apache.org/foundation/sponsors)[Privacy Policy](https://privacy.apache.org/policies/privacy-policy-public.html)
ASF
Toggle theme
Toggle theme
Apache Phoenix Project [Overview](/)[Downloads](/downloads)[Mailing Lists](/mailing-lists)[News](/news)[Team](/team)[Who is Using](/who-is-using)[Recent Improvements](/recent-improvements)[Roadmap](/roadmap)[Security Model](/security-model)
Documentation [Reference Guide](/docs)[Reference Guide (PDF)](/books/apache-phoenix-reference-guide.pdf)[Reference Guide (Dark PDF)](/books/apache-phoenix-reference-guide-dark-mode.pdf)[Release Notes](/release-notes)[Issues Tracking](/issues-tracking)[Source Repository](/source-repository)[Tech Talks](/tech-talks)[Presentations](/presentations)
ASF [Apache Software Foundation](http://www.apache.org/foundation/)[License](https://www.apache.org/licenses/)[How Apache Works](http://www.apache.org/foundation/how-it-works.html)[Foundation Program](http://www.apache.org/foundation/sponsorship.html)[Sponsors](https://www.apache.org/foundation/sponsors)[Privacy Policy](https://privacy.apache.org/policies/privacy-policy-public.html)
# We Put SQL Back in NoSQL
Query HBase with standard SQL and JDBC. Low latency OLTP and operational analytics for Hadoop.
[Download Phoenix](/downloads)[Read Documentation](/docs)
## Why Phoenix
The trusted data platform for OLTP and operational analytics on Hadoop.
### Standard SQL & JDBC
Use familiar SQL queries and JDBC APIs with full ACID transaction capabilities.
### Millisecond Performance
Low latency performance for small queries or seconds for tens of millions of rows.
### Schema Flexibility
Schema-on-read flexibility from the NoSQL world leveraging HBase as backing store.
### Hadoop Ecosystem
Fully integrated with Spark, Hive, Pig, Flume, and Map Reduce.
## Use Cases
Proven patterns where Phoenix delivers value.
### Operational Analytics
Real-time SQL queries on operational data with ACID guarantees for business insights.
### Low Latency OLTP
Transactional workloads with millisecond response times and full ACID support.
### Multi-tenant Applications
Build SaaS applications with tenant isolation using views and dynamic columns.
### Secondary Indexing
Fast lookups on non-primary key columns with automatic index maintenance.
### Time-Series Data
SQL queries over time-series data with efficient storage and retrieval patterns.
### Data Integration
ETL pipelines with Spark, Hive, and Map Reduce for comprehensive data workflows.
What's New in 5.3.1
## Latest Phoenix Highlights
Recent capabilities now available in the 5.3.1 release.
[### DynamoDB-Compatible REST API
Point your DynamoDB SDK clients at Phoenix using the phoenix-adapters REST service — no application rewrite required.
Learn more](/docs/integrations/phoenix-dynamodb)[### Document Data: BSON
Native binary JSON column type with server-side projection, filtering, and atomic per-field updates.
Learn more](/docs/features/bson)[### Change Data Capture
Stream row-level changes as ordered, partitioned events — read with standard SQL, with full split/merge lineage.
Learn more](/docs/features/change-data-capture)[### Eventually Consistent Indexes
Move global secondary index maintenance off the write path for write-heavy workloads — higher throughput, bounded staleness, no query-side changes.
Learn more](/docs/features/eventually-consistent-indexes)
[See all features in 5.3.1](/recent-improvements#release-5-3-1)
## SQL Support
Phoenix takes your SQL query, compiles it into HBase scans, and orchestrates execution to produce JDBC result sets.
### Complete SQL Support
SELECT, FROM, WHERE, GROUP BY, HAVING, ORDER BY, and more. Full DML and DDL support.
### Optimized Execution
Queries compiled into HBase scans with coprocessors and custom filters for millisecond performance.
### JDBC Connection
Connect using standard JDBC URL: jdbc:phoenix:server1,server2:port
## A Vibrant Community
Apache Phoenix is a top-level Apache project with an active community of users and contributors. Join discussions, explore the language reference, and help shape the future of SQL on HBase.
[Mailing Lists](/mailing-lists)[Contribute](/source-repository)[Team](/team)
- [News & EventsLatest releases and community tech talks.](/news)
- [Who is Using PhoenixOrganizations running Phoenix in production.](/who-is-using)
- [Language ReferenceComplete SQL grammar, functions, and datatypes.](/docs/grammar)
## Getting Started
From download to production in a few simple steps.
### 1. Download
Grab the latest stable release and verify checksums.
[Learn more →](/downloads)
### 2. Read the Guide
Walk through cluster setup, schema design, and operations.
[Learn more →](/docs)
### 3. Connect a Client
Configure the JDBC client classpath and connection URL.
[Learn more →](/docs/fundamentals/client-classpath-and-jdbc-url)
Apache Phoenix
Open-source SQL skin over Apache HBase for low-latency transactional and analytical workloads at scale.
Project
- [Overview](/)
- [Downloads](/downloads)
- [Mailing Lists](/mailing-lists)
- [News](/news)
- [Team](/team)
- [Who is Using](/who-is-using)
- [Recent Improvements](/recent-improvements)
- [Roadmap](/roadmap)
- [Security Model](/security-model)
Documentation
- [Reference Guide](/docs)
- [Reference Guide (PDF)](/books/apache-phoenix-reference-guide.pdf)
- [Reference Guide (Dark PDF)](/books/apache-phoenix-reference-guide-dark-mode.pdf)
- [Release Notes](/release-notes)
- [Issues Tracking](/issues-tracking)
- [Source Repository](/source-repository)
- [Tech Talks](/tech-talks)
- [Presentations](/presentations)
ASF
- [Apache Software Foundation](http://www.apache.org/foundation/)
- [License](https://www.apache.org/licenses/)
- [How Apache Works](http://www.apache.org/foundation/how-it-works.html)
- [Foundation Program](http://www.apache.org/foundation/sponsorship.html)
- [Sponsors](https://www.apache.org/foundation/sponsors)
- [Privacy Policy](https://privacy.apache.org/policies/privacy-policy-public.html)
Copyright ©2007-2026 The Apache Software Foundation. All rights reserved. Apache Phoenix, Phoenix, Apache, the Apache Phoenix logo and the ASF logo are either registered trademarks or trademarks of the Apache Software Foundation. All other marks mentioned may be trademarks or registered trademarks of their respective owners.