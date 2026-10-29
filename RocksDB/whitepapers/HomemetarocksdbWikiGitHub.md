# Home · meta/rocksdb Wiki · GitHub

- 来源: https://github.com/facebook/rocksdb/wiki/Architecture
- 归档时间: 2026-10-29
- 说明: 官方技术白皮书 / 架构文档的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

[Skip to content](#start-of-content)
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
- - - - - - -
## Navigation Menu
[](/)
[Sign in](/login?return_to=https%3A%2F%2Fgithub.com%2Fmeta%2Frocksdb%2Fwiki%2F)
- Products - Platform - [GitHubRepository hosting, code review, and collaboration](https://github.com/platform)
- [CopilotAI coding agent for tasks, projects and automated work](https://github.com/features/copilot)
- Build & Ship - [ActionsCI/CD and automation](https://github.com/features/actions)
- [Code QualityQuality analysis, fixes, and enforcement](https://github.com/features/code-quality)
- [CodespacesCloud development environments](https://github.com/features/codespaces)
- Secure - [Code SecurityVulnerability detection and remediation](https://github.com/security/advanced-security/code-security)
- [Secret ProtectionSecret scanning and leak prevention](https://github.com/security/advanced-security/secret-protection)
[All Features](https://github.com/features)
- Developers - Learn - [Documentation](https://docs.github.com/en)
- [Training](https://learn.github.com/skills)
- [Certifications](https://learn.github.com/credentials)
- Build - [Build with Copilot](https://github.com/features/ai)
- [Customize Copilot](https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/customize-copilot-overview)
- [Integrations](https://github.com/marketplace)
- Explore - [Trending repos](https://github.com/trending)
- [GitHub Sponsors](https://github.com/open-source/sponsors)
- [Events](https://github.com/resources/events)
- Changelog - [Changelog Your source for the latest features, improvements, and fixes across GitHub products, all in one place.](https://github.blog/changelog/)
- Businesses - By Stage - [Enterprises](https://github.com/enterprise)
- [Team](https://github.com/team)
- [Startups](https://github.com/enterprise/startups)
- [Nonprofits](https://github.com/solutions/industry/nonprofits)
- By Industry - [Healthcare](https://github.com/solutions/industry/healthcare)
- [Financial services](https://github.com/solutions/industry/financial-services)
- [Manufacturing](https://github.com/solutions/industry/manufacturing)
- [Government](https://github.com/solutions/industry/government)
- [See all industries](https://github.com/solutions/industry)
- Evaluate GitHub - [Why GitHub](https://github.com/why-github)
- [Customer Stories](https://github.com/customer-stories)
- [Business insights](https://github.com/solutions/executive-insights)
- [Trust Center](https://github.com/trust-center)
- Add-ons - [GitHub Advanced SecurityEnterprise-grade code security](https://github.com/security/advanced-security)
- [Copilot for businessEnterprise-grade AI features](https://github.com/features/copilot/copilot-business)
- [Premium SupportEnterprise-grade 24/7 support](https://github.com/enterprise/premium-support)
- Resources - Learn & Connect - [Documentation](https://docs.github.com/en)
- [Resource center](https://github.com/resources)
- [Blog](https://github.blog/)
- [Events & webinars](https://github.com/resources/events)
- [Community Forum](https://github.com/orgs/community/discussions)
- [Customer Stories](https://github.com/customer-stories)
- [Integrations](https://github.com/marketplace)
- Support - [Customer support](https://help.github.com/)
- [Training](https://learn.github.com/skills)
- [GitHub Status](https://www.githubstatus.com/)
- Company - [About](https://github.com/about)
- [Partners](https://github.com/partners)
- [Changelog](https://github.blog/changelog/)
- GitHub Universe - [GitHub Universe The event for developers, by developers — talks, workshops, and what’s next for GitHub.](https://githubuniverse.com/)
- [Pricing](https://github.com/pricing)
Search /
[Sign in](/login?return_to=https%3A%2F%2Fgithub.com%2Fmeta%2Frocksdb%2Fwiki%2F)
[Sign up](/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F%3Cuser-name%3E%2F%3Crepo-name%3E%2Fwiki%2Findex&source=header-repo&source_repo=meta%2Frocksdb) Appearance settings
You signed in with another tab or window. Reload to refresh your session.
You signed out in another tab or window. Reload to refresh your session.
You switched accounts on another tab or window. Reload to refresh your session.
Dismiss alert
{{ message }}
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
- [meta](/meta)
- [rocksdb](/meta/rocksdb)
## Repository navigation
-
- [Code](/meta/rocksdb)
- [Issues975 ( 975 )](/meta/rocksdb/issues)
- [Pull requests833 ( 833 )](/meta/rocksdb/pulls)
- [Discussions](/meta/rocksdb/discussions)
- [Actions](/meta/rocksdb/actions)
- [Projects](/meta/rocksdb/projects)
- [Wiki](/meta/rocksdb/wiki)
- [Security and quality](/meta/rocksdb/security)
- [Insights](/meta/rocksdb/pulse)
More items
# Home
[Jump to bottom](#wiki-pages-box)
ics091 edited this page Jun 14, 2023
·
[61 revisions](/meta/rocksdb/wiki/Home/_history)
# Welcome to RocksDB
[](#welcome-to-rocksdb)
RocksDB is a storage engine with key/value interface, where keys and values are arbitrary byte streams. It is a C++ library. It was developed at Facebook based on LevelDB and provides backwards-compatible support for LevelDB APIs.
RocksDB supports various storage hardware, with fast flash as the initial focus. It uses a Log Structured Database Engine for storage, is written entirely in C++, and has a Java wrapper called RocksJava. See [RocksJava Basics](/meta/rocksdb/wiki/RocksJava-Basics).
RocksDB can adapt to a variety of production environments, including pure memory, Flash, hard disks or remote storage. Where RocksDB cannot automatically adapt, highly flexible configuration settings are provided to allow users to tune it for them. It supports various compression algorithms and good tools for production support and debugging.
## Features
[](#features)
- Designed for application servers wanting to store up to a few terabytes of data on local or remote storage systems.
- Optimized for storing small to medium size key-values on fast storage -- flash devices or in-memory
- It works well on processors with many cores
## Features Not in LevelDB
[](#features-not-in-leveldb)
RocksDB introduces dozens of new major features. See [the list of features not in LevelDB](https://github.com/facebook/rocksdb/wiki/Features-Not-in-LevelDB).
## Getting Started
[](#getting-started)
For a complete Table of Contents, see the sidebar to the right. Most readers will want to start with the [Overview](https://github.com/facebook/rocksdb/wiki/RocksDB-Overview) and the [Basic Operations](https://github.com/facebook/rocksdb/wiki/Basic-Operations) section of the Developer's Guide. Get your initial options set-up following [Setup Options and Basic Tuning](/meta/rocksdb/wiki/Setup-Options-and-Basic-Tuning). Also check [RocksDB FAQ](/meta/rocksdb/wiki/RocksDB-FAQ). There is also a [RocksDB Tuning Guide](/meta/rocksdb/wiki/RocksDB-Tuning-Guide) for advanced RocksDB users.
Check [INSTALL.md](https://github.com/facebook/rocksdb/blob/main/INSTALL.md) for instructions on how to build Rocksdb.
## Releases
[](#releases)
RocksDB releases are done in github. For Java users, Maven Artifacts are also updated. See [RocksDB Release Methodology](/meta/rocksdb/wiki/RocksDB-Release-Methodology).
## Contributing to RocksDB
[](#contributing-to-rocksdb)
You are welcome to send pull requests to contribute to RocksDB code base! Check [RocksDB-Contribution-Guide](/meta/rocksdb/wiki/RocksDB-Contribution-Guide) for guideline.
## Troubleshooting and asking for help
[](#troubleshooting-and-asking-for-help)
Follow [RocksDB Troubleshooting Guide](/meta/rocksdb/wiki/RocksDB-Troubleshooting-Guide) for the guidelines.
## Blog
[](#blog)
- Check out our blog at [rocksdb.org/blog](http://rocksdb.org/blog)
## Project History
[](#project-history)
- [The History of RocksDB](http://rocksdb.blogspot.com/2013/11/the-history-of-rocksdb.html)
-
[Under the Hood: Building and open-sourcing RocksDB](https://www.facebook.com/notes/facebook-engineering/under-the-hood-building-and-open-sourcing-rocksdb/10151822347683920).
## Links
[](#links)
- [Examples](https://github.com/facebook/rocksdb/tree/main/examples)
- [Official Blog](http://rocksdb.org/blog/)
- [Stack Overflow: RocksDB](https://stackoverflow.com/questions/tagged/rocksdb)
- [Talks](https://github.com/facebook/rocksdb/wiki/Talks)
## Contact
[](#contact)
- [RocksDB Google Group](https://groups.google.com/forum/#!forum/rocksdb)
- [RocksDB Facebook Group](https://www.facebook.com/groups/rocksdb.dev/)
- [RocksDB Github Issues](https://github.com/facebook/rocksdb/issues)
-
[Asking For Help](https://github.com/facebook/rocksdb/wiki/RocksDB-Troubleshooting-Guide#asking-for-help)
We use github issues only for bug reports, and use RocksDB's Google Group or Facebook Group for other issues. It’s not always clear to users whether it is RocksDB bug or not. Pick one using your best judgement.
##
Wiki pages
Pages 167
-
Loading
[Home](/meta/rocksdb/wiki)
-
[Welcome to RocksDB](/meta/rocksdb/wiki#welcome-to-rocksdb)
-
[Features](/meta/rocksdb/wiki#features)
-
[Features Not in LevelDB](/meta/rocksdb/wiki#features-not-in-leveldb)
-
[Getting Started](/meta/rocksdb/wiki#getting-started)
-
[Releases](/meta/rocksdb/wiki#releases)
-
[Contributing to RocksDB](/meta/rocksdb/wiki#contributing-to-rocksdb)
-
[Troubleshooting and asking for help](/meta/rocksdb/wiki#troubleshooting-and-asking-for-help)
-
[Blog](/meta/rocksdb/wiki#blog)
-
[Project History](/meta/rocksdb/wiki#project-history)
-
[Links](/meta/rocksdb/wiki#links)
-
[Contact](/meta/rocksdb/wiki#contact)
-
Loading
[[To Be Deprecated] Persistent Read Cache](/meta/rocksdb/wiki/%5BTo-Be-Deprecated%5D-Persistent-Read-Cache)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[A Tutorial of RocksDB SST formats](/meta/rocksdb/wiki/A-Tutorial-of-RocksDB-SST-formats)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Administration and Data Access Tool](/meta/rocksdb/wiki/Administration-and-Data-Access-Tool)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Allocating Some Indexes and Bloom Filters using Huge Page TLB](/meta/rocksdb/wiki/Allocating-Some-Indexes-and-Bloom-Filters-using-Huge-Page-TLB)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Approximate Size](/meta/rocksdb/wiki/Approximate-Size)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Articles about Rocks](/meta/rocksdb/wiki/Articles-about-Rocks)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Asynchronous IO](/meta/rocksdb/wiki/Asynchronous-IO)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Atomic flush](/meta/rocksdb/wiki/Atomic-flush)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Background Error Handling](/meta/rocksdb/wiki/Background-Error-Handling)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Basic Operations](/meta/rocksdb/wiki/Basic-Operations)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Benchmarking tools](/meta/rocksdb/wiki/Benchmarking-tools)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[BlobDB](/meta/rocksdb/wiki/BlobDB)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Block Cache](/meta/rocksdb/wiki/Block-Cache)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Block cache analysis and simulation tools](/meta/rocksdb/wiki/Block-cache-analysis-and-simulation-tools)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Building on Windows](/meta/rocksdb/wiki/Building-on-Windows)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Checkpoints](/meta/rocksdb/wiki/Checkpoints)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Choose Level Compaction Files](/meta/rocksdb/wiki/Choose-Level-Compaction-Files)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Column Families](/meta/rocksdb/wiki/Column-Families)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Compaction](/meta/rocksdb/wiki/Compaction)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Compaction Filter](/meta/rocksdb/wiki/Compaction-Filter)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Compaction Stats and DB Status](/meta/rocksdb/wiki/Compaction-Stats-and-DB-Status)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Compaction Trivial Move](/meta/rocksdb/wiki/Compaction-Trivial-Move)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Compression](/meta/rocksdb/wiki/Compression)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Creating and Ingesting SST files](/meta/rocksdb/wiki/Creating-and-Ingesting-SST-files)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[CuckooTable Format](/meta/rocksdb/wiki/CuckooTable-Format)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Daily Off‐peak Time Option](/meta/rocksdb/wiki/Daily-Off%E2%80%90peak-Time-Option)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Data Block Hash Index](/meta/rocksdb/wiki/Data-Block-Hash-Index)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Delete A Range Of Keys](/meta/rocksdb/wiki/Delete-A-Range-Of-Keys)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Delete Stale Files](/meta/rocksdb/wiki/Delete-Stale-Files)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[DeleteRange](/meta/rocksdb/wiki/DeleteRange)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[DeleteRange Implementation](/meta/rocksdb/wiki/DeleteRange-Implementation)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Developing with an IDE](/meta/rocksdb/wiki/Developing-with-an-IDE)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Dictionary Compression](/meta/rocksdb/wiki/Dictionary-Compression)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Direct IO](/meta/rocksdb/wiki/Direct-IO)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[EventListener](/meta/rocksdb/wiki/EventListener)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[External Table (Experimental)](/meta/rocksdb/wiki/External-Table-(Experimental))
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Features Not in LevelDB](/meta/rocksdb/wiki/Features-Not-in-LevelDB)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[FIFO compaction style](/meta/rocksdb/wiki/FIFO-compaction-style)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Full File Checksum and Checksum Handoff](/meta/rocksdb/wiki/Full-File-Checksum-and-Checksum-Handoff)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Fuzz Test](/meta/rocksdb/wiki/Fuzz-Test)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[How to ask a performance related question](/meta/rocksdb/wiki/How-to-ask-a-performance-related-question)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[How to backup RocksDB](/meta/rocksdb/wiki/How-to-backup-RocksDB)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[How to persist in memory RocksDB database](/meta/rocksdb/wiki/How-to-persist-in-memory-RocksDB-database)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[How we keep track of live SST files](/meta/rocksdb/wiki/How-we-keep-track-of-live-SST-files)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Implement Queue Service Using RocksDB](/meta/rocksdb/wiki/Implement-Queue-Service-Using-RocksDB)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Index Block Format](/meta/rocksdb/wiki/Index-Block-Format)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Indexing SST Files for Better Lookup Performance](/meta/rocksdb/wiki/Indexing-SST-Files-for-Better-Lookup-Performance)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[IO](/meta/rocksdb/wiki/IO)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[IO Tracer and Parser](/meta/rocksdb/wiki/IO-Tracer-and-Parser)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Iterator](/meta/rocksdb/wiki/Iterator)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Iterator Implementation](/meta/rocksdb/wiki/Iterator-Implementation)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[JNI Debugging](/meta/rocksdb/wiki/JNI-Debugging)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Journal](/meta/rocksdb/wiki/Journal)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Known Issues](/meta/rocksdb/wiki/Known-Issues)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Leveled Compaction](/meta/rocksdb/wiki/Leveled-Compaction)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[log_format.txt](/meta/rocksdb/wiki/log_format.txt)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Logger](/meta/rocksdb/wiki/Logger)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Logging in RocksJava](/meta/rocksdb/wiki/Logging-in-RocksJava)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Low Priority Write](/meta/rocksdb/wiki/Low-Priority-Write)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Managing Disk Space Utilization](/meta/rocksdb/wiki/Managing-Disk-Space-Utilization)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[MANIFEST](/meta/rocksdb/wiki/MANIFEST)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Manual Compaction](/meta/rocksdb/wiki/Manual-Compaction)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Memory usage in RocksDB](/meta/rocksdb/wiki/Memory-usage-in-RocksDB)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Mempurge (Memtable Garbage Collection) [Experimental]](/meta/rocksdb/wiki/Mempurge-(Memtable-Garbage-Collection)-%5BExperimental%5D)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[MemTable](/meta/rocksdb/wiki/MemTable)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Merge Operator](/meta/rocksdb/wiki/Merge-Operator)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Merge Operator Implementation](/meta/rocksdb/wiki/Merge-Operator-Implementation)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Multi Column Family Iterator](/meta/rocksdb/wiki/Multi-Column-Family-Iterator)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[MultiGet Performance](/meta/rocksdb/wiki/MultiGet-Performance)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Object Registry](/meta/rocksdb/wiki/Object-Registry)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Online Verification](/meta/rocksdb/wiki/Online-Verification)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Open Projects](/meta/rocksdb/wiki/Open-Projects)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Option String and Option Map](/meta/rocksdb/wiki/Option-String-and-Option-Map)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Partitioned Index Filters](/meta/rocksdb/wiki/Partitioned-Index-Filters)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Perf Context and IO Stats Context](/meta/rocksdb/wiki/Perf-Context-and-IO-Stats-Context)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Performance Benchmark 2014](/meta/rocksdb/wiki/Performance-Benchmark-2014)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Performance Benchmark 201807](/meta/rocksdb/wiki/Performance-Benchmark-201807)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Performance Benchmarks](/meta/rocksdb/wiki/Performance-Benchmarks)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Performance Benchmarks October 2022](/meta/rocksdb/wiki/Performance-Benchmarks-October-2022)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Pipelined Write](/meta/rocksdb/wiki/Pipelined-Write)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[PlainTable Format](/meta/rocksdb/wiki/PlainTable-Format)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Platform Requirements](/meta/rocksdb/wiki/Platform-Requirements)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[poc](/meta/rocksdb/wiki/poc)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[poc test](/meta/rocksdb/wiki/poc-test)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[poc.html](/meta/rocksdb/wiki/poc.html)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Prefix Seek](/meta/rocksdb/wiki/Prefix-Seek)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Projects Being Developed](/meta/rocksdb/wiki/Projects-Being-Developed)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Proposal: Unifying Level and Universal Compactions](/meta/rocksdb/wiki/Proposal:-Unifying-Level-and-Universal-Compactions)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Proposals on Improving Rocksdb's Options](/meta/rocksdb/wiki/Proposals-on-Improving-Rocksdb's-Options)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Publication](/meta/rocksdb/wiki/Publication)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Rate Limiter](/meta/rocksdb/wiki/Rate-Limiter)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Read Modify Write Benchmarks](/meta/rocksdb/wiki/Read-Modify-Write-Benchmarks)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Read only and Secondary instances](/meta/rocksdb/wiki/Read-only-and-Secondary-instances)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Reducing memcpy overhead when using Iterators](/meta/rocksdb/wiki/Reducing-memcpy-overhead-when-using-Iterators)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Remote Compaction](/meta/rocksdb/wiki/Remote-Compaction)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Replication Helpers](/meta/rocksdb/wiki/Replication-Helpers)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Rocksdb Architecture Guide](/meta/rocksdb/wiki/Rocksdb-Architecture-Guide)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Rocksdb BlockBasedTable Format](/meta/rocksdb/wiki/Rocksdb-BlockBasedTable-Format)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[RocksDB Bloom Filter](/meta/rocksdb/wiki/RocksDB-Bloom-Filter)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[RocksDB Compatibility Between Different Releases](/meta/rocksdb/wiki/RocksDB-Compatibility-Between-Different-Releases)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[RocksDB Configurable Objects](/meta/rocksdb/wiki/RocksDB-Configurable-Objects)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[RocksDB Contribution Guide](/meta/rocksdb/wiki/RocksDB-Contribution-Guide)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[RocksDB Extensions](/meta/rocksdb/wiki/RocksDB-Extensions)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[RocksDB FAQ](/meta/rocksdb/wiki/RocksDB-FAQ)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[RocksDB In Memory Workload Performance Benchmarks](/meta/rocksdb/wiki/RocksDB-In-Memory-Workload-Performance-Benchmarks)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[RocksDB Options File](/meta/rocksdb/wiki/RocksDB-Options-File)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[RocksDB Overview](/meta/rocksdb/wiki/RocksDB-Overview)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[RocksDB Public Communication and Information Channels](/meta/rocksdb/wiki/RocksDB-Public-Communication-and-Information-Channels)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[RocksDB Release Methodology](/meta/rocksdb/wiki/RocksDB-Release-Methodology)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[RocksDB Repairer](/meta/rocksdb/wiki/RocksDB-Repairer)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Rocksdb Table Format](/meta/rocksdb/wiki/Rocksdb-Table-Format)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[RocksDB Trace, Replay, Analyzer, and Workload Generation](/meta/rocksdb/wiki/RocksDB-Trace,-Replay,-Analyzer,-and-Workload-Generation)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[RocksDB Troubleshooting Guide](/meta/rocksdb/wiki/RocksDB-Troubleshooting-Guide)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[RocksDB Tuning Guide](/meta/rocksdb/wiki/RocksDB-Tuning-Guide)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[RocksDB Users and Use Cases](/meta/rocksdb/wiki/RocksDB-Users-and-Use-Cases)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[RocksDB version macros](/meta/rocksdb/wiki/RocksDB-version-macros)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[RocksJava API TODO](/meta/rocksdb/wiki/RocksJava-API-TODO)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[RocksJava Basics](/meta/rocksdb/wiki/RocksJava-Basics)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[RocksJava Performance on Flash Storage](/meta/rocksdb/wiki/RocksJava-Performance-on-Flash-Storage)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[SecondaryCache (Experimental)](/meta/rocksdb/wiki/SecondaryCache-(Experimental))
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[SeekForPrev](/meta/rocksdb/wiki/SeekForPrev)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Setup Options and Basic Tuning](/meta/rocksdb/wiki/Setup-Options-and-Basic-Tuning)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Simulation Cache](/meta/rocksdb/wiki/Simulation-Cache)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Single Delete](/meta/rocksdb/wiki/Single-Delete)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Slow Deletion](/meta/rocksdb/wiki/Slow-Deletion)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Snapshot](/meta/rocksdb/wiki/Snapshot)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Space Tuning](/meta/rocksdb/wiki/Space-Tuning)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Speed Up DB Open](/meta/rocksdb/wiki/Speed-Up-DB-Open)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[SST File Manager](/meta/rocksdb/wiki/SST-File-Manager)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[SST Partitioner](/meta/rocksdb/wiki/SST-Partitioner)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Statistics](/meta/rocksdb/wiki/Statistics)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Stress test](/meta/rocksdb/wiki/Stress-test)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Subcompaction](/meta/rocksdb/wiki/Subcompaction)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Tailing Iterator](/meta/rocksdb/wiki/Tailing-Iterator)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Talks](/meta/rocksdb/wiki/Talks)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Terminology](/meta/rocksdb/wiki/Terminology)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[testpoc.html](/meta/rocksdb/wiki/testpoc.html)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Tests](/meta/rocksdb/wiki/Tests)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[The Customizable Class](/meta/rocksdb/wiki/The-Customizable-Class)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Third party language bindings](/meta/rocksdb/wiki/Third-party-language-bindings)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[This is a test](/meta/rocksdb/wiki/This-is-a-test)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Thread Pool](/meta/rocksdb/wiki/Thread-Pool)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Tiered Storage (Experimental)](/meta/rocksdb/wiki/Tiered-Storage-(Experimental))
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Tiered Storage Benchmarking](/meta/rocksdb/wiki/Tiered-Storage-Benchmarking)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Time to Live](/meta/rocksdb/wiki/Time-to-Live)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Track WAL in MANIFEST](/meta/rocksdb/wiki/Track-WAL-in-MANIFEST)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Transactions](/meta/rocksdb/wiki/Transactions)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Tuning RocksDB from Java](/meta/rocksdb/wiki/Tuning-RocksDB-from-Java)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Tuning RocksDB on Spinning Disks](/meta/rocksdb/wiki/Tuning-RocksDB-on-Spinning-Disks)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Two Phase Commit Implementation](/meta/rocksdb/wiki/Two-Phase-Commit-Implementation)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Universal Compaction](/meta/rocksdb/wiki/Universal-Compaction)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Universal Style Compaction Example](/meta/rocksdb/wiki/Universal-Style-Compaction-Example)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[unordered_write](/meta/rocksdb/wiki/unordered_write)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[User defined Timestamp](/meta/rocksdb/wiki/User-defined-Timestamp)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[WAL Compression](/meta/rocksdb/wiki/WAL-Compression)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[WAL Performance](/meta/rocksdb/wiki/WAL-Performance)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[WAL Recovery Modes](/meta/rocksdb/wiki/WAL-Recovery-Modes)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[What's new in RocksDB2.7](/meta/rocksdb/wiki/What's-new-in-RocksDB2.7)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Wide Columns](/meta/rocksdb/wiki/Wide-Columns)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Write Ahead Log (WAL)](/meta/rocksdb/wiki/Write-Ahead-Log-(WAL))
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Write Ahead Log File Format](/meta/rocksdb/wiki/Write-Ahead-Log-File-Format)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Write Batch With Index](/meta/rocksdb/wiki/Write-Batch-With-Index)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Write Buffer Manager](/meta/rocksdb/wiki/Write-Buffer-Manager)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[Write Stalls](/meta/rocksdb/wiki/Write-Stalls)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[WritePrepared Transactions](/meta/rocksdb/wiki/WritePrepared-Transactions)
### Uh oh!
There was an error while loading. Please reload this page .
-
Loading
[WriteUnprepared Transactions](/meta/rocksdb/wiki/WriteUnprepared-Transactions)
### Uh oh!
There was an error while loading. Please reload this page .
-
Show 152 more pages…
Contents
- [RocksDB Wiki](/meta/rocksdb/wiki/Home)
- [Overview](/meta/rocksdb/wiki/RocksDB-Overview)
- [RocksDB FAQ](/meta/rocksdb/wiki/RocksDB-FAQ)
- [Terminology](/meta/rocksdb/wiki/Terminology)
- [Requirements](/meta/rocksdb/wiki/Platform-Requirements)
- [Contributors' Guide](/meta/rocksdb/wiki/RocksDB-Contribution-Guide)
- [Release Methodology](/meta/rocksdb/wiki/RocksDB-Release-Methodology)
- [RocksDB Users and Use Cases](/meta/rocksdb/wiki/RocksDB-Users-and-Use-Cases)
- [RocksDB Public Communication and Information Channels](/meta/rocksdb/wiki/RocksDB-Public-Communication-and-Information-Channels)
-
[Basic Operations](/meta/rocksdb/wiki/Basic-Operations)
- [Iterator](/meta/rocksdb/wiki/Iterator)
- [Prefix seek](/meta/rocksdb/wiki/Prefix-Seek)
- [SeekForPrev](/meta/rocksdb/wiki/SeekForPrev)
- [Tailing Iterator](/meta/rocksdb/wiki/Tailing-Iterator)
- [Compaction Filter](/meta/rocksdb/wiki/Compaction-Filter)
- [Multi Column Family Iterator](/meta/rocksdb/wiki/Multi-Column-Family-Iterator)
- [Read-Modify-Write (Merge) Operator](/meta/rocksdb/wiki/Merge-Operator)
- [Column Families](/meta/rocksdb/wiki/Column-Families)
- [Creating and Ingesting SST files](/meta/rocksdb/wiki/Creating-and-Ingesting-SST-files)
- [Single Delete](/meta/rocksdb/wiki/Single-Delete)
- [SST Partitioner](/meta/rocksdb/wiki/SST-Partitioner)
- [Low Priority Write](/meta/rocksdb/wiki/Low-Priority-Write)
- [Time to Live (TTL) Support](/meta/rocksdb/wiki/Time-to-Live)
- [Transactions](/meta/rocksdb/wiki/Transactions)
- [Snapshot](/meta/rocksdb/wiki/Snapshot)
- [DeleteRange](/meta/rocksdb/wiki/DeleteRange)
- [Atomic flush](/meta/rocksdb/wiki/Atomic-flush)
- [Read-only and Secondary instances](/meta/rocksdb/wiki/Read-only-and-Secondary-instances)
- [Approximate Size](/meta/rocksdb/wiki/Approximate-Size)
- [User-defined Timestamp](/meta/rocksdb/wiki/User-defined-Timestamp)
- [Wide Columns](/meta/rocksdb/wiki/Wide-Columns)
- [BlobDB](/meta/rocksdb/wiki/BlobDB)
- [Online Verification](/meta/rocksdb/wiki/Online-Verification)
-
Options
- [Setup Options and Basic Tuning](/meta/rocksdb/wiki/Setup-Options-and-Basic-Tuning)
- [Option String and Option Map](/meta/rocksdb/wiki/Option-String-and-Option-Map)
- [RocksDB Options File](/meta/rocksdb/wiki/RocksDB-Options-File)
- [MemTable](/meta/rocksdb/wiki/MemTable)
-
[Journal](/meta/rocksdb/wiki/Journal)
-
[Write Ahead Log (WAL)](/meta/rocksdb/wiki/Write-Ahead-Log-%28WAL%29)
- [Write Ahead Log File Format](/meta/rocksdb/wiki/Write-Ahead-Log-File-Format)
- [WAL Recovery Modes](/meta/rocksdb/wiki/WAL-Recovery-Modes)
- [WAL Performance](/meta/rocksdb/wiki/WAL-Performance)
- [WAL Compression](/meta/rocksdb/wiki/WAL-Compression)
- [MANIFEST](/meta/rocksdb/wiki/MANIFEST)
- [Track WAL in MANIFEST](/meta/rocksdb/wiki/Track-WAL-in-MANIFEST)
-
Cache
- [Block Cache](/meta/rocksdb/wiki/Block-Cache)
- [SecondaryCache (Experimental)](/meta/rocksdb/wiki/SecondaryCache-%28Experimental%29)
- [Write Buffer Manager](/meta/rocksdb/wiki/Write-Buffer-Manager)
-
[Compaction](/meta/rocksdb/wiki/Compaction)
- [Leveled Compaction](/meta/rocksdb/wiki/Leveled-Compaction)
- [Universal compaction style](/meta/rocksdb/wiki/Universal-Compaction)
- [FIFO compaction style](/meta/rocksdb/wiki/FIFO-compaction-style)
- [Manual Compaction](/meta/rocksdb/wiki/Manual-Compaction)
- [Subcompaction](/meta/rocksdb/wiki/Subcompaction)
- [Choose Level Compaction Files](/meta/rocksdb/wiki/Choose-Level-Compaction-Files)
- [Managing Disk Space Utilization](/meta/rocksdb/wiki/Managing-Disk-Space-Utilization)
- [Trivial Move Compaction](/meta/rocksdb/wiki/Compaction-Trivial-Move)
- [Remote Compaction](/meta/rocksdb/wiki/Remote-Compaction)
-
SST File Formats
- [Block-based Table Format](/meta/rocksdb/wiki/Rocksdb-BlockBasedTable-Format)
- [PlainTable Format](/meta/rocksdb/wiki/PlainTable-Format)
- [CuckooTable Format](/meta/rocksdb/wiki/CuckooTable-Format)
- [External Table](/meta/rocksdb/wiki/External-Table-%28Experimental%29)
- [Index Block Format](/meta/rocksdb/wiki/Index-Block-Format)
- [Bloom Filter](/meta/rocksdb/wiki/RocksDB-Bloom-Filter)
- [Data Block Hash Index](/meta/rocksdb/wiki/Data-Block-Hash-Index)
-
[IO](/meta/rocksdb/wiki/IO)
- [Rate Limiter](/meta/rocksdb/wiki/Rate-Limiter)
- [SST File Manager](/meta/rocksdb/wiki/SST-File-Manager)
- [Direct I/O](/meta/rocksdb/wiki/Direct-IO)
-
[Compression](/meta/rocksdb/wiki/Compression) - [Dictionary Compression](/meta/rocksdb/wiki/Dictionary-Compression)
- [Full File Checksum and Checksum Handoff](/meta/rocksdb/wiki/Full-File-Checksum-and-Checksum-Handoff)
- [Background Error Handling](/meta/rocksdb/wiki/Background-Error-Handling)
- [Huge Page TLB Support](/meta/rocksdb/wiki/Allocating-Some-Indexes-and-Bloom-Filters-using-Huge-Page-TLB)
- [Tiered Storage (Experimental)](/meta/rocksdb/wiki/Tiered-Storage-%28Experimental%29)
-
Logging and Monitoring
- [Logger](/meta/rocksdb/wiki/Logger)
- [Statistics](/meta/rocksdb/wiki/Statistics)
- [Compaction Stats and DB Status](/meta/rocksdb/wiki/Compaction-Stats-and-DB-Status)
- [Perf Context and IO Stats Context](/meta/rocksdb/wiki/Perf-Context-and-IO-Stats-Context)
- [EventListener](/meta/rocksdb/wiki/EventListener)
- [Known Issues](/meta/rocksdb/wiki/Known-Issues)
- [Troubleshooting Guide](/meta/rocksdb/wiki/RocksDB-Troubleshooting-Guide)
-
[Tests](/meta/rocksdb/wiki/Tests)
-
[Stress Test](https://github.com/facebook/rocksdb/wiki/Stress-test)
- [Fuzzing](/meta/rocksdb/wiki/Fuzz-Test)
- [Benchmarking](/meta/rocksdb/wiki/Benchmarking-tools)
-
Tools / Utilities
- [Administration and Data Access Tool](/meta/rocksdb/wiki/Administration-and-Data-Access-Tool)
-
[How to Backup RocksDB?](https://github.com/facebook/rocksdb/wiki/How-to-backup-RocksDB)
- [Replication Helpers](/meta/rocksdb/wiki/Replication-Helpers)
- [Checkpoints](/meta/rocksdb/wiki/Checkpoints)
-
[How to persist in-memory RocksDB database](https://github.com/facebook/rocksdb/wiki/How-to-persist-in-memory-RocksDB-database)
- [Third-party language bindings](/meta/rocksdb/wiki/Third-party-language-bindings)
- [RocksDB Trace, Replay, Analyzer, and Workload Generation](/meta/rocksdb/wiki/RocksDB-Trace%2C-Replay%2C-Analyzer%2C-and-Workload-Generation)
- [Block cache analysis and simulation tools](/meta/rocksdb/wiki/Block-cache-analysis-and-simulation-tools)
- [IO Tracer and Parser](/meta/rocksdb/wiki/IO-Tracer-and-Parser)
-
Implementation Details
- [Delete Stale Files](/meta/rocksdb/wiki/Delete-Stale-Files)
- [Partitioned Index/Filters](/meta/rocksdb/wiki/Partitioned-Index-Filters)
- [WritePrepared-Transactions](/meta/rocksdb/wiki/WritePrepared-Transactions)
- [WriteUnprepared-Transactions](/meta/rocksdb/wiki/WriteUnprepared-Transactions)
- [How we keep track of live SST files](/meta/rocksdb/wiki/How-we-keep-track-of-live-SST-files)
- [How we index SST](/meta/rocksdb/wiki/Indexing-SST-Files-for-Better-Lookup-Performance)
- [Merge Operator Implementation](/meta/rocksdb/wiki/Merge-Operator-Implementation)
- [RocksDB Repairer](/meta/rocksdb/wiki/RocksDB-Repairer)
- [Write Batch With Index](/meta/rocksdb/wiki/Write-Batch-With-Index)
- [Two Phase Commit](/meta/rocksdb/wiki/Two-Phase-Commit-Implementation)
- [Iterator's Implementation](/meta/rocksdb/wiki/Iterator-Implementation)
- [Simulation Cache](/meta/rocksdb/wiki/Simulation-Cache)
- [[To Be Deprecated] Persistent Read Cache](/meta/rocksdb/wiki/%5BTo-Be-Deprecated%5D-Persistent-Read-Cache)
- [DeleteRange Implementation](/meta/rocksdb/wiki/DeleteRange-Implementation)
- [unordered_write](/meta/rocksdb/wiki/unordered_write)
-
Extending RocksDB
- [RocksDB Configurable Objects](/meta/rocksdb/wiki/RocksDB-Configurable-Objects)
- [The Customizable Class](/meta/rocksdb/wiki/The-Customizable-Class)
- [Object Registry](/meta/rocksdb/wiki/Object-Registry)
-
RocksJava
- [RocksJava Basics](/meta/rocksdb/wiki/RocksJava-Basics)
- [Logging in RocksJava](/meta/rocksdb/wiki/Logging-in-RocksJava)
- [JNI Debugging](/meta/rocksdb/wiki/JNI-Debugging)
- [RocksJava API TODO](/meta/rocksdb/wiki/RocksJava-API-TODO)
- [RocksJava Performance on Flash Storage](/meta/rocksdb/wiki/RocksJava-Performance-on-Flash-Storage)
- [Tuning RocksDB from Java](/meta/rocksdb/wiki/Tuning-RocksDB-from-Java)
-
Performance
- [Performance Benchmarks](/meta/rocksdb/wiki/Performance-Benchmarks)
- [In Memory Workload Performance](/meta/rocksdb/wiki/RocksDB-In-Memory-Workload-Performance-Benchmarks)
- [Read-Modify-Write (Merge) Performance](/meta/rocksdb/wiki/Read-Modify-Write-Benchmarks)
- [Delete A Range Of Keys](/meta/rocksdb/wiki/Delete-A-Range-Of-Keys)
- [Write Stalls](/meta/rocksdb/wiki/Write-Stalls)
- [Pipelined Write](/meta/rocksdb/wiki/Pipelined-Write)
- [MultiGet Performance](/meta/rocksdb/wiki/MultiGet-Performance)
- [Tuning Guide](/meta/rocksdb/wiki/RocksDB-Tuning-Guide)
- [Memory usage in RocksDB](/meta/rocksdb/wiki/Memory-usage-in-RocksDB)
- [Speed-Up DB Open](/meta/rocksdb/wiki/Speed-Up-DB-Open)
- [Implement Queue Service Using RocksDB](/meta/rocksdb/wiki/Implement-Queue-Service-Using-RocksDB)
- [Asynchronous IO](/meta/rocksdb/wiki/Asynchronous-IO)
- [Off-peak in RocksDB](/meta/rocksdb/wiki/Daily-Off%E2%80%90peak-Time-Option)
- [Projects Being Developed](/meta/rocksdb/wiki/Projects-Being-Developed)
-
Misc
- [Building on Windows](/meta/rocksdb/wiki/Building-on-Windows)
- [Developing with an IDE](/meta/rocksdb/wiki/Developing-with-an-IDE)
- [Open Projects](/meta/rocksdb/wiki/Open-Projects)
- [Talks](/meta/rocksdb/wiki/Talks)
- [Publication](/meta/rocksdb/wiki/Publication)
- [Features Not in LevelDB](/meta/rocksdb/wiki/Features-Not-in-LevelDB)
- [How to ask a performance-related question?](/meta/rocksdb/wiki/How-to-ask-a-performance-related-question)
- [Articles about Rocks](/meta/rocksdb/wiki/Articles-about-Rocks)
### Clone this wiki locally
## Footer
[](https://github.com)
© 2026 GitHub, Inc.
### Footer navigation
-
[Terms](https://docs.github.com/site-policy/github-terms/github-terms-of-service)
-
[Privacy](https://docs.github.com/site-policy/privacy-policies/github-privacy-statement)
-
[Security](https://github.com/security)
-
[Status](https://www.githubstatus.com/)
-
[Community](https://github.community/)
-
[Docs](https://docs.github.com/)
-
[Contact](https://support.github.com?tags=dotcom-footer)
-
Manage cookies
-
Do not share my personal information
You can’t perform that action at this time.