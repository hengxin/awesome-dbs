# PostgreSQL: Documentation: 18: 13.1. Introduction

- 来源: https://www.postgresql.org/docs/current/mvcc-intro.html
- 归档时间: 2026-10-29
- 说明: 官方技术白皮书 / 架构文档的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

[](/)
- [Home](/)
- [About](/about/)
- [Download](/download/)
- [Documentation](/docs/)
- [Community](/community/)
- [Developers](/developer/)
- [Support](/support/)
- [Donate](/about/donate/)
- [Your account](/account/)
October 15, 2026: [PostgreSQL 19 RC 1 Released!](/about/news/postgresql-19-rc-1-released-3409/)
[Documentation](/docs/) → [PostgreSQL 18](/docs/18/index.html)
Supported Versions:
[Current](/docs/current/mvcc-intro.html)
([18](/docs/18/mvcc-intro.html))
/
[17](/docs/17/mvcc-intro.html)
/
[16](/docs/16/mvcc-intro.html)
/
[15](/docs/15/mvcc-intro.html)
/
[14](/docs/14/mvcc-intro.html)
Development Versions:
[19](/docs/19/mvcc-intro.html)
/
[devel](/docs/devel/mvcc-intro.html)
Unsupported versions:
[13](/docs/13/mvcc-intro.html)
/
[12](/docs/12/mvcc-intro.html)
/
[11](/docs/11/mvcc-intro.html)
/
[10](/docs/10/mvcc-intro.html)
/
[9.6](/docs/9.6/mvcc-intro.html)
/
[9.5](/docs/9.5/mvcc-intro.html)
/
[9.4](/docs/9.4/mvcc-intro.html)
/
[9.3](/docs/9.3/mvcc-intro.html)
/
[9.2](/docs/9.2/mvcc-intro.html)
/
[9.1](/docs/9.1/mvcc-intro.html)
/
[9.0](/docs/9.0/mvcc-intro.html)
/
[8.4](/docs/8.4/mvcc-intro.html)
/
[8.3](/docs/8.3/mvcc-intro.html)
/
[8.2](/docs/8.2/mvcc-intro.html)
13.1. Introduction
[Prev](mvcc.html)
[Up](mvcc.html)
Chapter 13. Concurrency Control
[Home](index.html)
[Next](transaction-iso.html)
## 13.1. Introduction [#](#MVCC-INTRO)
PostgreSQL provides a rich set of tools for developers to manage concurrent access to data. Internally, data consistency is maintained by using a multiversion model (Multiversion Concurrency Control, MVCC ). This means that each SQL statement sees a snapshot of data (a database version ) as it was some time ago, regardless of the current state of the underlying data. This prevents statements from viewing inconsistent data produced by concurrent transactions performing updates on the same data rows, providing transaction isolation for each database session. MVCC , by eschewing the locking methodologies of traditional database systems, minimizes lock contention in order to allow for reasonable performance in multiuser environments.
The main advantage of using the MVCC model of concurrency control rather than locking is that in MVCC locks acquired for querying (reading) data do not conflict with locks acquired for writing data, and so reading never blocks writing and writing never blocks reading. PostgreSQL maintains this guarantee even when providing the strictest level of transaction isolation through the use of an innovative Serializable Snapshot Isolation ( SSI ) level.
Table- and row-level locking facilities are also available in PostgreSQL for applications which don't generally need full transaction isolation and prefer to explicitly manage particular points of conflict. However, proper use of MVCC will generally provide better performance than locks. In addition, application-defined advisory locks provide a mechanism for acquiring locks that are not tied to a single transaction.
[Prev](mvcc.html)
[Up](mvcc.html)
[Next](transaction-iso.html)
Chapter 13. Concurrency Control
[Home](index.html)
13.2. Transaction Isolation
## Submit correction
If you see anything in the documentation that is not correct, does not match
your experience with the particular feature or requires further clarification,
please use
[this form](/account/comments/new/18/mvcc-intro.html/)
to report a documentation issue.
[Policies](/about/policies/) |
[Code of Conduct](/about/policies/coc/) |
[About PostgreSQL](/about/) |
[Contact](/about/contact/)
Copyright © 1996-2026 The PostgreSQL Global Development Group