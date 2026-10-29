# Valkey &middot; Topics

- 来源: https://valkey.io/topics/
- 归档时间: 2026-10-29
- 说明: 官方技术白皮书 / 架构文档的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

[](/)
[Download](/download/)
[Documentation](/docs/)
[Command Reference](/commands/)
[Documentation by Topic](/topics/)
[Clients](/clients/)
[Integrations](/integrations/)
[Blog](/blog/)
[Community](/community/)
[Events](/events/)
[Planet](https://planet.valkey.io/)
[Participants](/participants/)
[Try Valkey](/try-valkey/)
[GitHub](https://github.com/valkey-io)
# Documentation by Topic
The Valkey documentation is managed in markdown files in the
[valkey-doc repository](https://github.com/valkey-io/valkey-doc).
It's released under the
[Creative Commons Attribution-ShareAlike 4.0 International license](https://creativecommons.org/licenses/by-sa/4.0/).
# Valkey Documentation
## 1. Introduction
- What is Valkey? See [Introduction](/topics/introduction).
- [Quick start](/topics/quickstart): Get started with Valkey.
- [Valkey Bundle](/topics/valkey-bundle): Get started with Valkey Bundle.
- [FAQ](/topics/faq): Frequently asked questions.
## 2. Developer Guide
### Core Concepts
- [Data types](/topics/data-types): Keys are strings, but values can be of many different data types.
- [The full list of commands](/commands/), with documentation for each of them.
- [Pipelining](/topics/pipelining): How to send multiple commands at once, saving on round trip time.
- [Transactions](/topics/transactions): Valkey's approach to atomic transactions.
- [Expires](/commands/expire): How to set a Time To Live (TTL) on key so that it will be automatically removed from the server when it expires.
- [Pub/Sub](/topics/pubsub): Using Valkey as a message broker using the Publish/Subscribe messaging system.
- [Keyspace notifications](/topics/notifications): Get notifications of keyspace events via Pub/Sub.
- [Keyspace management](/topics/keyspace): How to alter, query, and navigate the keyspace.
### Application Patterns & Tutorials
- [Valkey as an LRU cache](/topics/lru-cache): How to configure Valkey as a cache with a fixed amount of memory and automatic eviction of keys.
- [Client side caching](/topics/client-side-caching): How a client can be notified by the server when a key has changed.
- [Distributed locks](/topics/distlock): Implementing a distributed lock manager.
- [Secondary indexes](/topics/indexing): How to simulate secondary indexes, composed indexes and traverse graphs using various data structures.
- [Writing a simple Twitter clone with PHP and Valkey](/topics/twitter-clone)
## 3. Extending Valkey
### Server-side scripting in Valkey
- [Programmability overview](/topics/programmability): An overview of programmability in Valkey.
- [Introduction to Eval Scripts](/topics/eval-intro): An introduction about using cached scripts.
- [Introduction to Valkey Functions](/topics/functions-intro): An introduction about using functions.
- [Valkey Lua API](/topics/lua-api): The embedded [Lua 5.1](https://lua.org) interpreter runtime environment and APIs.
- [Debugging Lua scripts](/topics/ldb): An overview of the native Valkey Lua debugger for cached scripts.
### Valkey modules API
- [Introduction to Valkey modules](/topics/modules-intro): Extend Valkey using dynamically linked modules.
- [Implementing native data types](/topics/modules-native-types): Modules scan implement new data types (data structures and more) that look like built-in data types. This documentation covers the API to do so.
- [Blocking operations](/topics/modules-blocking-ops): Write commands that can block the client (without blocking Valkey) and can execute tasks in other threads.
- [Modules API reference](/topics/modules-api-ref): Documentation of all module API functions. Low level details about API usage.
## 4. Administration
### Core Management
- [License](/topics/license): License information for Valkey.
- [Installation](/topics/installation): How to install and configure Valkey. This targets people without prior experience with Valkey.
- [Release Downloads](https://valkey.io/download/releases/): Lists links to download all current and previous releases.
- [valkey-cli](/topics/cli): The Valkey command line interface, used for administration, troubleshooting and experimenting with Valkey.
- [valkey-server](/topics/server): How to run the Valkey server.
- [Configuration](/topics/valkey.conf): How to configure Valkey.
- [Persistence](/topics/persistence): Options for configuring durability using disk backups.
- [Signals Handling](/topics/signals): How Valkey handles signals.
- [Connections Handling](/topics/clients): How Valkey handles clients connections.
- [Migration](/topics/migration): How to migrate from Redis to Valkey and check Redis compatibility.
- [Releases and Versioning](/topics/releases): Valkey's development cycle and version numbering.
- [Administration](/topics/admin): Various administration topics.
### Deployment Topology
- [Replication](/topics/replication): What you need to know to set up primary-replica replication.
- [Sentinel](/topics/sentinel): Valkey Sentinel is one of the official high availability deployment modes.
- [Sentinel client spec](/topics/sentinel-clients): How to build clients for Valkey Sentinel.
- [Cluster tutorial](/topics/cluster-tutorial): A gentle introduction to Valkey Cluster, a deployment mode for horizontal scaling and high availability.
- [Cluster specification](/topics/cluster-spec): The more formal description of the behavior and algorithms used in Valkey Cluster.
- [Atomic slot migration](/topics/atomic-slot-migration): An overview of atomic slot migration in Valkey Cluster.
### Security
- [Security](/topics/security): An overview of Valkey's security.
- [Access Control Lists](/topics/acl): ACLs make it possible to allow users to run only selected commands and access only specific key patterns.
- [TLS](/topics/tls): How to use TLS for communication.
### Platform Specific
- [ARM and Raspberry Pi](/topics/ARM): ARM and the Raspberry Pi are supported platforms. This page contains general information and benchmarks.
- [RDMA](/topics/RDMA): An overview of RDMA support.
## 5. Performance & Troubleshooting
- [Troubleshooting](/topics/problems): Problems? Bugs? High latency? Other issues? Use our problems troubleshooting page as a starting point to find more information.
- [Memory optimization](/topics/memory-optimization): Understand how Valkey uses RAM.
- [Latency monitoring](/topics/latency-monitor): Integrated latency monitoring and reporting help tuning for low latency.
- [valkey-benchmark](/topics/benchmark): The benchmarking tool shipped with Valkey.
- [On-CPU profiling and tracing](/topics/performance-on-cpu): How to find on-CPU resource bottlenecks.
- [Debugging](/topics/debugging): How to debug Valkey server processes.
- [Diagnosing latency issues](/topics/latency): How to diagnose latency problems with Valkey.
- [Mass insertion of data](/topics/mass-insertion): How to add a big amount of data to a Valkey instance in a short time.
## 6. Low-Level Internals
- [Protocol specification](/topics/protocol): The client-server protocol, for client authors.
- [Command key specifications](/topics/key-specs): How to extract the names of keys accessed by every command.
- [Command tips](/topics/command-tips): Command tips communicate non-trivial execution modes and post-processing information about commands.
- [Command arguments](/topics/command-arguments): An overview of command arguments as returned by the COMMAND DOCS command.
## Alphabetical Index
-
[ACL
Valkey Access Control List](/topics/acl/)
-
[ARM support
Exploring Valkey on the ARM CPU Architecture](/topics/ARM/)
-
[Administration
Advice for configuring and managing Valkey in production](/topics/admin/)
-
[Atomic slot migration
Overview of atomic slot migration](/topics/atomic-slot-migration/)
-
[Benchmarking tool
Using the valkey-benchmark utility on a Valkey server](/topics/benchmark/)
-
[Bitfields
Introduction to Bitfields](/topics/bitfields/)
-
[Bitmaps
Introduction to Bitmaps](/topics/bitmaps/)
-
[Bloom Filters
Introduction to Bloom Filters](/topics/bloomfilters/)
-
[Bulk loading
Writing data in bulk using the RESP protocol](/topics/mass-insertion/)
-
[CLI
Valkey command line interface](/topics/cli/)
-
[CPU profiling
Performance engineering guide for on-CPU profiling and tracing](/topics/performance-on-cpu/)
-
[Client handling
How the Valkey server manages client connections](/topics/clients/)
-
[Client-side caching
Server-assisted, client-side caching in Valkey](/topics/client-side-caching/)
-
[Cluster specification
Detailed specification for Valkey cluster](/topics/cluster-spec/)
-
[Cluster tutorial
Horizontal scaling with Valkey Cluster](/topics/cluster-tutorial/)
-
[Command arguments
How Valkey commands expose their documentation programmatically](/topics/command-arguments/)
-
[Command key specifications
What are command key specification and how to use them in your client](/topics/key-specs/)
-
[Command tips
Get additional information about a command](/topics/command-tips/)
-
[Configuration
Overview of valkey.conf, the Valkey configuration file](/topics/valkey.conf/)
-
[Data types
Overview of data types supported by Valkey](/topics/data-types/)
-
[Debugging
A guide to debugging Valkey server processes](/topics/debugging/)
-
[Debugging Lua scripts
How to use the built-in Lua debugger](/topics/ldb/)
-
[Diagnosing latency issues
Finding the causes of slow responses](/topics/latency/)
-
[Distributed Locks
A distributed lock pattern with Valkey](/topics/distlock/)
-
[FAQ
Commonly asked questions when getting started with Valkey](/topics/faq/)
-
[Functions
Scripting with functions stored on the server](/topics/functions-intro/)
-
[Geospatial
Introduction to the Valkey Geospatial data type](/topics/geospatial/)
-
[Hashes
Introduction to Hashes](/topics/hashes/)
-
[High availability with Valkey Sentinel
High availability for non-clustered Valkey](/topics/sentinel/)
-
[History
How the Valkey project started](/topics/history/)
-
[HyperLogLog
HyperLogLog is a probabilistic data structure that estimates the cardinality of a set.](/topics/hyperloglogs/)
-
[Installation
Install Valkey on Linux, macOS, and Windows](/topics/installation/)
-
[Introduction
Learn about the Valkey open source project](/topics/introduction/)
-
[Key eviction
Overview of Valkey key eviction policies (LRU, LFU, etc.)](/topics/lru-cache/)
-
[Keyspace
Managing keys in Valkey: Key expiration, scanning, altering and querying the key space](/topics/keyspace/)
-
[Keyspace notifications
Monitor changes to Valkey keys and values in real time](/topics/notifications/)
-
[LDAP Authentication
Introduction to LDAP / Active Directory Authentication](/topics/ldap/)
-
[Latency monitoring
Discovering slow server events in Valkey](/topics/latency-monitor/)
-
[License
License and trademark information](/topics/license/)
-
[Lists
Introduction to Lists](/topics/lists/)
-
[Lua API reference
Executing Lua in Valkey](/topics/lua-api/)
-
[Memory optimization
Strategies for optimizing memory usage in Valkey](/topics/memory-optimization/)
-
[Migration from Redis to Valkey
How to migrate from Redis to Valkey and check Redis compatibility](/topics/migration/)
-
[Modules API for native types
How to use native types in a Valkey module](/topics/modules-native-types/)
-
[Modules API reference
Reference for the Valkey Modules API](/topics/modules-api-ref/)
-
[Modules Introduction
Introduction to writing Valkey modules](/topics/modules-intro/)
-
[Modules and blocking commands
How to implement blocking commands in a Valkey module](/topics/modules-blocking-ops/)
-
[Patterns example
Learn several Valkey patterns by building a Twitter clone](/topics/twitter-clone/)
-
[Persistence
How Valkey writes data to disk](/topics/persistence/)
-
[Pipelining
How to optimize round-trip times by batching Valkey commands](/topics/pipelining/)
-
[Programmability
Extending Valkey with Lua and Valkey Functions](/topics/programmability/)
-
[Pub/Sub
How to use pub/sub channels in Valkey](/topics/pubsub/)
-
[Quick start guide
Understand how to use basic Valkey data types](/topics/quickstart/)
-
[RDMA experimental support
Valkey Over RDMA experimental support](/topics/RDMA/)
-
[Releases and versioning schema
How new versions of Valkey are released and supported](/topics/releases/)
-
[Replication
How Valkey supports high availability and failover with replication](/topics/replication/)
-
[Scripting with Lua
Executing Lua in Valkey](/topics/eval-intro/)
-
[Secondary indexing
Building secondary indexes in Valkey](/topics/indexing/)
-
[Security
Security model and features in Valkey](/topics/security/)
-
[Sentinel client spec
How to build clients for Valkey Sentinel](/topics/sentinel-clients/)
-
[Serialization protocol specification
Valkey's serialization protocol (RESP) is the wire protocol that clients implement](/topics/protocol/)
-
[Sets
Introduction to Sets](/topics/sets/)
-
[Signal handling
How Valkey handles common Unix signals](/topics/signals/)
-
[Sorted Sets
Introduction to Sorted Sets](/topics/sorted-sets/)
-
[Streams
Introduction to Streams](/topics/streams-intro/)
-
[Strings
Introduction to Strings](/topics/strings/)
-
[TLS
Valkey TLS support](/topics/tls/)
-
[The Valkey server
Manual for valkey-server, the Valkey server program](/topics/server/)
-
[Transactions
How transactions work in Valkey](/topics/transactions/)
-
[Troubleshooting Valkey
Problems with Valkey? Start here.](/topics/problems/)
-
[Valkey Bundle Getting Started Guide
How to get started with Valkey Bundle](/topics/valkey-bundle/)
-
[Valkey JSON
Introduction to Valkey JSON](/topics/valkey-json/)
-
[Valkey Search - Aggregation Expressions
Valkey Search Module Aggregation Expression Language](/topics/search-expressions/)
-
[Valkey Search - Configuration
Valkey Search Module Configurable Settings](/topics/search-configurables/)
-
[Valkey Search - Data Formats
Valkey Search Module Formats for Input Field Data](/topics/search-data-formats/)
-
[Valkey Search - INFO SEARCH Metrics
Valkey Search Module INFO SEARCH Metrics](/topics/search-observables/)
-
[Valkey Search - Metrics and configurations
Valkey Search Module INFO SEARCH](/topics/search-monitoring/)
-
[Valkey Search - Overview
Valkey Search Module Overview](/topics/search/)
-
[Valkey Search - Queries
Valkey Search Module Query Language Syntax, Semantics and Examples](/topics/search-query/)
[Slack](https://valkey.io/slack)
[GitHub](https://github.com/valkey-io)
[LinkedIn](https://www.linkedin.com/company/valkey/)
[X.com](https://x.com/valkey_io)
[YouTube](https://www.youtube.com/@valkeyproject)
[Connect](/connect)
[Code of Conduct](/code_of_conduct)
[Meetup Groups](/community/meetup-groups/)
[Forum](https://github.com/orgs/valkey-io/discussions)
[Planet](https://planet.valkey.io/)
[About](/about)
[Leadership](/leadership)
[FAQ](/topics/faq)
## Subscribe for updates, event info, and the latest Valkey news
Stay connected with everything happening in the Valkey ecosystem: news, community stories, updates, and opportunities to get involved.
Subscriptions are open to all, so invite a friend or teammate. Thanks for joining and happy reading!
© Valkey contributors.
Valkey and the Valkey logo are trademarks of LF Projects, LLC.
[Trademark Policy](https://lfprojects.org/policies/trademark-policy/).
[Privacy Policy](https://lfprojects.org/policies/privacy-policy/).
[Terms of Use](https://lfprojects.org/policies/terms-of-use/).
For other policies, please see [lfprojects.org](https://lfprojects.org/).
Valkey includes certain 3-Clause BSD-licensed Redis code from Redis Ltd. and other source code. Redis Ltd. is
not the source of that other source code. Redis is a registered trademark of Redis Ltd.
Logo design by [Ziyang.](https://github.com/dizys)