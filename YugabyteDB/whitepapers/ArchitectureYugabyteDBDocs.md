# Architecture | YugabyteDB Docs

- 来源: https://docs.yugabyte.com/stable/architecture/
- 归档时间: 2026-10-29
- 说明: 官方技术白皮书 / 架构文档的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

[](/)
Ask AI about " "
OR Ask AI
-
[Star us on Github](https://github.com/yugabyte/yugabyte-db)
-
[Join us on Slack](https://inviter.co/yugabytedb)
-
Start Now
-
[YugabyteDB AeonTry our fully-managed cloud DBaaS for free.No credit card requiredSign up](https://cloud.yugabyte.com/signup?utm_medium=direct&utm_source=docs&utm_campaign=YBM_signup)
-
[YugabyteDBTry our open source distributed SQL database on your laptop.Download](https://download.yugabyte.com/#/)
-
[Products](/)
- [YugabyteDBThe open source distributed SQL database](/stable/)
- [YugabyteDB AnywhereSelf-managed cloud DBaaS](/stable/yugabyte-platform/)
- [YugabyteDB AeonFully-managed cloud DBaaS](/stable/yugabyte-cloud/)
- [YugabyteDB VoyagerDatabase migration service](/stable/yugabyte-voyager/)
-
[Develop](/stable/develop/)
-
[Integrations](/stable/integrations/)
-
[API](/stable/api/)
- SQL APIs
- [YSQL](/stable/api/ysql/)
- [YCQL](/stable/api/ycql/)
- Clients
- [ysqlsh](/stable/api/ysqlsh/)
- [ycqlsh](/stable/api/ycqlsh/)
- Management APIs
- [YugabyteDB Anywhere API](/stable/yugabyte-platform/anywhere-automation/anywhere-api/)
- [YugabyteDB Aeon API](/stable/yugabyte-cloud/managed-automation/managed-api/)
-
[FAQ](/stable/faq/general/)
-
[Releases](/stable/releases/)
- [YugabyteDB](/stable/releases/ybdb-releases/)
- [YugabyteDB Anywhere](/stable/releases/yba-releases/)
- [YugabyteDB Aeon](/stable/yugabyte-cloud/release-notes/)
- [YugabyteDB Voyager](/stable/yugabyte-voyager/release-notes/)
- [YugabyteDB Clients](/stable/releases/yugabyte-clients/)
- [Tech Advisories](/stable/releases/techadvisories/)
Docs Menu
YugabyteDB The open source distributed SQL database
-
[YugabyteDBThe open source distributed SQL database](/stable/)
-
[YugabyteDB AnywhereSelf-managed cloud DBaaS](/stable/yugabyte-platform/)
-
[YugabyteDB AeonFully-managed cloud DBaaS](/stable/yugabyte-cloud/)
-
[YugabyteDB VoyagerDatabase migration service](/stable/yugabyte-voyager/)
-
[Overview](/stable/)
-
[Quick Start](/stable/quick-start/macos/)
-
[Explore](/stable/explore/)
-
[Run the examples](/stable/explore/cluster-setup-local/)
-
[SQL features](/stable/explore/ysql-language-features/)
-
[Schemas and tables](/stable/explore/ysql-language-features/databases-schemas-tables/)
-
[Data types](/stable/explore/ysql-language-features/data-types/)
-
[Read data](/stable/explore/ysql-language-features/queries/)
-
[Write data](/stable/explore/ysql-language-features/data-manipulation/)
-
[Expressions and operators](/stable/explore/ysql-language-features/expressions-operators/)
-
[JSON support](/stable/explore/ysql-language-features/jsonb-ysql/)
-
[XML support](/stable/explore/ysql-language-features/xml-ysql/)
-
[Indexes](/stable/explore/ysql-language-features/indexes-constraints/)
-
[Primary keys](/stable/explore/ysql-language-features/indexes-constraints/primary-key-ysql/)
-
[Secondary indexes](/stable/explore/ysql-language-features/indexes-constraints/secondary-indexes-ysql/)
-
[Unique indexes](/stable/explore/ysql-language-features/indexes-constraints/unique-index-ysql/)
-
[Partial indexes](/stable/explore/ysql-language-features/indexes-constraints/partial-index-ysql/)
-
[Covering indexes](/stable/explore/ysql-language-features/indexes-constraints/covering-index-ysql/)
-
[Expression indexes](/stable/explore/ysql-language-features/indexes-constraints/expression-index-ysql/)
-
[GIN indexes](/stable/explore/ysql-language-features/indexes-constraints/gin/)
-
[Index backfill](/stable/explore/ysql-language-features/indexes-constraints/index-backfill/)
-
[Advanced features](/stable/explore/ysql-language-features/advanced-features/)
-
[Collations](/stable/explore/ysql-language-features/advanced-features/collations/)
-
[Cursors](/stable/explore/ysql-language-features/advanced-features/cursor/)
-
[Foreign data wrappers](/stable/explore/ysql-language-features/advanced-features/foreign-data-wrappers/)
-
[Savepoints](/stable/explore/ysql-language-features/advanced-features/savepoints/)
-
[Stored procedures](/stable/explore/ysql-language-features/advanced-features/stored-procedures/)
-
[Table partitioning](/stable/explore/ysql-language-features/advanced-features/partitions/)
-
[Triggers](/stable/explore/ysql-language-features/advanced-features/triggers/)
-
[Parallel index scans](/stable/explore/ysql-language-features/advanced-features/parallel-index-scan/)
-
[Synchronize snapshots](/stable/explore/ysql-language-features/advanced-features/snapshot-synchronization/)
-
[Views](/stable/explore/ysql-language-features/advanced-features/views/)
-
[Table inheritance](/stable/explore/ysql-language-features/advanced-features/inheritance/)
-
[PostgreSQL extensions](/stable/explore/ysql-language-features/pg-extensions/)
-
[Beyond PostgreSQL](/stable/explore/going-beyond-sql/)
-
[Follower reads](/stable/explore/going-beyond-sql/follower-reads-ysql/)
-
[Geo-placement](/stable/explore/going-beyond-sql/tablespaces/)
-
[Configurable data sharding](/stable/explore/going-beyond-sql/data-sharding/)
-
[xCluster - Asynchronous replication](/stable/explore/going-beyond-sql/asynchronous-replication-ysql/)
-
[Cluster topology](/stable/explore/going-beyond-sql/cluster-topology/)
-
[Cluster-aware drivers](/stable/explore/going-beyond-sql/cluster-aware-drivers/)
-
[Topology-aware drivers](/stable/explore/going-beyond-sql/topology-aware-drivers/)
-
[Built-in connection pooling](/stable/explore/going-beyond-sql/connection-mgr-ysql/)
-
[Decouple storage and compute](/stable/explore/going-beyond-sql/decoupling-compute-storage/)
-
[YCQL features](/stable/explore/ycql-language/)
-
[Cassandra feature support](/stable/explore/ycql-language/cassandra-feature-support/)
-
[Keyspaces and tables](/stable/explore/ycql-language/keyspaces-tables/)
-
[Data types](/stable/explore/ycql-language/data-types/)
-
[Indexes and constraints](/stable/explore/ycql-language/indexes-constraints/)
-
[Primary keys](/stable/explore/ycql-language/indexes-constraints/primary-key-ycql/)
-
[Secondary indexes](/stable/explore/ycql-language/indexes-constraints/secondary-indexes-ycql/)
-
[Unique indexes](/stable/explore/ycql-language/indexes-constraints/unique-index-ycql/)
-
[Partial indexes](/stable/explore/ycql-language/indexes-constraints/partial-index-ycql/)
-
[Covering indexes](/stable/explore/ycql-language/indexes-constraints/covering-index-ycql/)
-
[Secondary indexes with JSONB](/stable/explore/ycql-language/indexes-constraints/secondary-indexes-with-jsonb-ycql/)
-
[JSON support](/stable/explore/ycql-language/jsonb-ycql/)
-
[Gen-AI apps](/stable/explore/gen-ai-apps/)
-
[Horizontal scalability](/stable/explore/linear-scalability/)
-
[Horizontal vs vertical](/stable/explore/linear-scalability/horizontal-vs-vertical-scaling/)
-
[Data distribution](/stable/explore/linear-scalability/data-distribution/)
-
[Adding nodes](/stable/explore/linear-scalability/node-addition/)
-
[Scaling reads](/stable/explore/linear-scalability/scaling-reads/)
-
[Scaling writes](/stable/explore/linear-scalability/scaling-writes/)
-
[Scaling transactions](/stable/explore/linear-scalability/scaling-transactions/)
-
[Large datasets](/stable/explore/linear-scalability/scaling-large-datasets/)
-
[Scale out a universe](/stable/explore/linear-scalability/scaling-universe/)
-
[Resiliency](/stable/explore/fault-tolerance/)
-
[Node failures](/stable/explore/fault-tolerance/macos/)
-
[Rack failures](/stable/explore/fault-tolerance/handling-rack-failures/)
-
[Zone failures](/stable/explore/fault-tolerance/handling-zone-failures/)
-
[Region failures](/stable/explore/fault-tolerance/handling-region-failures/)
-
[Gray failures](/stable/explore/fault-tolerance/handling-gray-failures/)
-
[Periodic maintenance](/stable/explore/fault-tolerance/handling-node-upgrades/)
-
[Transactions](/stable/explore/fault-tolerance/transaction-availability/)
-
[Transactions](/stable/explore/transactions/)
-
[Distributed transactions](/stable/explore/transactions/distributed-transactions-ysql/)
-
[Isolation levels](/stable/explore/transactions/isolation-levels/)
-
[Explicit locking](/stable/explore/transactions/explicit-locking/)
-
[Transactional DDL](/stable/explore/transactions/transactional-ddl/)
-
[Faster writes to new tables](/stable/explore/transactions/new-table-writes/)
-
[Multi-region deployments](/stable/explore/multi-region-deployments/)
-
[Synchronous (3+ regions)](/stable/explore/multi-region-deployments/synchronous-replication-ysql/)
-
[Row-level geo-partitioning](/stable/explore/multi-region-deployments/row-level-geo-partitioning/)
-
[Read replicas](/stable/explore/multi-region-deployments/read-replicas-ysql/)
-
[Change data capture](/stable/explore/change-data-capture/)
-
[Cluster management](/stable/explore/cluster-management/)
-
[Point-in-time recovery](/stable/explore/cluster-management/point-in-time-recovery-ysql/)
-
[Observability](/stable/explore/observability/)
-
[Prometheus integration](/stable/explore/observability/prometheus-integration/)
-
[Grafana dashboard](/stable/explore/observability/grafana-dashboard/grafana/)
-
[Cluster-wide views](/stable/explore/observability/cluster-wide-db-views/)
-
[Live queries](/stable/explore/observability/pg-stat-activity/)
-
[Local tablet metadata](/stable/explore/observability/yb-local-tablets/)
-
[Cluster tablet metadata](/stable/explore/observability/yb-tablet-metadata/)
-
[Terminated queries](/stable/explore/observability/yb-pg-stat-get-queries/)
-
[Data transfer status](/stable/explore/observability/pg-stat-progress-copy/)
-
[Lock insights](/stable/explore/observability/pg-locks/)
-
[Active Session History](/stable/explore/observability/active-session-history/)
-
[Logs](/stable/explore/observability/logging/)
-
[Security](/stable/explore/security/security/)
-
[Secure](/stable/secure/)
-
[Security checklist](/stable/secure/security-checklist/)
-
[Enable authentication](/stable/secure/enable-authentication/)
-
[Enable users](/stable/secure/enable-authentication/authentication-ysql/)
-
[Create login profiles](/stable/secure/enable-authentication/ysql-login-profiles/)
-
[Configure client authentication](/stable/secure/enable-authentication/ysql_hba_conf-configuration/)
-
[Authentication methods](/stable/secure/authentication/)
-
[Password authentication](/stable/secure/authentication/password-authentication/)
-
[LDAP authentication](/stable/secure/authentication/ldap-authentication-ysql/)
-
[OIDC authentication](/stable/secure/authentication/oidc-authentication-ycql/)
-
[Host-based authentication](/stable/secure/authentication/host-based-authentication/)
-
[Trust authentication](/stable/secure/authentication/trust-authentication/)
-
[Role-based access control](/stable/secure/authorization/)
-
[Overview](/stable/secure/authorization/rbac-model/)
-
[Manage users and roles](/stable/secure/authorization/create-roles/)
-
[Grant privileges](/stable/secure/authorization/ysql-grant-permissions/)
-
[Row-level security](/stable/secure/authorization/row-level-security/)
-
[Column-level security](/stable/secure/authorization/column-level-security/)
-
[Encryption in transit](/stable/secure/tls-encryption/)
-
[Create server certificates](/stable/secure/tls-encryption/server-certificates/)
-
[Enable encryption in transit](/stable/secure/tls-encryption/server-to-server/)
-
[Connect to clusters](/stable/secure/tls-encryption/connect-to-cluster/)
-
[TLS and authentication](/stable/secure/tls-encryption/tls-authentication/)
-
[Encryption at rest](/stable/secure/encryption-at-rest/)
-
[Column-level encryption](/stable/secure/column-level-encryption/)
-
[Audit logging](/stable/secure/audit-logging/)
-
[Trace statements](/stable/secure/audit-logging/trace-statements-ysql/)
-
[Configure audit logging](/stable/secure/audit-logging/audit-logging-ysql/)
-
[Session-level audit logging](/stable/secure/audit-logging/session-audit-logging-ysql/)
-
[Object-level audit logging](/stable/secure/audit-logging/object-audit-logging-ysql/)
-
[Vulnerability disclosure policy](/stable/secure/vulnerability-disclosure-policy/)
-
[Launch and Manage](/stable/launch-and-manage/)
-
[Deploy](/stable/deploy/)
-
[Deployment checklist](/stable/deploy/checklist/)
-
[Single-DC deployments](/stable/deploy/manual-deployment/)
-
[1. System configuration](/stable/deploy/manual-deployment/system-config/)
-
[2. Install software](/stable/deploy/manual-deployment/install-software/)
-
[3. Deploy](/stable/deploy/manual-deployment/start-yugabyted/)
-
[4. Verify deployment](/stable/deploy/manual-deployment/verify-deployment-yugabyted/)
-
[Multi-DC deployments](/stable/deploy/multi-dc/)
-
[Three+ data center (3DC)](/stable/deploy/multi-dc/3dc-deployment/)
-
[xCluster](/stable/deploy/multi-dc/async-replication/)
-
[Transactional](/stable/deploy/multi-dc/async-replication/async-replication-transactional/)
-
[Setup](/stable/deploy/multi-dc/async-replication/async-transactional-setup-automatic/)
-
[Failover](/stable/deploy/multi-dc/async-replication/async-transactional-failover/)
-
[Switchover](/stable/deploy/multi-dc/async-replication/async-transactional-switchover/)
-
[Manual DDL changes](/stable/deploy/multi-dc/async-replication/async-transactional-tables/)
-
[Non-transactional](/stable/deploy/multi-dc/async-replication/async-deployment/)
-
[Read replicas](/stable/deploy/multi-dc/read-replica-clusters/)
-
[Public clouds](/stable/deploy/public-clouds/)
-
[Amazon Web Services](/stable/deploy/public-clouds/aws/cloudformation/)
-
[Google Cloud Platform](/stable/deploy/public-clouds/gcp/gcp-deployment-manager/)
-
[Microsoft Azure](/stable/deploy/public-clouds/azure/azure-arm/)
-
[Kubernetes](/stable/deploy/kubernetes/)
-
[Single-zone](/stable/deploy/kubernetes/single-zone/)
-
[Open Source](/stable/deploy/kubernetes/single-zone/oss/helm-chart/)
-
[Amazon EKS](/stable/deploy/kubernetes/single-zone/eks/helm-chart/)
-
[Google Kubernetes Engine](/stable/deploy/kubernetes/single-zone/gke/helm-chart/)
-
[Azure Kubernetes Service](/stable/deploy/kubernetes/single-zone/aks/helm-chart/)
-
[Multi-zone](/stable/deploy/kubernetes/multi-zone/)
-
[Amazon EKS](/stable/deploy/kubernetes/multi-zone/eks/helm-chart/)
-
[Google Kubernetes Engine](/stable/deploy/kubernetes/multi-zone/gke/helm-chart/)
-
[Multi-cluster](/stable/deploy/kubernetes/multi-cluster/)
-
[Google Kubernetes Engine](/stable/deploy/kubernetes/multi-cluster/gke/helm-chart/)
-
[Best practices](/stable/deploy/kubernetes/best-practices/)
-
[Connect Clients](/stable/deploy/kubernetes/clients/)
-
[Advanced capabilities](/stable/additional-features/)
-
[YSQL Connection Manager](/stable/additional-features/connection-manager-ysql/)
-
[Setup](/stable/additional-features/connection-manager-ysql/ycm-setup/)
-
[Best practices](/stable/additional-features/connection-manager-ysql/ycm-best-practices/)
-
[Observability](/stable/additional-features/connection-manager-ysql/ycm-monitor/)
-
[Migrate](/stable/additional-features/connection-manager-ysql/ycm-migrate/)
-
[Troubleshoot](/stable/additional-features/connection-manager-ysql/ycm-troubleshoot/)
-
[Change data capture](/stable/additional-features/change-data-capture/)
-
[PostgreSQL protocol](/stable/additional-features/change-data-capture/using-logical-replication/)
-
[Key concepts](/stable/additional-features/change-data-capture/using-logical-replication/key-concepts/)
-
[Get started](/stable/additional-features/change-data-capture/using-logical-replication/get-started/)
-
[Monitor](/stable/additional-features/change-data-capture/using-logical-replication/monitor/)
-
[Advanced configuration](/stable/additional-features/change-data-capture/using-logical-replication/advanced-configuration/)
-
[Advanced topics](/stable/additional-features/change-data-capture/using-logical-replication/advanced-topic/)
-
[Best practices](/stable/additional-features/change-data-capture/using-logical-replication/best-practices/)
-
[YugabyteDB connector](/stable/additional-features/change-data-capture/using-logical-replication/yugabytedb-connector/)
-
[Connector properties](/stable/additional-features/change-data-capture/using-logical-replication/yugabytedb-connector-properties/)
-
[Connector transformers](/stable/additional-features/change-data-capture/using-logical-replication/transformers/)
-
[Upgrade connector](/stable/additional-features/change-data-capture/using-logical-replication/upgrade-connector/)
-
[gRPC protocol](/stable/additional-features/change-data-capture/using-yugabytedb-grpc-replication/)
-
[Get started](/stable/additional-features/change-data-capture/using-yugabytedb-grpc-replication/cdc-get-started/)
-
[Monitor](/stable/additional-features/change-data-capture/using-yugabytedb-grpc-replication/cdc-monitor/)
-
[YugabyteDB gRPC Connector](/stable/additional-features/change-data-capture/using-yugabytedb-grpc-replication/debezium-connector-yugabytedb/)
-
[Connector transformers](/stable/additional-features/change-data-capture/using-yugabytedb-grpc-replication/yugabytedb-grpc-transformers/)
-
[Upgrade connector](/stable/additional-features/change-data-capture/using-yugabytedb-grpc-replication/upgrade-connector/)
-
[Flink CDC](/stable/additional-features/change-data-capture/using-flink-cdc/)
-
[Get started](/stable/additional-features/change-data-capture/using-flink-cdc/get-started/)
-
[Multitenancy](/stable/additional-features/multitenancy/)
-
[Set up](/stable/additional-features/multitenancy/set-up/)
-
[Observability](/stable/additional-features/multitenancy/monitor/)
-
[Colocation](/stable/additional-features/colocation/)
-
[Parallel queries](/stable/additional-features/parallel-query/)
-
[PostgreSQL extensions](/stable/additional-features/pg-extensions/)
-
[Install extensions](/stable/additional-features/pg-extensions/install-extensions/)
-
[Anonymizer](/stable/additional-features/pg-extensions/extension-pganon/)
-
[auto_explain](/stable/additional-features/pg-extensions/extension-auto-explain/)
-
[DocumentDB](/stable/additional-features/pg-extensions/extension-documentdb/)
-
[file_fdw](/stable/additional-features/pg-extensions/extension-file-fdw/)
-
[fuzzystrmatch](/stable/additional-features/pg-extensions/extension-fuzzystrmatch/)
-
[HypoPG](/stable/additional-features/pg-extensions/extension-hypopg/)
-
[passwordcheck](/stable/additional-features/pg-extensions/extension-passwordcheck/)
-
[pg_cron](/stable/additional-features/pg-extensions/extension-pgcron/)
-
[pg_parquet](/stable/additional-features/pg-extensions/extension-pgparquet/)
-
[pg_partman](/stable/additional-features/pg-extensions/extension-pgpartman/)
-
[pg_stat_statements](/stable/additional-features/pg-extensions/extension-pgstatstatements/)
-
[pgcrypto](/stable/additional-features/pg-extensions/extension-pgcrypto/)
-
[pgvector](/stable/additional-features/pg-extensions/extension-pgvector/)
-
[postgres_fdw](/stable/additional-features/pg-extensions/extension-postgres-fdw/)
-
[postgresql-hll](/stable/additional-features/pg-extensions/extension-postgresql-hll/)
-
[spi](/stable/additional-features/pg-extensions/extension-spi/)
-
[tablefunc](/stable/additional-features/pg-extensions/extension-tablefunc/)
-
[uuid-ossp](/stable/additional-features/pg-extensions/extension-uuid-ossp/)
-
[Auto Analyze](/stable/additional-features/auto-analyze/)
-
[Manage](/stable/manage/)
-
[Backup and restore](/stable/manage/backup-restore/)
-
[Export and import](/stable/manage/backup-restore/export-import-data-ysql/)
-
[Distributed snapshots](/stable/manage/backup-restore/snapshot-ysql/)
-
[Point-in-time recovery](/stable/manage/backup-restore/point-in-time-recovery/)
-
[Enable and disable](/stable/manage/backup-restore/point-in-time-recovery/enable-pitr/)
-
[Inspect at PIT](/stable/manage/backup-restore/point-in-time-recovery/inspect/)
-
[Clone to PIT](/stable/manage/backup-restore/point-in-time-recovery/clone/)
-
[Rewind to PIT](/stable/manage/backup-restore/point-in-time-recovery/rewind/)
-
[Restore to PIT](/stable/manage/backup-restore/point-in-time-recovery/restore/)
-
[Migrate](/stable/manage/data-migration/)
-
[Export data](/stable/manage/data-migration/bulk-export-ysql/)
-
[Import data](/stable/manage/data-migration/bulk-import-ysql/)
-
[Verify migration](/stable/manage/data-migration/verify-migration-ysql/)
-
[Migrate from PostgreSQL](/stable/manage/data-migration/migrate-from-postgres/)
-
[Change cluster configuration](/stable/manage/change-cluster-config/)
-
[Diagnostics reporting](/stable/manage/diagnostics-reporting/)
-
[Upgrade YugabyteDB](/stable/manage/upgrade-deployment/)
-
[YSQL major upgrade](/stable/manage/ysql-major-upgrade-yugabyted/)
-
[Kubernetes](/stable/manage/upgrade-deployment-kubernetes/)
-
[Monitor](/stable/launch-and-manage/monitor-and-alert/)
-
[Metrics](/stable/launch-and-manage/monitor-and-alert/metrics/)
-
[Throughput+latency metrics](/stable/launch-and-manage/monitor-and-alert/metrics/throughput/)
-
[Connection metrics](/stable/launch-and-manage/monitor-and-alert/metrics/connections/)
-
[Cache and storage metrics](/stable/launch-and-manage/monitor-and-alert/metrics/cache-storage/)
-
[Raft metrics](/stable/launch-and-manage/monitor-and-alert/metrics/raft-dst/)
-
[YB-Master metrics](/stable/launch-and-manage/monitor-and-alert/metrics/ybmaster/)
-
[xCluster](/stable/launch-and-manage/monitor-and-alert/metrics/replication/)
-
[xCluster](/stable/launch-and-manage/monitor-and-alert/xcluster-monitor/)
-
[Active Session History](/stable/launch-and-manage/monitor-and-alert/active-session-history-monitor/)
-
[Tablet metadata](/stable/launch-and-manage/monitor-and-alert/tablet-metadata/)
-
[Cluster-wide views](/stable/launch-and-manage/monitor-and-alert/cluster-wide-db-views/)
-
[YSQL Distributed Tracing](/stable/launch-and-manage/monitor-and-alert/ysql-distributed-tracing/)
-
[Query tuning](/stable/launch-and-manage/monitor-and-alert/query-tuning/)
-
[Get query statistics](/stable/launch-and-manage/monitor-and-alert/query-tuning/pg-stat-statements/)
-
[Column statistics](/stable/launch-and-manage/monitor-and-alert/query-tuning/pg-stats/)
-
[Analyze queries](/stable/launch-and-manage/monitor-and-alert/query-tuning/explain-analyze/)
-
[Query diagnostics](/stable/launch-and-manage/monitor-and-alert/query-tuning/query-diagnostics/)
-
[Temporal join scans](/stable/launch-and-manage/monitor-and-alert/query-tuning/parallel-temporal-join/)
-
[Optimize YSQL queries](/stable/launch-and-manage/monitor-and-alert/query-tuning/pg-hint-plan/)
-
[Query plan management](/stable/launch-and-manage/monitor-and-alert/query-tuning/query-plan-manage/)
-
[Best practices](/stable/best-practices-operations/)
-
[YSQL database administrators](/stable/best-practices-operations/administration/)
-
[YSQL catalog cache tuning](/stable/best-practices-operations/ysql-catalog-cache-tuning-guide/)
-
[YSQL cost-based optimizer](/stable/best-practices-operations/ysql-yb-enable-cbo/)
-
[Troubleshoot](/stable/troubleshoot/)
-
[Cluster-level issues](/stable/troubleshoot/cluster/)
-
[YCQL API connection issues](/stable/troubleshoot/cluster/connect-ycql/)
-
[Recover YB-TServer and YB-Master](/stable/troubleshoot/cluster/recover_server/)
-
[Replace a failed YB-TServer](/stable/troubleshoot/cluster/replace_tserver/)
-
[Replace a failed YB-Master](/stable/troubleshoot/cluster/replace_master/)
-
[Manual remote bootstrap of failed peer](/stable/troubleshoot/cluster/replace_failed_peers/)
-
[Recover YB-TServer from crash loop](/stable/troubleshoot/cluster/failed_tablets/)
-
[Performance issues](/stable/troubleshoot/cluster/performance-troubleshooting/)
-
[Node-level issues](/stable/troubleshoot/nodes/)
-
[Check servers](/stable/troubleshoot/nodes/check-processes/)
-
[System statistics](/stable/troubleshoot/nodes/check-stats/)
-
[Disk failure](/stable/troubleshoot/nodes/recover-disk/)
-
[Disk full](/stable/troubleshoot/nodes/disk-full/)
-
[Common error messages](/stable/troubleshoot/nodes/trouble-common/)
-
[YSQL issues](/stable/troubleshoot/ysql-issues/)
-
[Other issues](/stable/troubleshoot/other-issues/)
-
Reference
-
[Architecture](/stable/architecture/)
-
[Key concepts](/stable/architecture/key-concepts/)
-
[Design goals](/stable/architecture/design-goals/)
-
[YQL - Query layer](/stable/architecture/query-layer/)
-
[Query Planner](/stable/architecture/query-layer/planner-optimizer/)
-
[Join Strategies](/stable/architecture/query-layer/join-strategies/)
-
[System catalog](/stable/architecture/system-catalog/)
-
[DocDB - Storage layer](/stable/architecture/docdb/)
-
[Data model](/stable/architecture/docdb/data-model/)
-
[Packed rows](/stable/architecture/docdb/packed-rows/)
-
[LSM & SST](/stable/architecture/docdb/lsm-sst/)
-
[Performance](/stable/architecture/docdb/performance/)
-
[Sharding](/stable/architecture/docdb-sharding/)
-
[Hash and range sharding](/stable/architecture/docdb-sharding/sharding/)
-
[Tablet splitting](/stable/architecture/docdb-sharding/tablet-splitting/)
-
[Cluster balancing](/stable/architecture/docdb-sharding/cluster-balancing/)
-
[Replication](/stable/architecture/docdb-replication/)
-
[Raft](/stable/architecture/docdb-replication/raft/)
-
[Synchronous](/stable/architecture/docdb-replication/replication/)
-
[xCluster](/stable/architecture/docdb-replication/async-replication/)
-
[Read replicas](/stable/architecture/docdb-replication/read-replicas/)
-
[CDC using PostgreSQL protocol](/stable/architecture/docdb-replication/cdc-logical-replication/)
-
[CDC using gRPC protocol](/stable/architecture/docdb-replication/change-data-capture/)
-
[Transactions](/stable/architecture/transactions/)
-
[Fundamentals](/stable/architecture/transactions/transactions-overview/)
-
[Distributed transactions](/stable/architecture/transactions/distributed-txns/)
-
[Transactional I/O path](/stable/architecture/transactions/transactional-io-path/)
-
[Transactional DDL](/stable/architecture/transactions/transactional-ddl/)
-
[Skip intents optimization](/stable/architecture/transactions/skip-intents/)
-
[Single-row transactions](/stable/architecture/transactions/single-row-transactions/)
-
[Isolation levels](/stable/architecture/transactions/isolation-levels/)
-
[Concurrency control](/stable/architecture/transactions/concurrency-control/)
-
[Transaction priorities](/stable/architecture/transactions/transaction-priorities/)
-
[Read Committed](/stable/architecture/transactions/read-committed/)
-
[Read Restart error](/stable/architecture/transactions/read-restart-error/)
-
[YB-Master](/stable/architecture/yb-master/)
-
[YB-TServer](/stable/architecture/yb-tserver/)
-
[Configuration](/stable/reference/configuration/)
-
[yugabyted](/stable/reference/configuration/yugabyted/)
-
[yb-master](/stable/reference/configuration/yb-master/)
-
[yb-tserver](/stable/reference/configuration/yb-tserver/)
-
[Operating systems](/stable/reference/configuration/operating-systems/)
-
[Default ports](/stable/reference/configuration/default-ports/)
-
[Smart defaults](/stable/reference/configuration/smart-defaults/)
-
[Enhanced PG compatibility](/stable/reference/configuration/postgresql-compatibility/)
-
[CLIs](/stable/admin/)
-
[yb-admin](/stable/admin/yb-admin/)
-
[yb-ts-cli](/stable/admin/yb-ts-cli/)
-
[ysql_dump](/stable/admin/ysql-dump/)
-
[ysql_dumpall](/stable/admin/ysql-dumpall/)
-
[yb-ctl](/stable/admin/yb-ctl/)
-
[yb-docker-ctl](/stable/admin/yb-docker-ctl/)
-
[Docs MCP Server](/stable/reference/docs-mcp-server/)
-
[Resource guide](/stable/reference/get-started-guide/)
-
Misc
-
[YEDIS](/stable/yedis/)
-
[Quick start](/stable/yedis/quick-start/)
-
[Develop](/stable/yedis/develop/)
-
[Build an application](/stable/yedis/develop/client-drivers/)
-
[C#](/stable/yedis/develop/client-drivers/yedis/csharp/)
-
[C++](/stable/yedis/develop/client-drivers/yedis/cpp/)
-
[Go](/stable/yedis/develop/client-drivers/yedis/go/)
-
[Java](/stable/yedis/develop/client-drivers/yedis/java/)
-
[NodeJS](/stable/yedis/develop/client-drivers/yedis/nodejs/)
-
[Python](/stable/yedis/develop/client-drivers/yedis/python/)
-
[API reference](/stable/yedis/api/)
-
[APPEND](/stable/yedis/api/append/)
-
[AUTH](/stable/yedis/api/auth/)
-
[CONFIG](/stable/yedis/api/config/)
-
[CREATEDB](/stable/yedis/api/createdb/)
-
[DELETEDB](/stable/yedis/api/deletedb/)
-
[LISTDB](/stable/yedis/api/listdb/)
-
[SELECT](/stable/yedis/api/select/)
-
[DEL](/stable/yedis/api/del/)
-
[ECHO](/stable/yedis/api/echo/)
-
[EXISTS](/stable/yedis/api/exists/)
-
[EXPIRE](/stable/yedis/api/expire/)
-
[EXPIREAT](/stable/yedis/api/expireat/)
-
[FLUSHALL](/stable/yedis/api/flushall/)
-
[FLUSHDB](/stable/yedis/api/flushdb/)
-
[GET](/stable/yedis/api/get/)
-
[GETRANGE](/stable/yedis/api/getrange/)
-
[GETSET](/stable/yedis/api/getset/)
-
[HDEL](/stable/yedis/api/hdel/)
-
[HEXISTS](/stable/yedis/api/hexists/)
-
[HGET](/stable/yedis/api/hget/)
-
[HGETALL](/stable/yedis/api/hgetall/)
-
[HINCRBY](/stable/yedis/api/hincrby/)
-
[HKEYS](/stable/yedis/api/hkeys/)
-
[HLEN](/stable/yedis/api/hlen/)
-
[HMGET](/stable/yedis/api/hmget/)
-
[HMSET](/stable/yedis/api/hmset/)
-
[HSET](/stable/yedis/api/hset/)
-
[HSTRLEN](/stable/yedis/api/hstrlen/)
-
[HVALS](/stable/yedis/api/hvals/)
-
[INCR](/stable/yedis/api/incr/)
-
[INCRBY](/stable/yedis/api/incrby/)
-
[KEYS](/stable/yedis/api/keys/)
-
[MONITOR](/stable/yedis/api/monitor/)
-
[PEXPIRE](/stable/yedis/api/pexpire/)
-
[PEXPIREAT](/stable/yedis/api/pexpireat/)
-
[PTTL](/stable/yedis/api/pttl/)
-
[ROLE](/stable/yedis/api/role/)
-
[SADD](/stable/yedis/api/sadd/)
-
[SCARD](/stable/yedis/api/scard/)
-
[RENAME](/stable/yedis/api/rename/)
-
[SET](/stable/yedis/api/set/)
-
[SETEX](/stable/yedis/api/setex/)
-
[PSETEX](/stable/yedis/api/psetex/)
-
[SETRANGE](/stable/yedis/api/setrange/)
-
[SISMEMBER](/stable/yedis/api/sismember/)
-
[SMEMBERS](/stable/yedis/api/smembers/)
-
[SREM](/stable/yedis/api/srem/)
-
[STRLEN](/stable/yedis/api/strlen/)
-
[ZRANGE](/stable/yedis/api/zrange/)
-
[TSADD](/stable/yedis/api/tsadd/)
-
[TSCARD](/stable/yedis/api/tscard/)
-
[TSGET](/stable/yedis/api/tsget/)
-
[TSLASTN](/stable/yedis/api/tslastn/)
-
[TSRANGEBYTIME](/stable/yedis/api/tsrangebytime/)
-
[TSREM](/stable/yedis/api/tsrem/)
-
[TSREVRANGEBYTIME](/stable/yedis/api/tsrevrangebytime/)
-
[TTL](/stable/yedis/api/ttl/)
-
[ZADD](/stable/yedis/api/zadd/)
-
[ZCARD](/stable/yedis/api/zcard/)
-
[ZRANGEBYSCORE](/stable/yedis/api/zrangebyscore/)
-
[ZREM](/stable/yedis/api/zrem/)
-
[ZREVRANGE](/stable/yedis/api/zrevrange/)
-
[ZSCORE](/stable/yedis/api/zscore/)
-
[PUBSUB](/stable/yedis/api/pubsub/)
-
[PUBLISH](/stable/yedis/api/publish/)
-
[SUBSCRIBE](/stable/yedis/api/subscribe/)
-
[UNSUBSCRIBE](/stable/yedis/api/unsubscribe/)
-
[PSUBSCRIBE](/stable/yedis/api/psubscribe/)
-
[PUNSUBSCRIBE](/stable/yedis/api/punsubscribe/)
-
[Legal](/stable/legal/)
-
[Third-party software](/stable/legal/third-party-software/)
-
[Benchmark](/stable/benchmark/)
-
[TPC-C](/stable/benchmark/tpcc/)
-
[Run benchmark](/stable/benchmark/tpcc/running-tpcc/)
-
[Testing horizontal scalability](/stable/benchmark/tpcc/horizontal-scaling/)
-
[Testing high scale workloads](/stable/benchmark/tpcc/high-scale-workloads/)
-
[sysbench](/stable/benchmark/sysbench-ysql/)
-
[YCSB](/stable/benchmark/ycsb-jdbc/)
-
[Key-value workload](/stable/benchmark/key-value-workload-ycql/)
-
[Large datasets](/stable/benchmark/large-datasets-ycql/)
-
[Scalability](/stable/benchmark/scalability/)
-
[Scaling queries](/stable/benchmark/scalability/scaling-queries-ysql/)
-
[Resilience](/stable/benchmark/resilience/)
-
[Jepsen testing](/stable/benchmark/resilience/jepsen-testing/)
-
[Contribute](/stable/contribute/)
-
[Core database](/stable/contribute/core-database/)
-
[Contribution checklist](/stable/contribute/core-database/checklist/)
-
[Build the source](/stable/contribute/core-database/build-from-src-almalinux/)
-
[Configure a CLion project](/stable/contribute/core-database/clion-setup/)
-
[Build and test](/stable/contribute/core-database/build-and-test/)
-
[Coding style](/stable/contribute/core-database/coding-style/)
-
[Merge with upstream repositories](/stable/contribute/core-database/merge-with-upstream-repositories/)
-
[Documentation](/stable/contribute/docs/)
-
[Docs checklist](/stable/contribute/docs/docs-checklist/)
-
[Docs layout](/stable/contribute/docs/docs-layout/)
-
[Build the docs](/stable/contribute/docs/docs-build/)
-
[Editor setup](/stable/contribute/docs/docs-editor-setup/)
-
[Edit the docs](/stable/contribute/docs/docs-edit/)
-
[Docs page structure](/stable/contribute/docs/docs-page-structure/)
-
[Widgets and shortcodes](/stable/contribute/docs/widgets-and-shortcodes/)
-
[Syntax diagrams](/stable/contribute/docs/syntax-diagrams/)
-
[Page with elements](/stable/contribute/docs/all-page-elements/)
-
[Style guide](/stable/contribute/docs/docs-style/)
-
[Download](https://download.yugabyte.com/)
-
Join our community
-
[Slack](https://inviter.co/yugabytedb)
-
[Yugabyte University](https://university.yugabyte.com/)
-
[GitHub](https://github.com/yugabyte/yugabyte-db)
-
[Yugabyte Friday Tech Talks](https://www.yugabyte.com/yftt/)
-
[Forum](https://forum.yugabyte.com/)
-
[Contact Support](https://support.yugabyte.com/hc/en-us)
-
[YugabyteDB](/stable/)
-
Architecture
[v2026.1 STS Stable release with standard-term support](#)
[v2026.1 STS Stable release with standard-term support](/stable/architecture/)
[v2025.2 LTS Stable release with long-term support](/v2025.2/architecture/)
[v2025.1 STS Stable release with standard-term support](/v2025.1/architecture/)
[v2024.2 LTS Stable release with long-term support](/v2024.2/architecture/)
[Unsupported versions](https://docs-archive.yugabyte.com/v2.18/)
#
Architecture
Copy page as Markdown
Internals of query, transactions, sharding, replication, and storage layers
-
Contribute
[Report a doc issue](https://github.com/yugabyte/yugabyte-db/issues/new?title=%5BDocs%5D+Architecture&labels=area/documentation&template=docs.yml)
[Suggest new content](https://github.com/yugabyte/yugabyte-db/issues/new?title=%5BDocs%5D+New+docs+proposal&labels=area/documentation&template=docs.yml)
[Edit this page](https://github.com/yugabyte/yugabyte-db/tree/master/docs/content/stable/architecture/_index.md)[View as Markdown](/stable/architecture/index.md)[Contributor guide](/stable/contribute/docs/)
YugabyteDB is a distributed database that seamlessly combines the principles of distributed systems, where multiple machines collaborate, with the familiar concepts of traditional databases, where data is organized in tables with standard interfaces for reading and writing data.
Unlike traditional centralized databases, YugabyteDB is designed to manage and process data across multiple nodes or servers, ensuring resiliency, consistency, high availability, scalability, fault tolerance, and other [design goals](design-goals/).
Check out YugabyteDB [key concepts](./key-concepts/) for your quick reference.
[](./key-concepts/)
## Layered architecture[](#layered-architecture)
In general, operations in YugabyteDB are split logically into 2 layers, the query layer and the storage layer. The query layer is responsible for handling user requests and sending the requests to the right data. The storage layer is responsible for optimally storing the data on disk and managing replication and consistency.
## Query layer[](#query-layer)
For operating (CRUD) on the data that is split and stored across multiple machines, YugabyteDB provides two APIs, YSQL and YCQL. The query layer takes the user query submitted via the API and sends or fetches data to and from the right set of tablets.
To understand how the query layer is designed, see [Query layer](query-layer/).
[](query-layer/)
## Storage layer[](#storage-layer)
The tablet data is optimally stored and managed by DocDB, a document store that has been built on top of RocksDB for higher performance and persistence.
To understand how data storage works in YugabyteDB, see [DocDB](docdb/).
[](docdb/)
## Sharding[](#sharding)
YugabyteDB splits table data into smaller pieces called tablets so that the data can be stored in parts across multiple machines. The mapping of a row to a tablet is deterministic and this process is known as sharding.
To learn more about the various sharding schemes, see [Sharding](docdb-sharding/).
[](docdb-sharding/)
## Replication[](#replication)
Tablets are replicated for resiliency, high availability, and fault tolerance. Each tablet has a leader that is responsible for consistent reads and writes to the data of the tablet and a few followers. The replication is done using the Raft protocol to ensure consistency of data across the leader and followers.
To understand how replication works, see [Replication](docdb-replication/).
[](docdb-replication/)
## Transactions[](#transactions)
Transactions are a set of operations (CRUD) that are executed atomically with the option to roll back all actions if any operation fails.
To understand how transactions work in YugabyteDB, see [Transactions](transactions/).
[](transactions/)
## Master server[](#master-server)
The master service acts as a catalog manager and cluster orchestrator, and manages many background tasks.
For more details, see [YB-Master](./yb-master).
[](./yb-master)
## TServer[](#tserver)
YugabyteDB splits table data into tablets. These tablets are maintained and managed on each node by the TServer.
For more details, see [YB-TServer](./yb-tserver).
[](./yb-tserver)
[](/) [](https://inviter.co/yugabytedb)[](https://github.com/yugabyte/yugabyte-db)[](https://twitter.com/yugabyte)[](https://www.linkedin.com/company/yugabyte)[](https://www.youtube.com/channel/UCL9BhSLRowqQ1TyBndhiCEw)
© 2026 YugabyteDB, Inc. All Rights Reserved [Privacy Policy](https://www.yugabyte.com/privacy-policy/) |
[Terms of Service](https://www.yugabyte.com/terms-of-service/)