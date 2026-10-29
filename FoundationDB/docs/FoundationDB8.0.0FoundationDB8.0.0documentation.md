# FoundationDB 8.0.0 — FoundationDB 8.0.0 documentation

- 来源: https://apple.github.io/foundationdb/
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

[FoundationDB](#)
8.0.0
- [Site Map](contents.html)
-
[Site](#)
-
[Page](#)
- [FoundationDB 8.0.0](#)
- [Overview](#overview)
- [Documentation](#documentation)
-
[Developer Tools »](developer-tools.html)
- [FoundationDB 8.0.0](#)
- [Overview](#overview)
- [Documentation](#documentation)
# FoundationDB 8.0.0
## Overview
FoundationDB is a distributed database designed to handle large volumes of structured data across clusters of commodity servers. It organizes data as an ordered key-value store and employs [ACID transactions](transaction-manifesto.html) for all operations. It is especially well-suited for read/write workloads but also has excellent [performance](performance.html) for write-intensive workloads. Users interact with the database using a [API language binding](api-reference.html). You can [begin local development](local-dev.html) today.
## Documentation
FoundationDB is a robust choice for a broad range of use cases:
Developers can store all types of data. FoundationDB is multi-model, meaning you can store many types of data in a single database. All data is safely stored, distributed, and replicated in FoundationDB.
Administrators easily scale and handle hardware failures. FoundationDB is easy to install, grow, and manage. It has a distributed architecture that gracefully scales out and handles faults while acting like a single ACID database.
FoundationDB has industry-leading performance. FoundationDB provides amazing performance on commodity hardware, allowing you to support very heavy loads at low cost.
FoundationDB supports flexible application architectures. Your application can talk directly to FoundationDB, to a layer, or both. Layers provide new capability on top of FoundationDB but are stateless.
The latest released changes are detailed in [Release Notes](release-notes/release-notes-740.html#release-notes).
The documentation has the following sections:
- [Why FoundationDB](why-foundationdb.html) describes the technical alternatives involved in NoSQL database design and explains the advantages of transaction processing at scale.
- [Technical Overview](technical-overview.html) explains the engineering design of FoundationDB, with detailed information on its features, architecture, and performance.
- [Client Design](client-design.html) contains documentation on getting started, data modeling, and design principles for building applications with FoundationDB.
- [Design Recipes](design-recipes.html) give specific examples of how to build new data models, indexes, and more on top of the key-value store API.
- [API Reference](api-reference.html) give a detailed description of the API for each language.
- [Tutorials](tutorials.html) provide simple examples of client design using FoundationDB.
- [Administration](administration.html) contains documentation on administering FoundationDB.
- [Monitored Metrics](monitored-metrics.html) contains documentation on monitoring and alerting for FoundationDB.
- [Redwood Storage Engine](redwood.html) contains documentation on Redwood Storage Engine.
- [Visibility Documents](visibility.html) contains documentation related to Visibility into FoundationDB.
- [Developer Tools](developer-tools.html) contains documentation for FoundationDB contributors, including local development setup, static analysis, and internal testing tools.
[Back to top](#)
[Source](_sources/index.rst.txt)
© Copyright 2013-2025 Apple, Inc and the FoundationDB project authors.
Last updated on Oct 02, 2026.