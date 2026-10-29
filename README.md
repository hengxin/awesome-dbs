# awesome-dbs

A List of Awesome Database Systems

## 数据库索引

**[DATABASE-INDEX.md](DATABASE-INDEX.md)** — 全部数据库的统一表格索引，包含名称、官方链接、GitHub 仓库、数据库类型（可多选）、所属机构、许可证、首次发布年份，以及每个数据库已收录的论文与官方文档清单。

每个数据库一个子目录，内含该库的资料：

```
<数据库名>/
├── README.md        # 描述、官网、文档、GitHub、已收录资料清单
├── papers/          # 学术论文（VLDB2025-PaperTitle.pdf 格式）
├── whitepapers/     # 官方技术白皮书 / 架构文档
└── docs/            # 其它官方文档
```

命名规范：

- 论文：`<会议><年份>-<标题>`，如 `VLDB2025-LightningFastIndexing.pdf`
- 官方技术白皮书：`<年份>-<标题>`，如 `2018-RedisDataTypesandArchitecture.pdf`
- 标题去除全部标点与空格，保留原有大小写

## 数据来源

- [DB-Engines Ranking](https://db-engines.com/en/ranking)
	- [DB-Engines Ranking - Trend Popularity](https://db-engines.com/en/ranking_trend)
	- [DB-Engines Ranking - Trend of Key-value Stores Popularity](https://db-engines.com/en/ranking_trend/key-value+store)
	- [DB-Engines Ranking - Trend of Document Stores Popularity](https://db-engines.com/en/ranking_trend/document+store)

- [Database of Databases](https://dbdb.io/)

## 目录说明

| 目录 | 内容 |
| --- | --- |
| [Overview](Overview/) | 入门推荐与选型导引 |
| [Academic](Academic/) | 综述、课程与研究方法类资料 |
| [Conferences-Journals](Conferences-Journals/) | 相关会议与期刊 |
| [DB-Papers](DB-Papers/) | 跨数据库的通用论文 |
| [DB-Books](DB-Books/) | 书籍与早期白皮书 |
| [DB-Benchs](DB-Benchs/) | 基准测试报告 |
| [DB-Logos](DB-Logos/) | 各数据库 Logo |
| [数据库发展研究报告](数据库发展研究报告/) | 28 份数据库技术发展研究报告（信通院年度系列、Gartner/IDC 市场报告、学术综述），含[索引文档](数据库发展研究报告/数据库研究报告索引.md) |
| `Benchmarking/` | 基准测试工具与规范（TPC、LDBC 等） |

## 资料来源可追溯

每个下载的文件都在对应目录的 README 表格中给出原始来源链接；因链接失效或站点拒绝访问而未能获取的资料，会在 [DATABASE-INDEX.md](DATABASE-INDEX.md) 的「未能获取的资料」一节中逐条列出，不以任何方式补写不存在的内容。
