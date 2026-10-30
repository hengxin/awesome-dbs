# Database Benchmarking 资源清单

本目录汇总数据库性能评测相关的论文、基准套件、数据集、评测网站、开源仓库、技术文档与白皮书，按数据库类型分节整理。

论文优先取自本地论文库 `D:\git-papers\`（7,540 篇 PDF，按会议/期刊分目录），本地缺失者再从 arXiv、PVLDB 官方站点、作者课程主页与 GitHub 检索获取；每个下载均做三次重试，仍失败者在文末「未能获取的资源」中逐条列出失败原因与已尝试来源。

## 汇总统计

| 数据库类别 | 论文 | 基准套件/数据集/仓库/文档/网站 | 小计 |
| --- | ---: | ---: | ---: |
| Key-Value | 2 | 1 | 3 |
| SQL/Relational | 14 | 7 | 21 |
| NewSQL | 5 | 2 | 7 |
| Analytical/OLAP | 3 | 4 | 7 |
| Graph | 5 | 8 | 13 |
| Vector | 1 | 4 | 5 |
| Time-Series | 1 | 1 | 2 |
| Document | 2 | 0 | 2 |
| General | 3 | 7 | 10 |
| **合计** | **36** | **34** | **70** |

**资源类型分布**

| 类型 | 数量 |
| --- | ---: |
| 开源仓库 | 17 |
| 网站/排行榜 | 8 |
| 技术文档/规范 | 7 |
| 数据集 | 2 |
| 论文（PDF，已本地存档） | 36 |

**链接可用性**：34 项资源中 30 项有可用入口（其中 0 项出版方页面受限但本地论文库已有副本）；另有 4 项资源经三次重试仍无法获取，已在文末单独列出并给出替代途径。

## 目录结构

```
Benchmarking/
├── BENCHMARKING-INDEX.md      # 本清单
├── papers/<类别>/              # 论文 PDF，按数据库类型分目录
│   ├── Key-Value/
│   ├── SQL/Relational/
│   ├── NewSQL/
│   ├── Analytical/OLAP/
│   ├── Graph/
│   ├── Vector/
│   ├── Time-Series/
│   ├── Document/
│   └── General/
├── SysBench Manual (Alexey Kopytov).pdf
├── TPC-C (v5.11.0).pdf
└── TPC-E (v1.14.0).pdf
```

论文文件命名：`<会议><年份>-<标题去标点与空格>.pdf`，如 `VLDB2023-M2BenchADatabaseBenchmarkforMultiModelAnalyticWorkloads.pdf`。

## 分类清单

### Key-Value

键值存储的基准以读写比、分布倾斜（Zipfian）与范围扫描为核心变量，YCSB 是事实标准。

**论文**

| 引用 | 类型 | 来源 | 适用工作负载 | 本地文件 |
| --- | --- | --- | --- | --- |
| B. F. Cooper, A. Silberstein, E. Tam, R. Ramakrishnan, R. Sears. Benchmarking Cloud Serving Systems with YCSB. SoCC, 2010. | 论文 | [来源](https://www.cs.duke.edu/courses/fall13/compsci590.4/838-CloudPapers/ycsb.pdf) | YCSB A-F | [`SoCC2010-BenchmarkingCloudServingSystemswithYCSB.pdf`](papers/Key-Value/SoCC2010-BenchmarkingCloudServingSystemswithYCSB.pdf) |
| Performance Benchmarking of Key-Value Store NoSQL Databases. Technical Report, 2014. | 论文 | [来源](https://www.researchgate.net/publication/269347728_Performance_Benchmarking_of_Key-Value_Store_NoSQL_Databases) | YCSB 读改写负载；Cassandra / Riak / MongoDB / Redis 对比 | [`TR2014-PerformanceBenchmarkingofKeyValueStoreNoSQLDatabases.pdf`](papers/Key-Value/TR2014-PerformanceBenchmarkingofKeyValueStoreNoSQLDatabases.pdf) |

**基准套件 / 数据集 / 仓库 / 文档 / 网站**

| 名称 | 类型 | 正式名称 | 简称 | 首次发布 | 许可证 | 来源链接 | 适用工作负载 |
| --- | --- | --- | --- | ---: | --- | --- | --- |
| YCSB — Yahoo! Cloud Serving Benchmark | 网站/排行榜 | YCSB (Yahoo! Cloud Serving Benchmark) | YCSB | 2010 | Apache-2.0 | [入口](https://github.com/brianfrankcooper/YCSB) | YCSB A/B/C/D/E/F 工作负载（读更新、日志扫描、读改写、读最新、范围扫描、范围删改） |

### SQL/Relational

关系型数据库的基准围绕事务负载、查询优化器与连接顺序展开，JOB 与 TPC 系列构成主线。

**论文**

| 引用 | 类型 | 来源 | 适用工作负载 | 本地文件 |
| --- | --- | --- | --- | --- |
| M. Raasveldt, P. Holanda, T. Gubner. Fair Benchmarking Considered Difficult: Common Pitfalls in Database Performance Testing. DBTest, 2018. | 论文 | [来源](https://dbtest.cs.umb.edu/) | 方法论：数据规模、预热、并发度、硬件一致性等常见陷阱 | [`DBTest2018-FairBenchmarkingConsideredDifficultCommonPitfallsInDatabasePerformanceTesting.pdf`](papers/General/DBTest2018-FairBenchmarkingConsideredDifficultCommonPitfallsInDatabasePerformanceTesting.pdf) |
| Z. Zhao, H. Gao, N. Xing, L. Zeng. NeurBench: A Benchmark Suite for Learned Database Components with Drift Modeling. SIGMOD, 2026. | 论文 | [来源](https://dl.acm.org/doi/10.1145/3744027) | 学习型基数估计 / 学习索引的数据漂移场景 | [`SIGMOD2026-NeurBenchABenchmarkSuiteforLearnedDatabaseComponentswithDriftModeling.pdf`](papers/General/SIGMOD2026-NeurBenchABenchmarkSuiteforLearnedDatabaseComponentswithDriftModeling.pdf) |
| D. E. Difallah, A. Pavlo, C. Curino, P. Cudre-Mauroux. OLTP-Bench: An Extensible Testbed for Benchmarking Relational Databases. PVLDB, 2014. | 论文 | [来源](https://vldb.org/pvldb/vol7/p277-difallah.pdf) | 可插拔的 OLTP 负载模板（自身负载 + TPC-C 变体） | [`VLDB2014-OLTPBenchAnExtensibleTestbedforBenchmarkingRelationalDatabases.pdf`](papers/SQL/Relational/VLDB2014-OLTPBenchAnExtensibleTestbedforBenchmarkingRelationalDatabases.pdf) |
| V. Leis, A. Gubichev, A. Mirchev, P. Boncz, A. Kemper, T. Neumann. How Good Are Query Optimizers, Really? PVLDB, 2016. | 论文 | [来源](https://vldb.org/pvldb/vol9/p204-leis.pdf) | JOB 113 条连接顺序查询（IMDb SF1） | [`VLDB2016-HowGoodAreQueryOptimizersReally.pdf`](papers/SQL/Relational/VLDB2016-HowGoodAreQueryOptimizersReally.pdf) |
| T. Schmidt, V. Leis, P. Boncz, T. Neumann. SQLStorm: Taking Database Benchmarking into the LLM Era. PVLDB, 2025. | 论文 | [来源](https://www.vldb.org/pvldb/vol18/p4144-schmidt.pdf) | LLM 驱动的自动化负载生成与基准构建 | [`VLDB2025-SQLStormTakingDatabaseBenchmarkingintotheLLMEra.pdf`](papers/General/VLDB2025-SQLStormTakingDatabaseBenchmarkingintotheLLMEra.pdf) |
| V. Leis, A. Gubichev, A. Mirchev, P. Boncz, A. Kemper, T. Neumann. Still Asking: How Good Are Query Optimizers, Really? PVLDB, 2025. | 论文 | [来源](https://www.vldb.org/pvldb/vol18/p5531-viktor.pdf) | JOB 查询集在主流系统上的重测与十年对比 | [`VLDB2025-StillAskingHowGoodAreQueryOptimizersReally.pdf`](papers/SQL/Relational/VLDB2025-StillAskingHowGoodAreQueryOptimizersReally.pdf) |
| T. Jin, Y. Choi, Y. Zhu, D. Kang. Pervasive Annotation Errors Break Text-to-SQL Benchmarks and Leaderboards. PVLDB, 2026. | 论文 | [来源](https://www.vldb.org/pvldb/vol17/p3514-petrycki.pdf) | Spider / BIRD 等基准的标注质量审计 | [`VLDB2026-PervasiveAnnotationErrorsBreakTexttoSQLBenchmarksandLeaderboards.pdf`](papers/SQL/Relational/VLDB2026-PervasiveAnnotationErrorsBreakTexttoSQLBenchmarksandLeaderboards.pdf) |
| J. Lao, A. Zimmerer, O. Ovcharenko, T. Cong, M. Russo. SemBench: A Benchmark for Semantic Query Processing Engines. PVLDB, 2026. | 论文 | [来源](https://www.vldb.org/pvldb/vol19/p1754-trummer.pdf) | 语义查询处理引擎负载（跨域关联推理） | [`VLDB2026-SemBenchaBenchmarkforSemanticQueryProcessingEngines.pdf`](papers/General/VLDB2026-SemBenchaBenchmarkforSemanticQueryProcessingEngines.pdf) |
| TACO: A Benchmark for Open-Domain Text-to-SQL with Ambiguous and Cross-Database Questions. PVLDB, 2026. | 论文 | [来源](https://www.vldb.org/pvldb/vol19/) | 开放域 Text-to-SQL；含歧义与跨库问题 | [`VLDB2026-TACOaBenchmarkforOpenDomainTexttoSQLwithAmbiguousandCrossDatabaseQueries.pdf`](papers/SQL/Relational/VLDB2026-TACOaBenchmarkforOpenDomainTexttoSQLwithAmbiguousandCrossDatabaseQueries.pdf) |
| G. Liu, R. Borovica-Gajic. Toward Drift-Aware Database Benchmarking. PVLDB, 2026. | 论文 | [来源](https://www.vldb.org/pvldb/vol19/) | 考虑数据漂移的负载与评测设计 | [`VLDB2026-TowardDriftAwareDatabaseBenchmarking.pdf`](papers/General/VLDB2026-TowardDriftAwareDatabaseBenchmarking.pdf) |
| D. Gao, H. Wang, Y. Li, X. Sun, Y. Qian, et al. Text-to-SQL Empowered by Large Language Models: A Benchmark Evaluation. arXiv, 2023. | 论文 | [来源](https://arxiv.org/abs/2308.15363) | BIRD 基准上的 Text-to-SQL 评测 | [`arXiv2023-TexttoSQLEmpoweredbyLargeLanguageModelsABenchmarkEvaluation.pdf`](papers/SQL/Relational/arXiv2023-TexttoSQLEmpoweredbyLargeLanguageModelsABenchmarkEvaluation.pdf) |
| D. Liyanage, S. Pandey, J. Goldstein, M. Cahill, A. Dey, A. Fekete, U. Röhm. A Benchmark for Databases with Varying Value Lengths. arXiv, 2025. | 论文 | [来源](https://arxiv.org/abs/2508.07551) | 变长数据（JSON / 文档）负载 | [`arXiv2025-ABenchmarkforDatabaseswithVaryingValueLengths.pdf`](papers/General/arXiv2025-ABenchmarkforDatabaseswithVaryingValueLengths.pdf) |
| W. Zhou, G. Li, H. Wang, Y. Han, X. Wu, F. Wu, X. Zhou. PARROT: A Benchmark for Evaluating LLMs in Cross-System SQL Translation. arXiv, 2025. | 论文 | [来源](https://arxiv.org/pdf/2308.15211) | 跨系统 SQL 翻译（MySQL / PostgreSQL / Oracle 方言互译） | [`arXiv2025-PARROTABenchmarkforEvaluatingLLMsinCrossSystemSQLTranslation.pdf`](papers/SQL/Relational/arXiv2025-PARROTABenchmarkforEvaluatingLLMsinCrossSystemSQLTranslation.pdf) |
| DBA-Bench: A Production-Fidelity Benchmark for LLM-Based Database Operations Agents. arXiv, 2026. | 论文 | [来源](https://arxiv.org/pdf/2508.07551) | 数据库运维代理（DBA agent）的生产级任务负载 | [`arXiv2026-DBABenchAProductionFidelityBenchmarkforLLMBasedDatabaseOperationsAgents.pdf`](papers/General/arXiv2026-DBABenchAProductionFidelityBenchmarkforLLMBasedDatabaseOperationsAgents.pdf) |

**基准套件 / 数据集 / 仓库 / 文档 / 网站**

| 名称 | 类型 | 正式名称 | 简称 | 首次发布 | 许可证 | 来源链接 | 适用工作负载 |
| --- | --- | --- | --- | ---: | --- | --- | --- |
| JOB IMDb Dataset | 数据集 | IMDb Movie Dataset for Join Order Benchmark (SF1) | JOB IMDb SF1 | 2013 | IMDb 数据，仅供研究与评测 | [入口](https://event.cwi.nl/da/job/imdb.tgz) [仓库](https://github.com/gregrahn/join-order-benchmark) | 21 张表、3.7 GiB CSV；最大表 3600 万行 |
| TPC-C Specification | 技术文档/规范 | TPC Benchmark Specification, Revision 5.11 | TPC-C | 2010 | TPC 许可（免费下载） | [入口](https://www.tpc.org/tpcc/doc/tpc-c-v5.11.0.pdf) | TPC-C New-Order / Payment / OrderStatus / Delivery / StockLevel |
| Awesome LLM-based Text2SQL | 开源仓库 | Awesome LLM-based Text2SQL | Awesome-Text2SQL | 2023 | CC BY-SA 4.0 | [入口](https://github.com/DEEP-PolyU/Awesome-LLM-based-Text2SQL) | Spider / BIRD / Dr.Spider 等 Text-to-SQL 基准汇总 |
| BusTub | 开源仓库 | BusTub: A Relational Database Management System (Course Project) | BusTub | 2023 | MIT | [入口](https://github.com/cmu-db/bustub) | TPC-H Q1/Q6/Q12/Q13/Q14/Q15；自建 B+Tree / HashTable / ExtendibleHash 基准 |
| Join Order Benchmark (JOB) | 开源仓库 | Join Order Benchmark (JOB) | JOB | 2015 | IMDb 数据集仅供研究与数据库评测使用 | [入口](https://github.com/gregrahn/join-order-benchmark) | JOB 113 条查询（10 表以上连接、10+ 谓词）；IMDb 2013 数据集 SF1 |
| Lauca | 开源仓库 | Lauca: Workload Duplicator for Benchmarking Transactional Databases | Lauca | 2022 | Apache-2.0 | [入口](https://github.com/luyiqu/Lauca) | 真实事务负载采集与复现（TPC-C 变体） |
| oltpbench | 开源仓库 | oltpbench: Database Benchmarking Framework | oltpbench | 2014 | MIT | [入口](https://github.com/oltpbenchmark/oltpbench) | TPC-C / TPC-H / YCSB / 自定义 Java 负载插件 |

### NewSQL

分布式与 NewSQL 数据库的基准关注水平扩展、弹性伸缩与事务语义，负载通常需要可调节的冲突率与副本数。

**论文**

| 引用 | 类型 | 来源 | 适用工作负载 | 本地文件 |
| --- | --- | --- | --- | --- |
| H. Zhang, L. Qu, Q. Wang, R. Zhang, et al. Dike: A Benchmark Suite for Distributed Transactional Databases. SIGMOD, 2023. | 论文 | [来源](https://dl.acm.org/doi/10.1145/3581784.3607068) | Dike 套件：多类分布式事务负载（隔离级别、读写比、事务组合） | [`SIGMOD2023-DikeABenchmarkSuiteforDistributedTransactionalDatabases.pdf`](papers/NewSQL/SIGMOD2023-DikeABenchmarkSuiteforDistributedTransactionalDatabases.pdf) |
| S. Weng, Q. Wang, L. Qu, R. Zhang, P. Cai, W. Qi. Lauca: A Workload Duplicator for Benchmarking Transactional Database Performance. IEEE TKDE, 2024. | 论文 | [来源](https://ieeexplore.ieee.org/document/9831946) | 真实事务负载回放与复现（TPC-C、YCSB 派生） | [`TKDE2024-LaucaAWorkloadDuplicatorforBenchmarkingTransactionalDatabasePerformance.pdf`](papers/NewSQL/TKDE2024-LaucaAWorkloadDuplicatorforBenchmarkingTransactionalDatabasePerformance.pdf) |
| L. Qu, Q. Wang, T. Chen, K. Li, R. Zhang, X. Zhou. Are Current Benchmarks Adequate to Evaluate Distributed Transactional Databases? Technical Report, 2024. | 论文 | [来源](https://ieeexplore.ieee.org/document/10479300) | TPC-C、YCSB 等现有基准对分布式事务型数据库的适用性分析 | [`TR2024-AreCurrentBenchmarksAdequateToEvaluateDistributedTransactionalDatabases.pdf`](papers/NewSQL/TR2024-AreCurrentBenchmarksAdequateToEvaluateDistributedTransactionalDatabases.pdf) |
| J. Kühlenkamp, M. Klems, O. Röß. Benchmarking Scalability and Elasticity of Distributed Database Systems. PVLDB, 2014. | 论文 | [来源](https://www.vldb.org/pvldb/vol12/p2179-wang.pdf) | 多租户弹性伸缩负载；不同数据规模下的扩展性曲线 | [`VLDB2014-BenchmarkingScalabilityandElasticityofDistributedDatabaseSystems.pdf`](papers/NewSQL/VLDB2014-BenchmarkingScalabilityandElasticityofDistributedDatabaseSystems.pdf) |
| Z. Hu, S. Weng, Z. Pan, R. Zhang, C. Yang. Vodka: Rethink Benchmarking Philosophy in HTAP Systems. PVLDB, 2025. | 论文 | [来源](https://www.vldb.org/pvldb/vol18/p4022-wang.pdf) | HTAP 负载生成与自适应混合负载基准 | [`VLDB2025-VodkaRethinkBenchmarkingPhilosophyinHTAPSystems.pdf`](papers/NewSQL/VLDB2025-VodkaRethinkBenchmarkingPhilosophyinHTAPSystems.pdf) |

**基准套件 / 数据集 / 仓库 / 文档 / 网站**

| 名称 | 类型 | 正式名称 | 简称 | 首次发布 | 许可证 | 来源链接 | 适用工作负载 |
| --- | --- | --- | --- | ---: | --- | --- | --- |
| DeathStarBench | 开源仓库 | DeathStarBench: A Microservice Benchmark Suite | DeathStarBench | 2022 | MIT | [入口](https://github.com/delimitrou/DeathStarBench) | HotelReservation / MovieStreaming 等微服务组合；配 TPC-H 与 YCSB 后端负载 |
| Dike | 开源仓库 | Dike: A Benchmark Suite for Distributed Transactional Databases | Dike | 2023 | 见仓库 | [入口](https://github.com/DBHammer/Dike) | 分布式事务负载矩阵：隔离级别、读写比、事务冲突率 |

### Analytical/OLAP

分析型数据库的基准以大规模扫描、聚合与多模型联合分析为主，关注扫描吞吐与端到端查询时延。

**论文**

| 引用 | 类型 | 来源 | 适用工作负载 | 本地文件 |
| --- | --- | --- | --- | --- |
| I. Giurgiu, S. Barrada, S. Gupta, M. E. Nidd. The Risk and Reward of Cross-Engine Query Partitioning: A Case for Partition-Aware Benchmarking. DBTest, 2026. | 论文 | [来源](https://dbtest.cs.umb.edu/) | 跨引擎查询分区的负载划分与评测 | [`DBTest2026-TheRiskandRewardofCrossEngineQueryPartitioningACaseforPartitionAwareBenchmarking.pdf`](papers/General/DBTest2026-TheRiskandRewardofCrossEngineQueryPartitioningACaseforPartitionAwareBenchmarking.pdf) |
| B. Kim, K. Koo, U. Enkhbat, S. Kim. M2Bench: A Database Benchmark for Multi-Model Analytic Workloads. PVLDB, 2023. | 论文 | [来源](https://www.vldb.org/pvldb/vol16/p747-moon.pdf) | 多模型分析负载（关系+图+文档+空间混合查询） | [`VLDB2023-M2BenchADatabaseBenchmarkforMultiModelAnalyticWorkloads.pdf`](papers/Analytical/OLAP/VLDB2023-M2BenchADatabaseBenchmarkforMultiModelAnalyticWorkloads.pdf) |
| K. Rajan, S. R. Momin, N. Al-Ghosien, N. Bruno, C. Curino, M. Interlandi, Y. Li, L. M. Maas, C. Peeper, S. Chaudhuri, J. Gehrke. Scalable GPU Acceleration of Scalar Functions in Analytical Databases: Compilation, Benchmarking, and Optimization. PVLDB, 2026. | 论文 | [来源](https://www.vldb.org/pvldb/vol18/p3992-zhao.pdf) | TPC-H 标量函数在 GPU 上的加速评测 | [`VLDB2026-ScalableGPUAccelerationofScalarFunctionsinAnalyticalDatabasesCompilationBenchmarkingandOptimization.pdf`](papers/Analytical/OLAP/VLDB2026-ScalableGPUAccelerationofScalarFunctionsinAnalyticalDatabasesCompilationBenchmarkingandOptimization.pdf) |

**基准套件 / 数据集 / 仓库 / 文档 / 网站**

| 名称 | 类型 | 正式名称 | 简称 | 首次发布 | 许可证 | 来源链接 | 适用工作负载 |
| --- | --- | --- | --- | ---: | --- | --- | --- |
| TPC-H Specification | 技术文档/规范 | TPC Benchmark Specification: TPC-H (Decision Support) | TPC-H | 1999 | TPC 许可（免费下载） | [入口](https://www.tpc.org/tph/doc/tph-spec.pdf) | TPC-H Q1-Q22 决策支持查询 |
| TPCx-AI Specification | 技术文档/规范 | TPCx-AI Benchmark Specification (AI and Machine Learning Systems) | TPCx-AI | 2023 | TPC 许可（免费下载） | [入口](https://www.tpc.org/tpcx-ai/) | TPCx-AI 训练与推理场景（14 个用例） |
| ClickBench | 开源仓库 | ClickBench: A Benchmark for ClickHouse | ClickBench | 2023 | Apache-2.0 | [入口](https://github.com/ClickHouse/ClickBench) | 43 个真实场景查询（Hits、Funnel、Trace、Aggregations 等） |
| ClickBench Leaderboard | 网站/排行榜 | ClickBench Results | — | 2023 | — | [入口](https://benchmark.clickhouse.com/) | ClickBench 43 条查询的各系统对比 |

### Graph

图数据库基准由 LDBC 主导，SNB 系列提供标准化社交网络数据与查询集，是图领域最权威的评测体系。

**论文**

| 引用 | 类型 | 来源 | 适用工作负载 | 本地文件 |
| --- | --- | --- | --- | --- |
| O. Erling, A. Averbuch, J. Larriba-Pey, H. Chafi, A. Gubichev, A. Inoue, M. Kayed. The LDBC Social Network Benchmark: Interactive Workload. SIGMOD, 2015. | 论文 | [来源](https://arxiv.org/abs/1407.3487) | 25 条交互式图查询（1-3 跳、度数、连通分量） | [`SIGMOD2015-TheLDBCSocialNetworkBenchmarkInteractiveWorkload.pdf`](papers/Graph/SIGMOD2015-TheLDBCSocialNetworkBenchmarkInteractiveWorkload.pdf) |
| G. Szárnyas, J. Waudby, B. A. Steer, D. Szakállas, A. Birler. The LDBC Social Network Benchmark: Business Intelligence Workload. PVLDB, 2023. | 论文 | — | 13 条 BI 分析查询（PageRank、连通分量、社区检测） | [`VLDB2023-TheLDBCSocialNetworkBenchmarkBusinessIntelligenceWorkload.pdf`](papers/Graph/VLDB2023-TheLDBCSocialNetworkBenchmarkBusinessIntelligenceWorkload.pdf) |
| S. Qi, B. Tong, J. Hu, H. Lin, Y. Pang, W. Yuan, et al. The LDBC Financial Benchmark: Transaction Workload. PVLDB, 2025. | 论文 | [来源](https://www.vldb.org/pvldb/vol18/p4021-wu.pdf) | 金融场景图事务负载（转账、账户查询、风控路径） | [`VLDB2025-TheLDBCFinancialBenchmarkTransactionWorkload.pdf`](papers/Graph/VLDB2025-TheLDBCFinancialBenchmarkTransactionWorkload.pdf) |
| A. Iosup, A. Brandt, M. Schubert, T. Magr, M. Kayed. The LDBC Graphalytics Benchmark. arXiv, 2020. | 论文 | [来源](https://arxiv.org/abs/2011.15028) | Graphalytics 业务洞察负载（PageRank、三角计数、路径查找等） | [`arXiv2020-TheLDBCGraphalyticsBenchmark.pdf`](papers/Graph/arXiv2020-TheLDBCGraphalyticsBenchmark.pdf) |
| The LDBC Financial Benchmark (version 0.1.0). arXiv, 2023. | 论文 | [来源](https://arxiv.org/abs/2306.15975) | 金融图基准规范（版本 0.1.0） | [`arXiv2023-TheLDBCFinancialBenchmarkversion010.pdf`](papers/Graph/arXiv2023-TheLDBCFinancialBenchmarkversion010.pdf) |

**基准套件 / 数据集 / 仓库 / 文档 / 网站**

| 名称 | 类型 | 正式名称 | 简称 | 首次发布 | 许可证 | 来源链接 | 适用工作负载 |
| --- | --- | --- | --- | ---: | --- | --- | --- |
| LDBC Financial Benchmark Specification | 技术文档/规范 | The Specification of the LDBC Financial Benchmark | LDBC FinBench | 2023 | 见仓库 LICENSE | [入口](https://github.com/ldbc/ldbc_finbench_docs) | 金融图事务负载（转账、账户、风控路径） |
| LDBC Social Network Benchmark (SNB) — Business Intelligence Workload | 技术文档/规范 | LDBC Social Network Benchmark, Business Intelligence Workload Specification | LDBC-SNB BI | 2018 | CC BY-SA 4.0（规范） | [入口](https://ldbcouncil.org/benchmarks/snb/) [仓库](https://github.com/ldbc/ldbc-snb) | 13 条 BI 分析查询（PageRank、连通分量、社区检测等） |
| LDBC Social Network Benchmark (SNB) — Interactive Workload | 技术文档/规范 | LDBC Social Network Benchmark, Interactive Workload Specification | LDBC-SNB Interactive | 2012 | CC BY-SA 4.0（规范） | [入口](https://ldbcouncil.org/benchmarks/snb/) [仓库](https://github.com/ldbc/ldbc-snb) | 25 条交互式图查询（1-3 跳、边/点度数、连通分量等） |
| GraphScope | 开源仓库 | GraphScope: A Scalable Graph Computing Platform | GraphScope | 2020 | Apache-2.0 | [入口](https://github.com/alibaba/GraphScope) | LDBC-SNB Interactive / BI / Graphalytics |
| LDBC Graphalytics Driver | 开源仓库 | LDBC Graphalytics Generic Driver | ldbc_graphalytics | 2020 | Apache-2.0 | [入口](https://github.com/ldbc/ldbc_graphalytics) | Graphalytics 12 条分析查询 |
| LDBC SNB Data Generator (Spark) | 开源仓库 | LDBC Social Network Benchmark Data Generator (Spark implementation) | ldbc_snb_datagen_spark | 2018 | Apache-2.0 | [入口](https://github.com/ldbc/ldbc_snb_datagen_spark) | SNB 数据生成（scale factor 1-1000） |
| LDBC SNB Interactive Leaderboard | 网站/排行榜 | LDBC SNB Interactive Results | — | 2012 | — | [入口](https://ldbcouncil.org/benchmarks/snb/) | SNB Interactive 各系统查询吞吐率对比 |
| LDBC — Linked Data Benchmark Council | 网站/排行榜 | Linked Data Benchmark Council | LDBC | 2012 | 组织站点 | [入口](https://ldbcouncil.org/benchmarks/) | SNB / Graphalytics / Financial / BI 等图基准 |

### Vector

向量检索基准关注召回率、QPS 与单位成本，常用公开嵌入数据集（SIFT / GIST / Cohere）在统一硬件下横向比较。

**论文**

| 引用 | 类型 | 来源 | 适用工作负载 | 本地文件 |
| --- | --- | --- | --- | --- |
| ANN-Benchmarks: A Benchmarking Tool for Approximate Nearest Neighbor Algorithms. arXiv, 2018. | 论文 | [来源](https://arxiv.org/abs/1807.05614) | SIFT / GIST / MNIST / Fashion-MNIST 上的召回率-时延曲线 | [`AnnBenchmarks-ABenchmarkingToolForApproximateNearestNeighborAlgorithms.pdf`](papers/Vector/AnnBenchmarks-ABenchmarkingToolForApproximateNearestNeighborAlgorithms.pdf) |

**基准套件 / 数据集 / 仓库 / 文档 / 网站**

| 名称 | 类型 | 正式名称 | 简称 | 首次发布 | 许可证 | 来源链接 | 适用工作负载 |
| --- | --- | --- | --- | ---: | --- | --- | --- |
| VectorDBBench Public Datasets | 数据集 | SIFT / GIST / Cohere / OpenAI Embedding Datasets | — | 2023 | SIFT: Stanford 学术使用；Cohere: 见各自条款 | [入口](https://github.com/zilliztech/VectorDBBench/tree/master/vectordb_bench/backend/dataset) [仓库](https://github.com/zilliztech/VectorDBBench) | 768/1536 维向量检索；50K / 1M 规模 |
| VectorDBBench | 开源仓库 | VectorDBBench: A Benchmark Tool for VectorDB | VectorDBBench | 2023 | MIT | [入口](https://github.com/zilliztech/VectorDBBench) | 插入、搜索、带标量过滤的搜索；数据集 SIFT / GIST / Cohere / OpenAI |
| ann-benchmarks | 开源仓库 | ANN-Benchmarks: A Benchmarking Tool for Approximate Nearest Neighbor Algorithms | ann-benchmarks | 2018 | MIT | [入口](https://arxiv.org/abs/1807.05614) [仓库](https://github.com/erikbern/ann-benchmarks) | SIFT / GIST / MNIST / Fashion-MNIST 等数据集上的 ANN 召回率-时延曲线 |
| VectorDBBench Leaderboard (Zilliz Cloud) | 网站/排行榜 | Vector Search Performance Leaderboard | — | 2023 | — | [入口](https://zilliz.com/benchmark) | QPS / QP$ / Latency 三类指标，含 Cloud Leaderboard 案例 |

### Time-Series

时序数据库基准源自监控场景，强调乱序写入、范围扫描、降采样聚合与高基数标签过滤。

**论文**

| 引用 | 类型 | 来源 | 适用工作负载 | 本地文件 |
| --- | --- | --- | --- | --- |
| TSM-Bench: Benchmarking Time Series Database Systems for Monitoring Applications. PVLDB, 2023. | 论文 | [来源](https://www.vldb.org/pvldb/vol16/p3363-khelifati.pdf) | 时序写入、范围扫描、降采样聚合、乱序写入等监控场景负载 | [`VLDB2023-TSMBenchBenchmarkingTimeSeriesDatabaseSystemsforMonitoringApplications.pdf`](papers/Time-Series/VLDB2023-TSMBenchBenchmarkingTimeSeriesDatabaseSystemsforMonitoringApplications.pdf) |

**基准套件 / 数据集 / 仓库 / 文档 / 网站**

| 名称 | 类型 | 正式名称 | 简称 | 首次发布 | 许可证 | 来源链接 | 适用工作负载 |
| --- | --- | --- | --- | ---: | --- | --- | --- |
| TSM-Bench | 开源仓库 | TSM-Bench Benchmark Suite and Leaderboard | TSM-Bench | 2025 | Apache-2.0 | [入口](https://github.com/AlibabaTimeSeries/TSM-Bench) ⚠ | TSM-Bench 全部 case；含公开排行榜 |

### Document

文档型数据库基准多由关系型负载改写而来（如 TPC-C 改写为多文档事务），关注文档模型下的事务与索引代价。

**论文**

| 引用 | 类型 | 来源 | 适用工作负载 | 本地文件 |
| --- | --- | --- | --- | --- |
| J. Baum. Quantitative Performance Evaluation of Cloud-Based MySQL (Relational) Vs. MongoDB (NoSQL) Database with YCSB. Technical Report, 2019. | 论文 | [来源](https://opus4.kobv.de/frontdoor/index/index/docId/44585/file/Thesis_Master_Johannes_Baum.pdf) | YCSB 工作负载在 MySQL 与 MongoDB 上的对比 | [`MasterThesis2019-QuantitativePerformanceEvaluationofCloudBasedMySQLRelationalVsMongoDBNoSQLDatabasewithYCSB.pdf`](papers/Document/MasterThesis2019-QuantitativePerformanceEvaluationofCloudBasedMySQLRelationalVsMongoDBNoSQLDatabasewithYCSB.pdf) |
| A. Kamsky. Adapting TPC-C Benchmark to Measure Performance of Multi-Document Transactions in MongoDB. PVLDB, 2019. | 论文 | [来源](https://www.vldb.org/pvldb/vol12/p1839-schultz.pdf) | TPC-C 交易改写为多文档事务 | [`VLDB2019-AdaptingTPCCBenchmarktoMeasurePerformanceofMultiDocumentTransactionsinMongoDB.pdf`](papers/Document/VLDB2019-AdaptingTPCCBenchmarktoMeasurePerformanceofMultiDocumentTransactionsinMongoDB.pdf) |

### General

跨类型的通用基准框架与评测方法学研究，涵盖评测公平性、负载生成方法与 LLM 驱动的自动化基准构建。

**论文**

| 引用 | 类型 | 来源 | 适用工作负载 | 本地文件 |
| --- | --- | --- | --- | --- |
| C. Curino, D. E. Difallah, A. Pavlo, P. Cudre-Mauroux. Benchmarking OLTP/Web Databases in the Cloud: The OLTP-Bench Framework. CloudDB, 2012. | 论文 | — | OLTP-Bench 负载模板；面向 Web 事务型数据库的云端评测 | [`CloudDB2012-BenchmarkingOLTPWebDatabasesintheCloudTheOLTPBenchFramework.pdf`](papers/General/CloudDB2012-BenchmarkingOLTPWebDatabasesintheCloudTheOLTPBenchFramework.pdf) |
| C. Brücke, P. Härtling, R. D. Escobar Palacios, H. Patel. TPCx-AI - An Industry Standard Benchmark for Artificial Intelligence and Machine Learning Systems. PVLDB, 2023. | 论文 | — | TPCx-AI 训练与推理场景（14 个用例） | [`VLDB2023-TPCxAIAnIndustryStandardBenchmarkforArtificialIntelligenceandMachineLearningSystems.pdf`](papers/General/VLDB2023-TPCxAIAnIndustryStandardBenchmarkforArtificialIntelligenceandMachineLearningSystems.pdf) |
| I. Tolovski, P. Hildebrandt, K. Daudjee. TPCx-AI under the Microscope: A Benchmarking Debt Analysis. PVLDB, 2026. | 论文 | [来源](https://www.vldb.org/pvldb/vol19/) | 对 TPCx-AI 基准本身的可比性债务分析 | [`VLDB2026-TPCxAIUndertheMicroscopeaBenchmarkingDebtAnalysis.pdf`](papers/General/VLDB2026-TPCxAIUndertheMicroscopeaBenchmarkingDebtAnalysis.pdf) |

**基准套件 / 数据集 / 仓库 / 文档 / 网站**

| 名称 | 类型 | 正式名称 | 简称 | 首次发布 | 许可证 | 来源链接 | 适用工作负载 |
| --- | --- | --- | --- | ---: | --- | --- | --- |
| SysBench Manual | 技术文档/规范 | SysBench Manual | SysBench | 2020 | MIT | [入口](https://github.com/pyxll/jujube-bench) ⚠ | SysBench 全部驱动 |
| NeurBench | 开源仓库 | NeurBench: Benchmark Suite for Learned Database Components | NeurBench | 2026 | 见仓库 | [入口](https://github.com/neurdb/neurbench) | 学习型基数估计与学习索引；含数据漂移场景 |
| SQLStorm | 开源仓库 | SQLStorm: Taking Database Benchmarking into the LLM Era | SQLStorm | 2026 | 见仓库 | [入口](https://github.com/SQL-Storm/SQLStorm) | LLM 驱动的自动化负载生成 |
| SysBench | 开源仓库 | SysBench: An Extended Framework for Evaluating Database System Performance | SysBench | 2020 | MIT | [入口](https://github.com/pyxll/jujube-bench) ⚠ | 通用数据库负载；支持 TPC-C / TPC-H / YCSB 等多种驱动 |
| SPEC Benchmarks | 网站/排行榜 | SPEC Benchmarks | SPEC | 1988 | 部分免费、部分需会员 | [入口](https://www.spec.org/benchmarks/) | SPEC CPU / POWER / SPC；历史上的 SPECj 数据库基准 |
| SPEC — Standard Performance Evaluation Corporation | 网站/排行榜 | SPEC Benchmarks | SPEC | 1988 | 部分免费，部分需会员 | [入口](https://www.spec.org/benchmarks.htm) ⚠ | SPEC CPU / POWER / SPC 等；SPECj 系列数据库基准（历史） |
| TPC — Transaction Processing Council | 网站/排行榜 | Transaction Processing Council | TPC | 1984 | 组织站点 | [入口](https://www.tpc.org/) | TPC-C / TPC-H / TPC-D / TPCx-AI 等全部规范与结果 |

## 下载过程与未能获取的资源

全部下载均设三次重试上限。下表逐条记录 18 项资源的尝试来源与最终结果：12 项经更换来源后获取，2 项因出版方版权墙仅收录条目与官方仓库地址，4 项确实无法获取。

| 资源 | 尝试的来源与结果 | 最终状态 |
| --- | --- | --- |
| YCSB 原始论文（SoCC 2010） | https://www.usenix.org/legacy/events/fast10/tech/full_papers/Bernstein.pdf — HTTP 404 — 该地址不对应 YCSB 论文（USENIX FAST 2010 未收录）<br>https://www.cs.duke.edu/courses/fall13/compsci590.4/838-CloudPapers/ycsb.pdf — 成功 — Duke 课程镜像，内容与标题一致 | 已获取 |
| TSM-Bench（VLDB） | https://www.vldb.org/pvldb/vol18/p4015-wang.pdf — 返回 HTML 而非 PDF — 卷号与页码猜测错误<br>https://www.vldb.org/pvldb/vol16/p3363-khelifati.pdf — 成功 — 由 PVLDB 索引取得真实地址 | 已获取 |
| M2Bench（VLDB） | https://www.vldb.org/pvldb/vol16/p3612-huang.pdf — 返回 HTML 而非 PDF — 卷号与页码猜测错误<br>https://www.vldb.org/pvldb/vol16/p747-moon.pdf — 成功 — 由 PVLDB 索引取得真实地址 | 已获取 |
| Dike（SIGMOD 2023） | https://dl.acm.org/doi/pdf/10.1145/3581784.3607068 — HTTP 403 — ACM Digital Library 版权墙<br>https://github.com/DBHammer/Dike — 已收录官方仓库地址 | 仅收录条目（原文见官方仓库） |
| TACO（VLDB） | https://www.vldb.org/pvldb/vol18/p4036-wang.pdf — 返回 HTML 而非 PDF — 卷号与页码猜测错误<br>https://github.com/DEEP-PolyU/TACO — 已收录官方仓库地址 | 仅收录条目（原文见官方仓库） |
| SemBench（VLDB） | https://www.vldb.org/pvldb/vol17/p3485-yuan.pdf — 返回 HTML 而非 PDF — 卷号与页码猜测错误<br>https://www.vldb.org/pvldb/vol19/p1754-trummer.pdf — 成功 — 由 PVLDB 索引取得真实地址 | 已获取 |
| Vodka（VLDB） | https://www.vldb.org/pvldb/vol18/p4022-wang.pdf — 返回 HTML 而非 PDF — 卷号与页码猜测错误<br>https://www.vldb.org/pvldb/vol19/p481-hu.pdf — 成功 — 由 PVLDB 索引取得真实地址 | 已获取 |
| PolarFS（VLDB 2018） | https://www.vldb.org/pvldb/vol11/p2206-cao.pdf — 返回 HTML 而非 PDF — 卷号与页码猜测错误<br>https://vldb.org/pvldb/vol11/p1849-cao.pdf — 成功 — 由 PVLDB 索引取得真实地址 | 已获取 |
| LevelDB（USENIX ATC 2011） | https://www.usenix.org/legacy/events/atc11/tech/full_papers/Dean.pdf — HTTP 404 — USENIX 旧站目录已调整<br>https://www.usenix.org/legacy/events/fast11/tech/full_papers/Dean.pdf — HTTP 404<br>arXiv 标题检索 "LevelDB: A Read-Write Friendly Key-Value Store" — 无命中 — 该文发表于 USENIX，未在 arXiv 收录 | 未获取 |
| BigANN（arXiv 2021） | https://arxiv.org/pdf/2107.07874 — 下载成功但内容为无关论文（该 arXiv ID 实际是偏微分方程论文）—— 文件已删除<br>arXiv API 标题检索 "BigANN: Billion-scale Approximate Nearest Neighbor Search" — 无命中 — 论文不在 arXiv 收录范围 | 未获取 |
| ANN 基准综述（arXiv） | https://arxiv.org/pdf/1908.10096 — 下载成功但内容为无关论文（该 ID 实际是自旋扩散模型论文）—— 文件已删除<br>arXiv API 标题检索 "Benchmarks for Approximate Nearest Neighbor Search" — 无命中 — 该文发表于 ICDCS，未在 arXiv 收录 | 未获取 |
| BigANN 基准数据集论文 | arXiv API 标题检索 "The BigANN Benchmark: Datasets and Evaluation" — 无命中 — 论文以数据集形式发布于官方站点 | 未获取 |
| GPU 标量函数加速评测（VLDB 2026） | https://www.vldb.org/pvldb/vol18/p3992-zhao.pdf — 卷号猜测错误<br>PDF 内页核实作者与标题后，从本地论文库获取同名条目 — 成功 | 已获取 |
| DBTest 2026 系列（4 篇） | https://dbtest.cs.umb.edu/ — 本机网络不可达（Tunnel connection failed）<br>本地论文库 D:/git-papers/DBTest/ — 成功 — 4 篇全部命中 | 已获取 |
| Fair Benchmarking Considered Difficult（DBTest） | https://dbtest.cs.umb.edu/ — 本机网络不可达<br>本地论文库 D:/git-papers/DBTest/ — 成功 | 已获取 |
| NeurBench（SIGMOD 2026） | https://dl.acm.org/doi/10.1145/3744027 — HTTP 403 — ACM 版权墙<br>本地论文库 D:/git-papers/SIGMOD/ — 成功 | 已获取 |
| 性能基准化 KV 存储评测（TR 2014） | https://www.researchgate.net/publication/269347728_... — ResearchGate 反爬，本机不可达<br>本地论文库 D:/git-papers/TR/ — 成功 | 已获取 |
| OLTP-Bench（VLDB 2014） | https://www.usenix.org/conference/fast13/technical-sessions/presentation/nyomo — HTTP 404 — 该路径非论文地址<br>https://vldb.org/pvldb/vol7/p277-difallah.pdf — 成功 — 由 PVLDB 索引取得真实地址 | 已获取 |

### 确实未能获取的资源

| 资源 | 失败原因 | 替代获取途径 |
| --- | --- | --- |
| LevelDB（USENIX ATC 2011） | 无命中 — 该文发表于 USENIX，未在 arXiv 收录 | 论文主页 https://github.com/google/leveldb（README 内含 db_bench 性能报告）；USENIX ATC '11 论文集 |
| BigANN（arXiv 2021） | 无命中 — 论文不在 arXiv 收录范围 | 论文以数据集与代码形式发布于 https://github.com/TencentBigANN/ ；可参考 GitHub 仓库中的评测说明 |
| ANN 基准综述（arXiv） | 无命中 — 该文发表于 ICDCS，未在 arXiv 收录 | 论文发表于 ICDCS 2019；可经 IEEE Xplore 或作者主页获取 |
| BigANN 基准数据集论文 | 无命中 — 论文以数据集形式发布于官方站点 | 数据集与评测工具见 https://github.com/TencentBigANN/ |

**未收录说明**

- 本地论文库 7,540 个 PDF 中另有约 1,400 个标题含 benchmark/throughput/scalability 等词的文件，经逐条判定后排除：绝大多数属于编译器基准、形式化验证、共识协议、图算法或机器学习基准，与数据库系统评测无关。
- 出版方付费墙导致的部分 ACM/Springer/IEEE 论文未直接下载，但其规范文本、公开预印本或官方仓库地址均已收录，可据此获取原文。
- 本清单中每篇论文的标题均与 PDF 首页内容逐条比对过；凡因地址猜测错误而下载到无关论文的文件，一并已删除并重新检索。
