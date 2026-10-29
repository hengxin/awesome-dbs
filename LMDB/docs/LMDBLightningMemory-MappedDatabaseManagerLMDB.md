# LMDB: Lightning Memory-Mapped Database Manager (LMDB)

- 来源: http://www.lmdb.tech/doc/
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

LMDB
1.0
- [Main Page](index.html)
- [Related Pages](pages.html)
- [Modules](modules.html)
- [Data Structures](annotated.html)
- [Files](files.html)
-
[](javascript:searchBox.CloseResultsWindow())
[ All](javascript:void(0))[ Data Structures](javascript:void(0))[ Files](javascript:void(0))[ Functions](javascript:void(0))[ Variables](javascript:void(0))[ Typedefs](javascript:void(0))[ Enumerations](javascript:void(0))[ Enumerator](javascript:void(0))[ Macros](javascript:void(0))[ Groups](javascript:void(0))[ Pages](javascript:void(0))
Lightning Memory-Mapped Database Manager (LMDB)
#
Introduction
LMDB is a Btree-based database management library modeled loosely on the BerkeleyDB API, but much simplified. The entire database is exposed in a memory map, and all data fetches return data directly from the mapped memory, so no malloc's or memcpy's occur during data fetches. As such, the library is extremely simple because it requires no page caching layer of its own, and it is extremely high performance and memory-efficient. It is also fully transactional with full ACID semantics, and when the memory map is read-only, the database integrity cannot be corrupted by stray pointer writes from application code.
## Note: This is the documentation for LMDB 1.0. The docs for LMDB 0.9 are archived [here](lmdb0.9/).
See [Upgrading From Release 0.9](upgrading.html) if you used LMDB 0.9 previously.
The library is fully thread-aware and supports concurrent read/write access from multiple processes and threads. Data pages use a copy-on- write strategy so no active data pages are ever overwritten, which also provides resistance to corruption and eliminates the need of any special recovery procedures after a system crash. Writes are fully serialized; only one write transaction may be active at a time, which guarantees that writers can never deadlock. The database structure is multi-versioned so readers run with no locks; writers cannot block readers, and readers don't block writers.
Unlike other well-known database mechanisms which use either write-ahead transaction logs or append-only data writes, LMDB requires no maintenance during operation. Both write-ahead loggers and append-only databases require periodic checkpointing and/or compaction of their log or database files otherwise they grow without bound. LMDB tracks free pages within the database and re-uses them for new write operations, so the database size does not grow without bound in normal use.
The memory map can be used as a read-only or read-write map. It is read-only by default as this provides total immunity to corruption. Using read-write mode offers much higher write performance, but adds the possibility for stray application writes thru pointers to silently corrupt the database. Of course if your application code is known to be bug-free (...) then this is not an issue.
If this is your first time using a transactional embedded key/value store, you may find the [Getting Started](starting.html) page to be helpful.
#
Caveats
Troubleshooting the lock file, plus semaphores on BSD systems:
- A broken lockfile can cause sync issues. Stale reader transactions left behind by an aborted program cause further writes to grow the database quickly, and stale locks can block further operation.
Fix: Check for stale readers periodically, using the [mdb_reader_check](group__internal.html#ga576f9ec8e49724e52b2cd7ce7b832856) function or the [mdb_stat](./man1/mdb_stat_1.html) tool. Stale writers will be cleared automatically on most systems:
- Windows - automatic
- BSD, systems using SysV semaphores - automatic
- Linux, systems using POSIX mutexes with Robust option - automatic Otherwise just make all programs using the database close it; the lockfile is always reset on first open of the environment.
- On BSD systems or others configured with MDB_USE_SYSV_SEM or MDB_USE_POSIX_SEM, startup can fail due to semaphores owned by another userid.
Fix: Open and close the database as the user which owns the semaphores (likely last user) or as root, while no other process is using the database.
Restrictions/caveats (in addition to those listed for some functions):
- Only the database owner should normally use the database on BSD systems or when otherwise configured with MDB_USE_POSIX_SEM. Multiple users can cause startup to fail later, as noted above.
- There is normally no pure read-only mode, since readers need write access to locks and lock file. Exceptions: On read-only filesystems or with the [MDB_NOLOCK](group__mdb__env.html#ga9b0450b1a87cb9f22e033550e49e5037) flag described under [mdb_env_open()](group__mdb.html#ga32a193c6bf4d7d5c5d579e71f22e9340).
- An LMDB configuration will often reserve considerable unused memory address space and maybe file size for future growth. This does not use actual memory or disk space, but users may need to understand the difference so they won't be scared off.
- By default, in versions before 0.9.10, unused portions of the data file might receive garbage data from memory freed by other code. (This does not happen when using the [MDB_WRITEMAP](group__mdb__env.html#ga7b81e9fd5f8fae38786d67e1a8387fa7) flag.) As of 0.9.10 the default behavior is to initialize such memory before writing to the data file. Since there may be a slight performance cost due to this initialization, applications may disable it using the [MDB_NOMEMINIT](group__mdb__env.html#gafa035a1f17ebf31376eafb7bd2cdd448) flag. Applications handling sensitive data which must not be written should not use this flag. This flag is irrelevant when using [MDB_WRITEMAP](group__mdb__env.html#ga7b81e9fd5f8fae38786d67e1a8387fa7).
- A thread can only use one transaction at a time, plus any child transactions. Each transaction belongs to one thread. See below. The [MDB_NOTLS](group__mdb__env.html#ga5dca84a576d14b4bfe2deddc2dc622d3) flag changes this for read-only transactions.
- Use an MDB_env* in the process which opened it, not after fork().
- Do not have open an LMDB database twice in the same process at the same time. Not even from a plain open() call - close()ing it breaks fcntl() advisory locking. (It is OK to reopen it after fork() - exec*(), since the lockfile has FD_CLOEXEC set.)
- Avoid long-lived transactions. Read transactions prevent reuse of pages freed by newer write transactions, thus the database can grow quickly. Write transactions prevent other write transactions, since writes are serialized.
- Avoid suspending a process with active transactions. These would then be "long-lived" as above. Also read transactions suspended when writers commit could sometimes see wrong data.
...when several processes can use a database concurrently:
- Avoid aborting a process with an active transaction. The transaction becomes "long-lived" as above until a check for stale readers is performed or the lockfile is reset, since the process may not remove it from the lockfile.
This does not apply to write transactions if the system clears stale writers, see above.
- If you do that anyway, do a periodic check for stale readers. Or close the environment once in a while, so the lockfile can get reset.
- Do not use LMDB databases on remote filesystems, even between processes on the same host. This breaks flock() on some OSes, possibly memory map sync, and certainly sync between programs on different hosts.
- Opening a database can fail if another process is opening or closing it at exactly the same time.
Author Howard Chu, Symas Corporation.
Copyright Copyright 2011-2026 Howard Chu, Symas Corp. All rights reserved.
Redistribution and use in source and binary forms, with or without modification, are permitted only as authorized by the OpenLDAP Public License.
A copy of this license is available in the file LICENSE in the top-level directory of the distribution or, alternatively, at [http://www.OpenLDAP.org/license.html](http://www.OpenLDAP.org/license.html).
Derived From: This code is derived from btree.c written by Martin Hedenfalk.
Copyright (c) 2009, 2010 Martin Hedenfalk [marti.nosp@m.n@bz.nosp@m.ero.s.nosp@m.e](mai)
Permission to use, copy, modify, and distribute this software for any purpose with or without fee is hereby granted, provided that the above copyright notice and this permission notice appear in all copies.
THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.
Generated on Tue Jun 30 2026 20:10:10 for LMDB by  [](http://www.doxygen.org/index.html) 1.8.2-20120930