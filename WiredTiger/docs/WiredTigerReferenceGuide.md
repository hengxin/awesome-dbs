# WiredTiger: Reference Guide

- 来源: http://source.wiredtiger.com/develop/index.html
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

[](http://wiredtiger.com/)
Version 12.0.0
[Fork me on GitHub](https://github.com/wiredtiger/wiredtiger)
[Join my user group](http://groups.google.com/group/wiredtiger-users)
Reference Guide
WiredTiger is a production quality, high performance, scalable, NoSQL, Open Source extensible platform for data management. WiredTiger is developed and maintained by MongoDB, Inc., where it is the principal database storage engine.
WiredTiger supports row-oriented storage (where all columns of a row are stored together), and column-oriented storage (where columns are stored in groups, allowing for more efficient access and storage of column subsets).
WiredTiger includes ACID transactions with standard isolation levels and durability at both checkpoint and commit-level granularity.
WiredTiger can be used as a simple key/value store, but also has a complete schema layer, including indices and projections.
WiredTiger should be generally portable to any 64-bit system supporting the ANSI C11 and POSIX 1003.1 standards.
For more information on the WiredTiger architecture and why it might be right for your project, see:
- [WiredTiger Overview and Features](overview.html)
For more information about building and installing WiredTiger, see:
- [General information on portability](portability.html)
- [Building and installing WiredTiger on POSIX (Linux, *BSD, OS X):](build-posix.html)
- [Building and installing WiredTiger on Windows](build-windows.html)
For more information about writing WiredTiger applications, see:
- [Writing WiredTiger applications](programming.html)
- [WiredTiger API reference manual](group__wt.html)
For more information about administrating WiredTiger databases, see:
- [WiredTiger command line utility](command_line.html)
- [Managing WiredTiger databases](admin.html)
For release upgrading information, see:
- [Upgrading WiredTiger applications](upgrading.html)
WiredTiger is distributed under Open Source licenses; for more information, see:
- [WiredTiger licensing](license.html)
For more information on tools and techniques used during WiredTiger development, see:
- [Tools and Techniques](tool-index.html)
For more information about the architecture and internals of WiredTiger, see:
- [WiredTiger Architecture Guide](arch-index.html)
To browse the WiredTiger source code repository or contact us, see:
- [WiredTiger community and contact information](community.html)
- Copyright (c) 2008-present MongoDB, Inc. All rights reserved. Contact [info@wiredtiger.com](mailto:info@wiredtiger.com) for more information.