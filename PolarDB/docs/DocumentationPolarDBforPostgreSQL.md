# Documentation | PolarDB for PostgreSQL

- 来源: https://polardb.github.io/polardb-pg-docs/
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

[PolarDB for PostgreSQL](/polardb-pg-docs/) Deployment Deployment - [架构简介](/polardb-pg-docs/deploying/introduction.html)
- [快速部署](/polardb-pg-docs/deploying/quick-start.html)
- [进阶部署](/polardb-pg-docs/deploying/deploy.html)
-
#### Preparation of Shared-Storage Device
- [阿里云 ECS + ESSD 云盘存储](/polardb-pg-docs/deploying/storage-aliyun-essd.html)
-
#### Preparation of File System
- [格式化并挂载 PFS](/polardb-pg-docs/deploying/fs-pfs.html)
-
#### Deploying PolarDB
- [基于单机文件系统部署](/polardb-pg-docs/deploying/db-localfs.html)
- [基于 PFS 文件系统部署](/polardb-pg-docs/deploying/db-pfs.html)
-
#### More about Deployment
- [购买商业版](/polardb-pg-docs/deploying/deploy-official.html)
Ops Ops -
#### Daily Ops
- [备份恢复](/polardb-pg-docs/operation/backup-and-restore.html)
- [共享存储在线扩容](/polardb-pg-docs/operation/grow-storage.html)
- [计算节点扩缩容](/polardb-pg-docs/operation/scale-out.html)
- [Replica 节点在线 Promote](/polardb-pg-docs/operation/ro-online-promote.html)
-
#### Benchmarks
- [TPC-C 测试](/polardb-pg-docs/operation/tpcc-test.html)
- [TPC-H 测试](/polardb-pg-docs/operation/tpch-test.html)
[Kernel Features](/polardb-pg-docs/features/)
Theory Theory -
#### PolarDB for PostgreSQL
- [Overview](/polardb-pg-docs/theory/arch-overview.html)
- [HTAP Architecture](/polardb-pg-docs/theory/arch-htap.html)
- [Buffer Management](/polardb-pg-docs/theory/buffer-management.html)
- [DDL Synchronization](/polardb-pg-docs/theory/ddl-synchronization.html)
- [LogIndex](/polardb-pg-docs/theory/logindex.html)
-
#### PostgreSQL
- [Code Analysis of ANALYZE](/polardb-pg-docs/theory/analyze.html)
- [Sequence](/polardb-pg-docs/theory/polar-sequence-tech.html)
Dev Dev - [基于 Docker 容器开发](/polardb-pg-docs/development/dev-on-docker.html)
- [定制开发环境](/polardb-pg-docs/development/customize-dev-env.html)
Contributing Contributing - [Code Contributing](/polardb-pg-docs/contributing/contributing-polardb-kernel.html)
- [Documentation Contributing](/polardb-pg-docs/contributing/contributing-polardb-docs.html)
- [Coding Style](/polardb-pg-docs/contributing/coding-style.html)
- [问题报告](/polardb-pg-docs/contributing/trouble-issuing.html)
Languages Languages - [English](/polardb-pg-docs/)
- [简体中文](/polardb-pg-docs/zh/)
[GitHub](https://github.com/polardb/polardb-pg-docs)
Search K
Deployment Deployment - [架构简介](/polardb-pg-docs/deploying/introduction.html)
- [快速部署](/polardb-pg-docs/deploying/quick-start.html)
- [进阶部署](/polardb-pg-docs/deploying/deploy.html)
-
#### Preparation of Shared-Storage Device
- [阿里云 ECS + ESSD 云盘存储](/polardb-pg-docs/deploying/storage-aliyun-essd.html)
-
#### Preparation of File System
- [格式化并挂载 PFS](/polardb-pg-docs/deploying/fs-pfs.html)
-
#### Deploying PolarDB
- [基于单机文件系统部署](/polardb-pg-docs/deploying/db-localfs.html)
- [基于 PFS 文件系统部署](/polardb-pg-docs/deploying/db-pfs.html)
-
#### More about Deployment
- [购买商业版](/polardb-pg-docs/deploying/deploy-official.html)
Ops Ops -
#### Daily Ops
- [备份恢复](/polardb-pg-docs/operation/backup-and-restore.html)
- [共享存储在线扩容](/polardb-pg-docs/operation/grow-storage.html)
- [计算节点扩缩容](/polardb-pg-docs/operation/scale-out.html)
- [Replica 节点在线 Promote](/polardb-pg-docs/operation/ro-online-promote.html)
-
#### Benchmarks
- [TPC-C 测试](/polardb-pg-docs/operation/tpcc-test.html)
- [TPC-H 测试](/polardb-pg-docs/operation/tpch-test.html)
[Kernel Features](/polardb-pg-docs/features/)
Theory Theory -
#### PolarDB for PostgreSQL
- [Overview](/polardb-pg-docs/theory/arch-overview.html)
- [HTAP Architecture](/polardb-pg-docs/theory/arch-htap.html)
- [Buffer Management](/polardb-pg-docs/theory/buffer-management.html)
- [DDL Synchronization](/polardb-pg-docs/theory/ddl-synchronization.html)
- [LogIndex](/polardb-pg-docs/theory/logindex.html)
-
#### PostgreSQL
- [Code Analysis of ANALYZE](/polardb-pg-docs/theory/analyze.html)
- [Sequence](/polardb-pg-docs/theory/polar-sequence-tech.html)
Dev Dev - [基于 Docker 容器开发](/polardb-pg-docs/development/dev-on-docker.html)
- [定制开发环境](/polardb-pg-docs/development/customize-dev-env.html)
Contributing Contributing - [Code Contributing](/polardb-pg-docs/contributing/contributing-polardb-kernel.html)
- [Documentation Contributing](/polardb-pg-docs/contributing/contributing-polardb-docs.html)
- [Coding Style](/polardb-pg-docs/contributing/coding-style.html)
- [问题报告](/polardb-pg-docs/contributing/trouble-issuing.html)
Languages Languages - [English](/polardb-pg-docs/)
- [简体中文](/polardb-pg-docs/zh/)
[GitHub](https://github.com/polardb/polardb-pg-docs)
# PolarDB for PostgreSQL
A cloud-native database developed by Alibaba Cloud
### [Quick Start with Docker](#quick-start-with-docker)
Pull the [local instance image](https://hub.docker.com/r/polardb/polardb_pg_local_instance/tags) of PolarDB for PostgreSQL based on local storage. Create and run the container, and try PolarDB-PG instance directly:
DockerHub Alibaba Cloud ACR
DockerHub
# pull the instance image and run the container
docker pull polardb/polardb_pg_local_instance:15
docker run -it --cap-add = SYS_PTRACE --privileged = true --rm polardb/polardb_pg_local_instance:15 psql
# check
postgres = # SELECT version();
version
----------------------------------------------------------------------
PostgreSQL 15 .x ( PolarDB 15 .x.x.x build xxxxxxxx ) on { your_platform }
( 1 row )
Alibaba Cloud ACR
# pull the instance image and run the container
docker pull registry.cn-hangzhou.aliyuncs.com/polardb_pg/polardb_pg_local_instance:15
docker run -it --cap-add = SYS_PTRACE --privileged = true --rm registry.cn-hangzhou.aliyuncs.com/polardb_pg/polardb_pg_local_instance:15 psql
# check
postgres = # SELECT version();
version
----------------------------------------------------------------------
PostgreSQL 15 .x ( PolarDB 15 .x.x.x build xxxxxxxx ) on { your_platform }
( 1 row )
Apache 2.0 Licensed | Copyright © Alibaba Group, Inc.