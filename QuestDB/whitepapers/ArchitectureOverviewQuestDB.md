# Architecture Overview | QuestDB

- 来源: https://questdb.com/docs/architecture/questdb-architecture
- 归档时间: 2026-10-29
- 说明: 官方技术白皮书 / 架构文档的 Markdown 快照（由 HTML 转换，格式为自动生成）

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
- [Overview](/docs/architecture/questdb-architecture/)
- [Storage Engine](/docs/architecture/storage-engine/)
- [Memory Management](/docs/architecture/memory-management/)
- [Query Engine](/docs/architecture/query-engine/)
- [Time Series Optimizations](/docs/architecture/time-series-optimizations/)
- [Observability](/docs/architecture/observability/)
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
- Architecture
- Overview
On this page
# Architecture Overview
Copy as Markdown
QuestDB offers high-speed ingestion and low-latency analytics on time-series
data. It stores data in a three-tier architecture (streaming WAL files, local
binary storage, and local or remote storage in Parquet format) to improve
interoperability and avoid vendor lock-in.
WHERE symbol in ('AAPL', 'NVDA')
LATEST ON timestamp PARTITION BY symbol
CREATE MATERIALIZED VIEW 'trades_OHLC'
min(price) AS low
timestamp IN today()
SELECT spread_bps(bids[1][1], asks[1][1])
FROM read_parquet('trades.parquet')
SAMPLE BY 15m
Tier One : Hot ingest (WAL), durable by default
Incoming data is appended to the write-ahead log (WAL) with ultra-low latency. Writes are made durable before any processing, preserving order and surviving failures without data loss. The WAL is asynchronously shipped to object storage, so new replicas can bootstrap quickly and read the same history.
Tier Two : Real-time SQL on live data
Data is time-ordered and de-duplicated into QuestDB's native, time-partitioned columnar format and becomes immediately queryable. Power real-time analysis with vectorized, multi-core execution, streaming materialized views, and time-series SQL (e.g., ASOF JOIN, SAMPLE BY). The query planner spans tiers seamlessly.
Tier Three : Cold storage, open and queryable
Older data is automatically tiered to object storage in Apache Parquet. Query it in-place through QuestDB or use any tool that reads Parquet. This delivers predictable costs, interoperability with AI/ML tooling, and zero lock-in.
This document explains QuestDB's internal architecture.
## Key components[​](#key-components)
QuestDB is comprised of several key components:
-
[Storage engine](/docs/architecture/storage-engine/): Uses a
column-oriented design to ensure high I/O performance and low latency.
-
[Memory management and native integration](/docs/architecture/memory-management/):
The system leverages both memory mapping and explicit memory management
techniques, integrating native code for performance-critical tasks.
-
[Query engine](/docs/architecture/query-engine/): A custom SQL
parser, a just-in-time (JIT) compiler, and a vectorized execution engine
process data in table page frames for better CPU use.
-
[Time-series optimizations](/docs/architecture/time-series-optimizations/):
QuestDB is specifically designed for time-series, and it provides several
optimizations, such as a designated timestamp, sequential reads, materialized
views, and in-memory processing.
-
[Replication](/docs/high-availability/overview/): QuestDB Enterprise supports
high availability with read replicas and multi-primary configurations.
See [High Availability](/docs/high-availability/overview/) for details.
-
[Observability](/docs/architecture/observability/): QuestDB exposes
real-time metrics, health checks, and structured logs to monitor performance
and streamline diagnostics.
-
[Web console](/docs/getting-started/web-console/overview/): The engine includes
a web console for running SQL statements, bulk loading CSV files, and
displaying monitoring dashboards. QuestDB Enterprise supports single sign-on
(SSO) in the web console.
## Design patterns & best practices throughout the codebase[​](#design-patterns--best-practices-throughout-the-codebase)
-
Immutable data structures: The system favors immutability to avoid
concurrency issues and simplify state management.
-
Modular architecture: Each component (eg., storage, query processing,
ingestion, etc.) has well-defined interfaces that enhance maintainability and
decouple functionality.
-
Factory & builder patterns: These patterns are used to centralize
construction logic for complex objects such as SQL execution plans and storage
buffers.
-
Lazy initialization: Resource-intensive components initialize only when
needed to reduce startup overhead.
-
Rigorous testing & benchmarks:
[Unit tests, integration tests](https://github.com/questdb/questdb/tree/master/core/src/test),
and performance benchmarks ensure that new enhancements do not compromise
reliability or performance.
## Next up[​](#next-up)
Continue to [Storage Engine](/docs/architecture/storage-engine/) to learn how QuestDB stores and manages data on disk.
[Edit this page](https://github.com/questdb/documentation/edit/main/documentation/architecture/overview.mdx)
[Previous
Root directory](/docs/concepts/deep-dive/root-directory-structure/)[Next
Storage Engine](/docs/architecture/storage-engine/)
- [Key components](#key-components)
- [Design patterns & best practices throughout the codebase](#design-patterns--best-practices-throughout-the-codebase)
- [Next up](#next-up)
Need a hand? Join our vibrant [public Slack](https://slack.questdb.com/) and [Discourse forum](https://community.questdb.com) communities.
Copyright © 2026 QuestDB SOC 2 Type 2 Compliant [Privacy](/privacy-notice/)[Terms](/terms/) Cookie settings