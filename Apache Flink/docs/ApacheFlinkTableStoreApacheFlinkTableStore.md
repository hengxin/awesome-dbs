# Apache Flink Table Store | Apache Flink Table Store

- 来源: https://nightlies.apache.org/flink/flink-table-store-docs-stable/
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

[](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3)
v0.3.0
-
Concepts
▾
-
[Overview](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/concepts/overview/)
-
[Basic Concepts](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/concepts/basic-concepts/)
-
[File Layouts](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/concepts/file-layouts/)
-
[LSM Trees](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/concepts/lsm-trees/)
-
[Consistency Guarantees](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/concepts/consistency-guarantees/)
-
Engines
▾
-
[Overview](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/engines/overview/)
-
[Flink](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/engines/flink/)
-
[Spark3](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/engines/spark3/)
-
[Spark2](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/engines/spark2/)
-
[Hive](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/engines/hive/)
-
[Trino](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/engines/trino/)
-
Filesystems
▾
-
[Overview](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/filesystems/overview/)
-
[OSS](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/filesystems/oss/)
-
[S3](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/filesystems/s3/)
-
How to
▾
-
[Creating Catalogs](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/how-to/creating-catalogs/)
-
[Creating Tables](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/how-to/creating-tables/)
-
[Altering Tables](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/how-to/altering-tables/)
-
[Writing Tables](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/how-to/writing-tables/)
-
[Querying Tables](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/how-to/querying-tables/)
-
Features
▾
-
[Table Types](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/features/table-types/)
-
[External Log Systems](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/features/external-log-systems/)
-
[Lookup Joins](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/features/lookup-joins/)
-
Maintenance
▾
-
[Write Performance](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/maintenance/write-performance/)
-
[Expiring Snapshots](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/maintenance/expiring-snapshots/)
-
[Rescale Bucket](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/maintenance/rescale-bucket/)
-
[Manage Partition](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/maintenance/manage-partition/)
-
[Configurations](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/maintenance/configurations/)
[Project Homepage](//flink.apache.org)
[JavaDocs](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/api/java/)
-
Pick Docs Version
▾
[0.3 (✓)](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3)
-
[v0.2](https://nightlies.apache.org/flink/flink-table-store-docs-release-0.2)
-
[All Versions](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/versions)
Apache Flink Table Store
#
Apache Flink Table Store
[#](#apache-flink-table-store)
Flink Table Store is a unified storage to build dynamic tables for both streaming and
batch processing in Flink, supporting high-speed data ingestion and timely data query.
Table Store offers the following core capabilities:
- Support storage of large datasets and allow read/write in both batch and streaming mode.
- Support streaming queries with minimum latency down to milliseconds.
- Support Batch/OLAP queries with minimum latency down to the second level.
- Support incremental snapshots for stream consumption by default. So users do not need to combine different pipelines by themself.
## Try Table Store
If you’re interested in playing around with Flink Table Store, check out our
quick start guide with [Flink](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/engines/flink/), [Spark](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/engines/spark3/) or [Hive](//nightlies.apache.org/flink/flink-table-store-docs-release-0.3/docs/engines/hive/). It provides a step by
step introduction to the APIs and guides you through real applications.
## Get Help with Table Store
If you get stuck, check out our [community support
resources](https://flink.apache.org/community.html). In particular, Apache
Flink’s user mailing list is consistently ranked as one of the most active of
any Apache project, and is a great way to get help quickly.
Flink Table Store is developed under the umbrella of
[Apache Flink](https://flink.apache.org/).