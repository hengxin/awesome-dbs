# SQLite Documentation

- 来源: https://www.sqlite.org/docs.html
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

[](index.html)
Small. Fast. Reliable.
Choose any three.
- [Home](index.html)
- [Menu](javascript:void(0))
- [About](about.html)
- [Documentation](docs.html)
- [Download](download.html)
- [License](copyright.html)
- [Support](support.html)
- [Purchase](prosupport.html)
-
[Search](javascript:void(0))
- [About](about.html)
- [Documentation](docs.html)
- [Download](download.html)
- [Support](support.html)
- [Purchase](prosupport.html)
Search Documentation
Search Changelog
### Common Links
- [Features](features.html)
- [When to use SQLite](whentouse.html)
- [Getting Started](quickstart.html)
- [Try it live!
- SQL Syntax](https://sqlite.org/fiddle)
- [Pragmas](pragma.html#toc)
- [SQL functions](lang_corefunc.html)
- [Date & time functions](lang_datefunc.html)
- [Aggregate functions](lang_aggfunc.html#aggfunclist)
- [Window functions](windowfunctions.html#biwinfunc)
- [Math functions](lang_mathfunc.html)
- [JSON functions](json1.html)
- [C/C++ Interface Spec](c3ref/intro.html)
- [Introduction](cintro.html)
- [List of C-language APIs](c3ref/funclist.html)
- [The CLI (Command-Line Interface)](cli.html)
- [The TCL Interface Spec](tclsqlite.html)
- [Quirks and Gotchas](quirks.html)
- [Frequently Asked Questions](faq.html)
- [Commit History](https://www.sqlite.org/src/timeline)
- [Prior Releases](chronology.html)
- [Bugs](https://www.sqlite.org/src/wiki?name=Bug+Reports)
- [News](news.html)
## Documentation
Search Documentation
Search Changelog
- ▼ Document Lists And Indexes
- [Alphabetical Listing Of All Documents](doclist.html)
- [Website Keyword Index](keyword_index.html)
- [Permuted Title Index](sitemap.html)
- ► Overview Documents
- [About SQLite](about.html)
→
A high-level overview of what SQLite is and why you might be
interested in using it.
- [Appropriate Uses For SQLite](whentouse.html)
→
This document describes situations where SQLite is an appropriate
database engine to use versus situations where a client/server
database engine might be a better choice.
- [Distinctive Features](different.html)
→
This document enumerates and describes some of the features of
SQLite that make it different from other SQL database engines.
- [Quirks of SQLite](quirks.html)
→
This document is a short list of some unusual features of SQLite
that tend to cause misunderstandings and confusion. The list includes
both deliberate innovations and "misfeatures" that are retained only
for backwards compatibility.
- [How SQLite Is Tested](testing.html)
→
The reliability and robustness of SQLite is achieved in large part
by thorough and careful testing. This document identifies the
many tests that occur before every release of SQLite.
- [Copyright](copyright.html)
→
SQLite is in the public domain. This document describes what that means
and the implications for contributors.
- [Frequently Asked Questions](faq.html)
→
The title of the document says all...
- [Books About SQLite](books.html)
→
A list of independently written books about SQLite.
- ► Programming Interfaces
- [SQLite In 5 Minutes Or Less](quickstart.html)
→
A very quick introduction to programming with SQLite.
- [Introduction to the C/C++ API](cintro.html)
→
This document introduces the C/C++ API. Users should read this document
before the C/C++ API Reference Guide linked below.
- [How To Compile SQLite](howtocompile.html)
→
Instructions and hints for compiling SQLite C code and integrating
that code with your own application.
- [C/C++ API Reference](c3ref/intro.html)
→
This document describes each API function separately.
- [Result and Error Codes](rescode.html)
→
A description of the meanings of the numeric result codes
returned by various C/C++ interfaces.
- [Application-Defined SQL Function](appfunc.html)
→
An overview of the C-language interfaces used to create new
application-defined SQL functions in SQLite.
- [Tcl API](tclsqlite.html)
→
A description of the TCL interface bindings for SQLite.
- [SQLite Android Bindings](http://sqlite.org/android/)
→
Information on how to deploy your own private copy of SQLite on
Android, bypassing the built-in SQLite, but using the same Java
interface.
- [System.Data.SQLite](http://system.data.sqlite.org/)
→
C#/.NET bindings for SQLite
- ► SQL Language Documentation
- [SQL Syntax](lang.html)
→
This document describes the SQL language that is understood by
SQLite.
- [Pragma commands](pragma.html)
→
This document describes SQLite performance tuning options and other
special purpose database commands.
- [Core SQL Functions](lang_corefunc.html)
→
General-purpose built-in scalar SQL functions.
- [Aggregate SQL Functions](lang_aggfunc.html)
→
General-purpose built-in aggregate SQL functions.
- [Date and Time SQL Functions](lang_datefunc.html)
→
SQL functions for manipulating dates and times.
- [Window Functions](windowfunctions.html)
→
SQL Window functions.
- [Generated Columns](gencol.html)
→
Stored and virtual columns in table definitions.
- [DataTypes](datatype3.html)
→
SQLite version 3 introduces the concept of manifest typing, where the
type of a value is associated with the value itself, not the column that
it is stored in.
This page describes data typing for SQLite version 3 in further detail.
- [Indexes On Expressions](expridx.html)
→
Indexes in SQLite do not have to be over just plain table columns.
Expressions can also be indexed.
- [Row Values](rowvalue.html)
→
SQLite supports comparisons, including inequality comparisons, between
tuples of values, call "row values". This document explains.
- [STRICT Tables](stricttables.html)
→
A STRICT table in SQLite does rigid type enforcement, in order to more
closely mimic the behavior of other SQL database engines.
- ► Extensions
- [JSON Functions](json1.html)
→
SQL functions for creating, parsing, and querying JSON content.
- [FTS5 - Full Text Search](fts5.html)
→
A description of the SQLite Full Text Search (FTS5) extension.
- [FTS3 - Full Text Search](fts3.html)
→
A description of the SQLite Full Text Search (FTS3) extension.
- [R-Tree Module](rtree.html)
→
A description of the SQLite R-Tree extension. An R-Tree is a specialized
data structure that supports fast multi-dimensional range queries often
used in geospatial systems.
- [Sessions](sessionintro.html)
→
The Sessions extension allows change to an SQLite database to be
captured in a compact file which can be reverted on the original
database (to implement "undo") or transferred and applied to another
similar database.
- [Run-Time Loadable Extensions](loadext.html)
→
A general overview on how run-time loadable extensions work, how they
are compiled, and how developers can create their own run-time loadable
extensions for SQLite.
- [Dbstat Virtual Table](dbstat.html)
→
The DBSTAT virtual table reports on the sizes and geometries of tables
storing content in an SQLite database, and is the basis for the
[sqlite3_analyzer](sqlanalyze.html) utility program.
- [Csv Virtual Table](csv.html)
→
The CSV virtual table allows SQLite to directly read and query
[RFC 4180](https://www.ietf.org/rfc/rfc4180.txt) formatted files.
- [Carray](carray.html)
→
CARRAY is a [table-valued function](vtab.html#tabfunc2)
that allows C-language arrays to be used in SQL queries.
- [generate_series](series.html)
→
A description of the generate_series()
[table-valued function](vtab.html#tabfunc2).
- [Spellfix1](spellfix1.html)
→
The spellfix1 extension is an experiment in doing spelling correction
for [full-text search](fts3.html).
- [Zipfile](zipfile.html)
→
A [virtual table] with accompanying support functions that can
read and write a ZIP archive as if it were a database.
- [The IEEE754 Extension](floatingpoint.html#the_ieee754_c_extension)
→
A set of SQL functions for encoding and decoding IEEE-754 floating
point numbers.
- [The Decimal Extension](floatingpoint.html#the_decimal_c_extension)
→
A set of functions for doing arbitrary-precision decimal arithmetic,
including expanding IEEE-754 floating point values to their exact
decimal representation.
- [The UINT Collating Sequence](uintcseq.html)
→
A collating sequence that sorts text with embedded numbers in
numeric order.
- [The Percentile Extension](percentile.html)
→
An implementation of aggregate functions:
[median()](percentile.html#*medianfunc),
[percentile()](percentile.html#*percentilefunc),
[percentile_cont()](percentile.html#*percentilecontfunc), and
[percentile_disc()](percentile.html#*percentilediscfunc).
- ► Features
- [8+3 Filenames](shortnames.html)
→
How to make SQLite work on filesystems that only support
8+3 filenames.
- [Autoincrement](autoinc.html)
→
A description of the AUTOINCREMENT keyword in SQLite, what it does,
why it is sometimes useful, and why it should be avoided if not
strictly necessary.
- [Backup API](backup.html)
→
The [online-backup interface](c3ref/backup_finish.html) can be
used to copy content from a disk file into an in-memory database or vice
versa and it can make a hot backup of a live database. This application
note gives examples of how.
- [Error and Warning Log](errlog.html)
→
SQLite supports an "error and warning log" design to capture information
about suspicious and/or error events during operation. Embedded applications
are encouraged to enable the error and warning log to help with debugging
application problems that arise in the field. This document explains how
to do that.
- [Foreign Key Support](foreignkeys.html)
→
This document describes the support for foreign key constraints introduced
in version 3.6.19.
- [Indexes On Expressions](expridx.html)
→
Notes on how to create indexes on expressions instead of just
individual columns.
- [Internal versus External Blob Storage](intern-v-extern-blob.html)
→
Should you store large BLOBs directly in the database, or store them
in files and just record the filename in the database? This document
seeks to shed light on that question.
- [Limits In SQLite](limits.html)
→
This document describes limitations of SQLite (the maximum length of a
string or blob, the maximum size of a database, the maximum number of
tables in a database, etc.) and how these limits can be altered at
compile-time and run-time.
- [Memory-Mapped I/O](mmap.html)
→
SQLite supports memory-mapped I/O. Learn how to enable memory-mapped
I/O and about the various advantages and disadvantages to using
memory-mapped I/O in this document.
- [Multi-threaded Programs and SQLite](threadsafe.html)
→
SQLite is safe to use in multi-threaded programs. This document
provides the details and hints on how to maximize performance.
- [Null Handling](nulls.html)
→
Different SQL database engines handle NULLs in different ways. The
SQL standards are ambiguous. This (circa 2003) document describes
how SQLite handles NULLs in comparison with other SQL database engines.
- [Partial Indexes](partialindex.html)
→
A partial index is an index that only covers a subset of the rows in
a table. Learn how to use partial indexes in SQLite from this document.
- [Shared Cache Mode](sharedcache.html)
→
Version 3.3.0 and later supports the ability for two or more
database connections to share the same page and schema cache.
This feature is useful for certain specialized applications.
- [Unlock Notify](unlock_notify.html)
→
The "unlock notify" feature can be used in conjunction with
[shared cache mode](sharedcache.html) to more efficiently
manage resource conflict (database table locks).
- [URI Filenames](uri.html)
→
The names of database files can be specified using either an ordinary
filename or a URI. Using URI filenames provides additional capabilities,
as this document describes.
- [WITHOUT ROWID Tables](withoutrowid.html)
→
The WITHOUT ROWID optimization is a option that can sometimes result
in smaller and faster databases.
- [Write-Ahead Log (WAL) Mode](wal.html)
→
Transaction control using a write-ahead log offers more concurrency and
is often faster than the default rollback transactions. This document
explains how to use WAL mode for improved performance.
- ► Tools
- [Command-Line Shell (sqlite3.exe)](cli.html)
→
Notes on using the "sqlite3.exe" command-line interface that
can be used to create, modify, and query arbitrary SQLite
database files.
- [Remote Copy Of A Live Database](rsync.html)
→
The sqlite3_rsync program makes a consistent copy of a
live database to or from a remote system.
- [Database Hash (dbhash.exe)](dbhash.html)
→
This program demonstrates how to compute a hash over the content
of an SQLite database.
- [Fossil](http://www.fossil-scm.org/)
→
The Fossil Version Control System is a distributed VCS designed specifically
to support SQLite development. Fossil uses SQLite as for storage.
- [RBU](rbu.html)
→
The "Resumable Bulk Update" utility program allows a batch of changes
to be applied to a remote database running on embedded hardware in a
way that is resumeable and does not interrupt ongoing operation.
- [SQLite Database Analyzer (sqlite3_analyzer.exe)](sqlanalyze.html)
→
This stand-alone program reads an SQLite database and outputs a file
showing the space used by each table and index and other statistics.
Built using the [dbstat virtual table](dbstat.html).
- [SQLite Database Diff (sqldiff.exe)](sqldiff.html)
→
This stand-alone program compares two SQLite database files and
outputs the SQL needed to convert one into the other.
- [SQLite Archiver (sqlar.exe)](https://sqlite.org/sqlar/)
→
A ZIP-like archive program that uses SQLite for storage.
- ► Advocacy
- [35% Faster Than The Filesystem](fasterthanfs.html)
→
This article points out that reading blobs out of an SQLite database
is often faster than reading the same blobs from individual files in
the filesystem.
- [Flexible Typing Is A Feature](flextypegood.html)
→
SQLite provides developers with the freedom to store content in any
desired format, regardless of the declared datatype of the column.
This article explains why that is a feature, not a bug.
- [SQLite As An Application File Format](appfileformat.html)
→
This article advocates using SQLite as an application file format
in place of XML or JSON or a "pile-of-file".
- [Well Known Users](famous.html)
→
This page lists a small subset of the many thousands of devices
and application programs that make use of SQLite.
- [Why SQLite Is Coded In C](whyc.html)
→
Why is SQLite not coded in some other trendy language like C++ or
Rust? Isn't C obsolete?
- [Why SQLite Does Not Use Git](whynotgit.html)
→
Why SQLite does not use Git for version control, like most everybody
else?
- ► Technical and Design Documentation
- [How Database Corruption Can Occur](howtocorrupt.html)
→
SQLite is highly resistant to database corruption. But application,
OS, and hardware bugs can still result in corrupt database files.
This article describes many of the ways that SQLite database files
can go corrupt.
- [Defense Against Dark Arts](security.html)
→
Hints for avoiding application vulnerabilities when using SQLite.
- [Temporary Files Used By SQLite](tempfiles.html)
→
SQLite can potentially use many different temporary files when
processing certain SQL statements. This document describes the
many kinds of temporary files that SQLite uses and offers suggestions
for avoiding them on systems where creating a temporary file is an
expensive operation.
- [In-Memory Databases](inmemorydb.html)
→
SQLite normally stores content in a disk file. However, it can also
be used as an in-memory database engine. This document explains how.
- [How SQLite Implements Atomic Commit](atomiccommit.html)
→
A description of the logic within SQLite that implements
transactions with atomic commit, even in the face of power
failures.
- [Dynamic Memory Allocation in SQLite](malloc.html)
→
SQLite has a sophisticated memory allocation subsystem that can be
configured and customized to meet memory usage requirements of the
application and that is robust against out-of-memory conditions and
leak-free. This document provides the details.
- [Customizing And Porting SQLite](custombuild.html)
→
This document explains how to customize the build of SQLite and
how to port SQLite to new platforms.
- [Locking And Concurrency In SQLite Version 3](lockingv3.html)
→
A description of how the new locking code in version 3 increases
concurrency and decreases the problem of writer starvation.
- [Isolation In SQLite](isolation.html)
→
When we say that SQLite transactions are "serializable" what exactly
does that mean? How and when are changes made visible within the
same database connection and to other database connections?
- [Overview Of The Optimizer](optoverview.html)
→
A quick overview of the various query optimizations that are
attempted by the SQLite code generator.
- [The Next-Generation Query Planner](queryplanner-ng.html)
→
Additional information about the SQLite query planner, and in particular
the redesign of the query planner that occurred for version 3.8.0.
- [Architecture](arch.html)
→
An architectural overview of the SQLite library, useful for those who want
to hack the code.
- [VDBE Opcodes](opcode.html)
→
This document is an automatically generated description of the various
opcodes that the VDBE understands. Programmers can use this document as
a reference to better understand the output of EXPLAIN listings from
SQLite.
- [Virtual Filesystem](vfs.html)
→
The "VFS" object is the interface between the SQLite core and the
underlying operating system. Learn more about how the VFS object
works and how to create new VFS objects from this article.
- [Virtual Tables](vtab.html)
→
This article describes the virtual table mechanism and API in SQLite and how
it can be used to add new capabilities to the core SQLite library.
- [The SQLite File Format](fileformat2.html)
→
A description of the format used for SQLite database and journal files, and
other details required to create software to read and write SQLite
databases without using SQLite.
- [Compilation Options](compile.html)
→
This document describes the compile time options that may be set to
modify the default behavior of the library or omit optional features
in order to reduce binary size.
- [Android Bindings for SQLite](https://sqlite.org/android/)
→
A description of how to compile your own SQLite for Android
(bypassing the SQLite that is built into Android) together with
code and makefiles.
- [Debugging Hints](debugging.html)
→
A list of tricks and techniques used to trace, examine, and understand
the operation of the core SQLite library.
- ► Upgrading SQLite, Backwards Compatibility
- [Moving From SQLite 3.5 to 3.6](35to36.html)
→
A document describing the differences between SQLite version 3.5.9
and 3.6.0.
- [Moving From SQLite 3.4 to 3.5](34to35.html)
→
A document describing the differences between SQLite version 3.4.2
and 3.5.0.
- [Release History](changes.html)
→
A chronology of SQLite releases going back to version 1.0.0
- [Backwards Compatibility](formatchng.html)
→
This document details all of the incompatible changes to the SQLite
file format that have occurred since version 1.0.0.
- [Private Branches](privatebranch.html)
→
This document suggests procedures for maintaining a private branch
or fork of SQLite and keeping that branch or fork in sync with the
public SQLite source tree.
- ► Obsolete Documents
- [Asynchronous IO Mode](asyncvfs.html)
→
This page describes the asynchronous IO extension developed alongside
SQLite. Using asynchronous IO can cause SQLite to appear more responsive
by delegating database writes to a background thread. NB: This
extension is deprecated. [WAL mode](wal.html) is recommended
as a replacement.
- [Version 2 C/C++ API](c_interface.html)
→
A description of the C/C++ interface bindings for SQLite through version
2.8
- [Version 2 DataTypes](datatypes.html)
→
A description of how SQLite version 2 handles SQL datatypes.
Short summary: Everything is a string.
- [VDBE Tutorial](vdbe.html)
→
The VDBE is the subsystem within SQLite that does the actual work of
executing SQL statements. This page describes the principles of operation
for the VDBE in SQLite version 2.7. This is essential reading for anyone
who want to modify the SQLite sources.
- [SQLite Version 3](version3.html)
→
A summary of the changes between SQLite version 2.8 and SQLite version 3.0.
- [Version 3 C/C++ API](capi3.html)
→
A summary of the API related changes between SQLite version 2.8 and
SQLite version 3.0.
- [Speed Comparison](speed.html)
→
The speed of version 2.7.6 of SQLite is compared against PostgreSQL and
MySQL.