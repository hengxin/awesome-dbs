# TiDB Architecture | TiDB Docs

- 来源: https://docs.pingcap.com/tidb/stable/tidb-architecture
- 归档时间: 2026-10-29
- 说明: 官方技术白皮书 / 架构文档的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

📣 New in Public Preview: [TiDB Cloud BYOC](https://www.pingcap.com/blog/tidb-cloud-byoc-public-preview/) , [TiDB Cloud Filesystem](https://www.pingcap.com/tidb/tidb-cloud-filesystem/) , [PostgreSQL-compatible TiDB Cloud Starter](https://docs.pingcap.com/tidbcloud/starter/?plan=starter&compatibility=postgresql)
[](/)
[](/)
​
​
[Sign In](https://tidbcloud.com/signin)[Start for Free](https://tidbcloud.com/free-trial)
Product
[AI](/ai/)[Developer](/developer/)[Best Practices](/best-practices/)[API](/api/) Releases
​
​
[Sign In](https://tidbcloud.com/signin)[Start for Free](https://tidbcloud.com/free-trial)
English
[TiDB Self-Managed](/tidb/stable/)
v8.5
-
About TiDB Self-Managed
-
Get Started
-
Deploy
-
Migrate
-
Stream Data
-
Maintain
-
Monitor and Alert
-
Troubleshoot
-
Performance Tuning
-
Tutorials
-
TiDB Tools
-
Reference
-
Cluster Architecture
[-
Overview](/tidb/stable/tidb-architecture/)[-
Storage](/tidb/stable/tidb-storage/)[-
Computing](/tidb/stable/tidb-computing/)[-
Scheduling](/tidb/stable/tidb-scheduling/)[-
TSO](/tidb/stable/tso/)
-
Storage Engine - TiKV
-
Storage Engine - TiFlash
-
TiDB Distributed eXecution Framework (DXF)
[-
System Variables](/tidb/stable/system-variables/)[-
System Variable Reference](/tidb/stable/system-variable-reference/)[-
Server Status Variables](/tidb/stable/status-variables/)-
Configuration File Parameters
-
CLI
-
Command Line Flags
-
Key Monitoring Metrics
-
Privileges
-
SQL
[-
Telemetry](/tidb/stable/telemetry/)[-
Error Codes](/tidb/stable/error-codes/)[-
Table Filter](/tidb/stable/table-filter/)[-
TiDB Installation Packages](/tidb/stable/binary-package/)[-
Schedule Replicas by Topology Labels](/tidb/stable/schedule-replicas-by-topology-labels/)[-
URI Formats of External Storage Services](/tidb/stable/external-storage-uri/)[-
Interaction Test on Online Workloads and
ADD INDEX Operations](/tidb/stable/online-workloads-and-add-index-operations/)[-
ANALYZE Embedded in DDL Statements](/tidb/stable/ddl_embedded_analyze/)
-
FAQs
[-
Glossary](/tidb/stable/glossary/)
# TiDB Architecture[](#tidb-architecture)
Contribute
Copy as Markdown View as Markdown Download PDF
Compared with the traditional standalone databases, TiDB has the following advantages:
- Has a distributed architecture with flexible and elastic scalability.
- Fully compatible with the MySQL protocol, common features and syntax of MySQL. To migrate your applications to TiDB, you do not need to change a single line of code in many cases.
- Supports high availability with automatic failover when a minority of replicas fail; transparent to applications.
- Supports ACID transactions, suitable for scenarios requiring strong consistency such as bank transfer.
- Provides a rich series of [data migration tools](/tidb/stable/migration-overview/) for migrating, replicating, or backing up data.
As a distributed database, TiDB is designed to consist of multiple components. These components communicate with each other and form a complete TiDB system. The architecture is as follows:
## TiDB server[](#tidb-server)
The [TiDB server](/tidb/stable/tidb-computing/) is a stateless SQL layer that exposes the connection endpoint of the MySQL protocol to the outside. The TiDB server receives SQL requests, performs SQL parsing and optimization, and ultimately generates a distributed execution plan. It is horizontally scalable and provides the unified interface to the outside through the load balancing components such as TiProxy, Linux Virtual Server (LVS), HAProxy, ProxySQL or F5. It does not store data and is only for computing and SQL analyzing, transmitting actual data read request to TiKV nodes (or TiFlash nodes).
## Placement Driver (PD) server[](#placement-driver-pd-server)
The [PD server](/tidb/stable/tidb-scheduling/) is the metadata managing component of the entire cluster. It stores metadata of real-time data distribution of every single TiKV node and the topology structure of the entire TiDB cluster, provides the TiDB Dashboard management UI, and allocates transaction IDs to distributed transactions. The PD server is "the brain" of the entire TiDB cluster because it not only stores metadata of the cluster, but also sends data scheduling command to specific TiKV nodes according to the data distribution state reported by TiKV nodes in real time. In addition, the PD server consists of three nodes at least and has high availability. It is recommended to deploy an odd number of PD nodes.
## Storage servers[](#storage-servers)
### TiKV server[](#tikv-server)
The [TiKV server](/tidb/stable/tidb-storage/) is responsible for storing data. TiKV is a distributed transactional key-value storage engine.
[Region](/tidb/stable/glossary/#regionpeerraft-group) is the basic unit to store data. Each Region stores the data for a particular Key Range which is a left-closed and right-open interval from StartKey to EndKey.
Multiple Regions exist in each TiKV node. TiKV APIs provide native support to distributed transactions at the key-value pair level and supports the Snapshot Isolation level isolation by default. This is the core of how TiDB supports distributed transactions at the SQL level. After processing SQL statements, the TiDB server converts the SQL execution plan to an actual call to the TiKV API. Therefore, data is stored in TiKV. All the data in TiKV is automatically maintained in multiple replicas (three replicas by default), so TiKV has native high availability and supports automatic failover.
### TiFlash server[](#tiflash-server)
The [TiFlash server](/tidb/stable/tiflash-overview/) is a special type of storage server. Unlike ordinary TiKV nodes, TiFlash stores data by column, mainly designed to accelerate analytical processing.
## Was this page helpful?
Yes No
ON THIS PAGE
- [TiDB server](#tidb-server)
- [Placement Driver (PD) server](#placement-driver-pd-server)
- [Storage servers](#storage-servers) - [TiKV server](#tikv-server)
- [TiFlash server](#tiflash-server)
ON THIS PAGE
Product
[Product Overview](https://www.pingcap.com/tidb/)[TiDB Cloud](https://www.pingcap.com/tidb/cloud/)[TiDB Self-Managed](https://www.pingcap.com/tidb/self-managed/)[Pricing](https://www.pingcap.com/pricing/)
Ecosystem
[Integrations](https://www.pingcap.com/integrations/)[TiKV](https://github.com/tikv/tikv)[TiFlash](https://github.com/pingcap/tiflash)[OSS Insight](https://ossinsight.io/)
Resources
[Blog](https://www.pingcap.com/blog/)[Articles](https://www.pingcap.com/article/)[Events & Webinars](https://www.pingcap.com/event)[Docs](https://docs.pingcap.com/)[Developer Guide](https://docs.pingcap.com/developer/)[FAQs](https://www.pingcap.com/faqs/)[Support](https://tidb.support.pingcap.com/)[llms.txt](https://docs.pingcap.com/llms.txt)
Company
[About Us](https://www.pingcap.com/about-us/)[News](https://www.pingcap.com/press-releases-news)[Careers](https://www.pingcap.com/careers/)[Contact Us](https://www.pingcap.com/contact-us/)[Partners](https://www.pingcap.com/partners/)[Trust Hub](https://www.pingcap.com/trust-hub/)[Security](https://www.pingcap.com/security/)[Release Support](https://www.pingcap.com/tidb-release-support-policy/)[Brand Guidelines](https://www.pingcap.com/tidb-brand-guidelines/)
Stay Connected
[](https://github.com/pingcap)[](https://twitter.com/PingCAP)[](https://linkedin.com/company/pingcap)[](https://facebook.com/pingcap2015)[](https://slack.tidb.io/invite?team=tidb-community&channel=everyone&ref=pingcap-docs)[](https://discord.com/invite/vYU9h56kAX?utm_source=doc)[](https://www.youtube.com/PingCAP)
[](https://github.com/pingcap)[](https://twitter.com/PingCAP)[](https://linkedin.com/company/pingcap)[](https://facebook.com/pingcap2015)[](https://slack.tidb.io/invite?team=tidb-community&channel=everyone&ref=pingcap-docs)[](https://discord.com/invite/vYU9h56kAX?utm_source=doc)[](https://www.youtube.com/PingCAP)
© 2026 PingCAP. All Rights Reserved.
/
[Privacy Policy](https://www.pingcap.com/privacy-policy) /
[Legal](https://www.pingcap.com/legal/)