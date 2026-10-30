# Database Benchmarking

数据库性能评测相关的论文、基准套件、数据集、评测网站、开源仓库与技术文档。

**[BENCHMARKING-INDEX.md](BENCHMARKING-INDEX.md)** 是本目录的主清单，按数据库类型（Key-Value、SQL/关系型、NewSQL、Analytical/OLAP、Graph、Vector、时序、文档型、通用）分节整理，每条记录给出类型、来源链接、所属类别与适用的评测工作负载，并附汇总统计表与下载失败记录。

## 目录结构

```
Benchmarking/
├── BENCHMARKING-INDEX.md    # 结构化清单（主文档）
├── papers/<数据库类别>/       # 论文 PDF
├── SysBench Manual (Alexey Kopytov).pdf
├── TPC-C (v5.11.0).pdf
└── TPC-E (v1.14.0).pdf
```

论文文件命名：`<会议><年份>-<标题去标点与空格>.pdf`，例如
`VLDB2023-M2BenchADatabaseBenchmarkforMultiModelAnalyticWorkloads.pdf`。
白皮书与规范文档用 `<年份>-<标题>.pdf`。

## 资料来源

论文优先取自本地论文库 `D:\git-papers\`（7,540 个 PDF，按会议/期刊分目录），
本地缺失者再从 arXiv、PVLDB 官方站点、作者课程主页与 GitHub 检索获取。

所有下载设三次重试上限，仍无法获取的资源在清单末尾逐条列出失败原因、
已尝试的来源与替代获取途径。

## 质量校验

- 每篇论文的标题均与 PDF 首页内容逐条比对，下载到无关论文的文件一律删除重取
- 所有 PDF 通过 `%PDF` 头 + `%%EOF` 尾校验
- 仓库地址经 GitHub API 核验存在性与描述后写入
- 论文引用串（作者、标题、会议、年份）取自论文首页，而非凭记忆填写
