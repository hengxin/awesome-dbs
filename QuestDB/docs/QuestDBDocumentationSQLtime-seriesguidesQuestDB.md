# QuestDB Documentation: SQL time-series guides | QuestDB

- 来源: https://questdb.com/docs/
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

For AI agents: the complete documentation index is at [llms.txt](https://questdb.com/docs/llms.txt). Every page is also available as markdown by appending .md to its URL, or by sending an Accept: text/markdown request header.
- [](https://questdb.com/)[Return to QuestDB.com](https://questdb.com/)[Documentation](/docs/)[Tutorials](https://questdb.com/blog/?tag=tutorial)[Blog](https://questdb.com/blog/)[QuestDB Enterprise](https://questdb.com/enterprise/)[Free Enterprise trial](https://questdb.com/enterprise/trial/)[Public Slack](https://slack.questdb.com/)[Discourse Community](https://community.questdb.com/)[View QuestDB Repo](https://github.com/questdb/questdb/)
[⚡️ QuestDB Enterprise](https://questdb.com/enterprise/) - [Enterprise overview](https://questdb.com/enterprise/)
- [Free 30-day trial](https://questdb.com/enterprise/trial/)
[10.1.0| 17.5k](https://github.com/questdb/questdb/) - [Release Notes](https://questdb.com/release-notes?ref=docs)
- [Roadmap](https://github.com/orgs/questdb/projects/1/views/5)
Search
- [Introduction](/docs/)
- [Schema design](/docs/schema-design-essentials/)
- [Getting Started](/docs/getting-started/quick-start/)
- [Connect](/docs/connect/overview/)
- [SQL Reference](/docs/query/overview/)
- [Web Console](/docs/getting-started/web-console/overview/)
- [Concepts](/docs/concepts/designated-timestamp/)
- [Architecture](/docs/architecture/questdb-architecture/)
- [Configuration](/docs/configuration/overview/)
- [Security](/docs/security/governance/)
- [High Availability](/docs/high-availability/overview/)
- [Operations](/docs/operations/upgrade/)
- [Deployment](/docs/deployment/docker/)
- [Integrations](/docs/integrations/overview/)
- [Tutorials & Cookbook](/docs/cookbook/sql/finance/post-trade-overview/)
- [Troubleshooting](/docs/troubleshooting/faq/)
- [Changelog](/docs/changelog/)
- [Release Notes](https://questdb.com/release-notes)
- [](/docs/)
- Introduction
On this page
Copy as Markdown
# Introduction
QuestDB is an open source time-series database engineered for low latency. It uses a column-oriented, time-partitioned storage engine with memory-mapped files and vectorized (SIMD) execution to support high-throughput ingestion and millisecond-level analytical queries. The system is built from scratch with a zero-GC Java core and focused C++/Rust components, in a compact codebase optimized for cache locality and predictable tail latency. SQL is extended with time-series operators such as SAMPLE BY , LATEST ON , ASOF JOIN , WINDOW JOIN , and HORIZON JOIN . ASOF JOIN alone has several execution algorithms, and the engine picks one based on the shape of the data. See [Architecture](https://questdb.com/docs/architecture/questdb-architecture/) for details.
[Quick start](/docs/getting-started/quick-start/)[Live demo](https://demo.questdb.io)[Test your skills](https://questdb.com/quiz/)
## About this documentation[​](#about-this-documentation)
This documentation covers both QuestDB Open Source and QuestDB Enterprise .
QuestDB Enterprise builds on top of QuestDB Open Source, using it as its core
library. Everything in open source works in Enterprise, but not the other way
around. Enterprise adds features like high availability, advanced security, RBAC,
automated backups, and multi-tier storage with seamless object storage integration.
## Get started[​](#get-started)
- [Quick start](/docs/getting-started/quick-start/) - Install and run QuestDB
- [Schema design](/docs/schema-design-essentials/) - Design your tables
- [Ingest data](/docs/connect/overview/) - Bring your data using QuestDB clients
- [Query data](/docs/query/overview/) - Analyze with SQL
## Guides[​](#guides)
### Create database
Set up your first QuestDB database and start storing time-series data.
[Read more](/docs/getting-started/create-database/)
### Capacity planning
Select a storage medium, plan, size and compress your QuestDB deployment.
[Read more](/docs/getting-started/capacity-planning/)
### Working with time
It's about time. Learn how to work with timestamps and timezones in QuestDB.
[Read more](/docs/concepts/timestamps-timezones/)
### Backup and restore
See the methods to backup and restore your QuestDB deployment.
[Read more](/docs/operations/backup/)
## Resources[​](#resources)
### [Query overview](/docs/query/overview/)
Learn about our powerful extended SQL and how to use it to query QuestDB.
### [Language clients](/docs/connect/overview/#client-libraries)
Explore our language clients and how to use them to ingest data into QuestDB.
### [Configuration](/docs/configuration/overview/)
See all of our available configuration options and fine-tune to match your use case.
### [Third-Party Tools](/docs/integrations/overview/)
Our recommended third-party tools can aid you in analyzing and visualizing your data.
[Next
Schema design](/docs/schema-design-essentials/)
- [About this documentation](#about-this-documentation)
- [Get started](#get-started)
- [Guides](#guides)
- [Resources](#resources)
Need a hand? Join our vibrant [public Slack](https://slack.questdb.com/) and [Discourse forum](https://community.questdb.com) communities.
Copyright © 2026 QuestDB SOC 2 Type 2 Compliant [Privacy](/privacy-notice/)[Terms](/terms/) Cookie settings