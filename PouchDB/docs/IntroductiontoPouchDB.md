# Introduction to PouchDB

- 来源: https://pouchdb.com/guides
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

[GitHub](https://github.com/apache/pouchdb)
[PouchDB](/)
-
[Blog](/blog/)
-
[Guides](/guides/)
-
[API](/api.html)
-
[Learn](/learn.html)
-
[Download v9.0.0](/download.html)
# Introduction to PouchDB
[](https://github.com/apache/pouchdb/edit/master/docs/_guides/index.md)
-
[Intro](/guides/)
-
[Setting up CouchDB](/guides/setup-couchdb.html)
-
[Setting up PouchDB](/guides/setup-pouchdb.html)
-
[Working with databases](/guides/databases.html)
-
[Working with documents](/guides/documents.html)
-
[Asynchronous code](/guides/async-code.html)
-
[Updating/deleting documents](/guides/updating-deleting.html)
-
[Bulk operations](/guides/bulk-operations.html)
-
[Working with attachments](/guides/attachments.html)
-
[Replication](/guides/replication.html)
-
[Conflicts](/guides/conflicts.html)
-
[Changes feed](/guides/changes.html)
-
[Mango queries](/guides/mango-queries.html)
-
[Map/reduce queries](/guides/queries.html)
-
[Compacting and destroying](/guides/compact-and-destroy.html)
-
[Local documents](/guides/local-documents.html)
Welcome to the PouchDB guide! Consider this your starting point for anything and everything related to the world of PouchDB and CouchDB.
For a quicker TodoMVC-based tutorial, you can also check out the ["Getting Started" guide](/getting-started.html).
Feel free to skip ahead using the sidebar at any time.
[What is PouchDB?](#what-is-pouchdb)
PouchDB is a JavaScript implementation of [CouchDB](https://couchdb.apache.org). Its goal is to emulate the CouchDB API with near-perfect fidelity, while running in the browser or in Node.js.
[What is CouchDB?](#what-is-couchdb)
CouchDB is a NoSQL database created in 2005 by Damien Katz, and now maintained by the Apache Software Foundation. If you are a JavaScript developer, you probably use CouchDB every day, because it's the core technology that powers [npm](https://www.npmjs.org/).
[Couchbase, CouchDB, Couch-what?](#couchbase-couchdb-couch-what)
Today there are two major database companies that
can trace their lineage back to CouchDB: [Couchbase](http://couchbase.com) and [Cloudant](http://cloudant.com). Both of them are separate products compared to CouchDB.
However, all three of these databases share the same CouchDB sync protocol . This means that PouchDB can sync with either one of them, and you can always swap out one database for another. You're never locked in.
In a sense, these databases are like competing phone companies, and the CouchDB sync protocol is the underlying telephony infrastructure.
[CouchDB's one-two punch: HTTP and sync](#http-and-sync)
With so many SQL and NoSQL databases out there – MongoDB, PostgreSQL, MySQL, etc. – you may wonder why we chose to implement CouchDB instead of the others.
We have two very good answers to that question: HTTP and sync .
[HTTP: the little protocol that could](#http)
When working with databases, we're often accustomed to writing some kind of conversion layer between the database and our client-side applications. This means, however, that we are just translating database queries into RESTful HTTP calls, over and over. For every app we write.
CouchDB throws this out the window by daring us to talk to the database directly, from our client-side apps. And it does so by using HTTP as its primary means of communication. No special protocol, no special drivers: just REST and HTTP. You can communicate with CouchDB entirely through your browser, curl , or a REST client like [Postman](https://chrome.google.com/webstore/detail/postman-rest-client/fdmmgilgnpjigdojojpjoooidkmcomcm).
In this way, CouchDB truly is a "database for the web."
[Sync: CouchDB's killer feature](#sync)
Another unique feature of CouchDB is that it was designed from the bottom-up to enable easy synchronization between different databases.
For example, if you are worried about latency in your client-side applications, you can simply set up one CouchDB in Europe, another in North America, and another in Asia. After enabling continuous two-way replication between these databases, your clients can simply talk to whichever one is closer.
PouchDB takes this one step further by putting the database inside your browser.
[Next](#next)
Now that you understand the basics of the PouchDB/CouchDB universe, let's set up CouchDB!
-
[Setting up CouchDB →](/guides/setup-couchdb.html)
[](https://bsky.app/profile/pouchdb.bsky.social)
[](https://fosstodon.org/@pouchdb)
[](https://github.com/rvagg/node-levelup)
[](https://github.com/apache/pouchdb)
[](http://couchdb.apache.org/)
### Learn
- [Getting Started](/getting-started.html)
- [API Guide](/api.html)
- [Wiki](https://github.com/apache/pouchdb/wiki)
### Discuss
- [Bluesky](https://bsky.app/profile/pouchdb.bsky.social)
- [Mastodon](https://fosstodon.org/@pouchdb)
- [GitHub Discussions](https://github.com/apache/pouchdb/discussions)
- [Slack](https://join.slack.com/t/couchdb/shared_invite/zt-3aqucllea-C92fkzW5oO_VhllRCqFbcw)
- [StackOverflow](http://stackoverflow.com/questions/tagged/pouchdb)
### Contribute
- [Contributing](https://github.com/apache/pouchdb/blob/master/CONTRIBUTING.md)
- [Source](https://github.com/apache/pouchdb)
- [Issues](https://github.com/apache/pouchdb/issues)
- [Apache License](https://github.com/apache/pouchdb/blob/master/LICENSE)
- [Dev Mailing List](https://lists.apache.org/list.html?dev@pouchdb.apache.org)
Content updated, reload now? ↻