# Apache HBase® Reference Guide

- 来源: https://hbase.apache.org/book.html
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

These docs are legacy and not supported anymore. Please go to
[hbase.apache.org/docs](https://hbase.apache.org/docs/).
# Apache HBase ® Reference Guide
Apache HBase Team
<[hbase-dev@lists.apache.org](mailto:hbase-dev@lists.apache.org)>
version 4.0.0-alpha-1-SNAPSHOT
Contents
- [Preface](#_preface)
- [Getting Started](#getting_started)
- [1. Introduction](#_introduction)
- [2. Quick Start - Standalone HBase](#quickstart)
- [Apache HBase Configuration](#configuration)
- [3. Configuration Files](#_configuration_files)
- [4. Basic Prerequisites](#basic.prerequisites)
- [5. HBase run modes: Standalone and Distributed](#standalone_dist)
- [6. Running and Confirming Your Installation](#confirm)
- [7. Default Configuration](#config.files)
- [8. Example Configurations](#example_config)
- [9. The Important Configurations](#important_configurations)
- [10. Dynamic Configuration](#dyn_config)
- [Upgrading](#upgrading)
- [11. HBase version number and compatibility](#hbase.versioning)
- [12. Rollback](#_rollback)
- [13. Upgrade Paths](#_upgrade_paths)
- [The Apache HBase Shell](#shell)
- [14. Scripting with Ruby](#scripting)
- [15. Running the Shell in Non-Interactive Mode](#_running_the_shell_in_non_interactive_mode)
- [16. HBase Shell in OS Scripts](#hbase.shell.noninteractive)
- [17. Read HBase Shell Commands from a Command File](#_read_hbase_shell_commands_from_a_command_file)
- [18. Passing VM Options to the Shell](#_passing_vm_options_to_the_shell)
- [19. Overriding configuration starting the HBase Shell](#_overriding_configuration_starting_the_hbase_shell)
- [20. Shell Tricks](#_shell_tricks)
- [Data Model](#datamodel)
- [21. Conceptual View](#conceptual.view)
- [22. Physical View](#physical.view)
- [23. Namespace](#_namespace)
- [24. Table](#_table)
- [25. Row](#_row)
- [26. Column Family](#columnfamily)
- [27. Cells](#_cells)
- [28. Data Model Operations](#_data_model_operations)
- [29. Versions](#versions)
- [30. Sort Order](#dm.sort)
- [31. Column Metadata](#dm.column.metadata)
- [32. Joins](#joins)
- [33. ACID](#_acid)
- [HBase and Schema Design](#schema)
- [34. Schema Creation](#schema.creation)
- [35. Table Schema Rules Of Thumb](#table_schema_rules_of_thumb)
- [RegionServer Sizing Rules of Thumb](#regionserver_sizing_rules_of_thumb)
- [36. On the number of column families](#number.of.cfs)
- [37. Rowkey Design](#rowkey.design)
- [38. Number of Versions](#schema.versions)
- [39. Supported Datatypes](#supported.datatypes)
- [40. Joins](#schema.joins)
- [41. Time To Live (TTL)](#ttl)
- [42. Keeping Deleted Cells](#cf.keep.deleted)
- [43. Secondary Indexes and Alternate Query Paths](#secondary.indexes)
- [44. Constraints](#_constraints)
- [45. Schema Design Case Studies](#schema.casestudies)
- [46. Operational and Performance Configuration Options](#schema.ops)
- [47. Special Cases](#_special_cases)
- [HBase and MapReduce](#mapreduce)
- [48. HBase, MapReduce, and the CLASSPATH](#hbase.mapreduce.classpath)
- [49. MapReduce Scan Caching](#_mapreduce_scan_caching)
- [50. Bundled HBase MapReduce Jobs](#_bundled_hbase_mapreduce_jobs)
- [51. HBase as a MapReduce Job Data Source and Data Sink](#_hbase_as_a_mapreduce_job_data_source_and_data_sink)
- [52. Writing HFiles Directly During Bulk Import](#_writing_hfiles_directly_during_bulk_import)
- [53. RowCounter Example](#_rowcounter_example)
- [54. Map-Task Splitting](#splitter)
- [55. HBase MapReduce Examples](#mapreduce.example)
- [56. Accessing Other HBase Tables in a MapReduce Job](#mapreduce.htable.access)
- [57. Speculative Execution](#mapreduce.specex)
- [Securing Apache HBase](#security)
- [58. Web UI Security](#_web_ui_security)
- [59. Secure Client Access to Apache HBase](#hbase.secure.configuration)
- [60. Simple User Access to Apache HBase](#hbase.secure.simpleconfiguration)
- [61. Transport Level Security (TLS) in HBase RPC communication](#_transport_level_security_tls_in_hbase_rpc_communication)
- [62. Securing Access to HDFS and ZooKeeper](#_securing_access_to_hdfs_and_zookeeper)
- [63. Securing Access To Your Data](#_securing_access_to_your_data)
- [64. Security Configuration Example](#security.example.config)
- [Architecture](#_architecture)
- [65. Overview](#arch.overview)
- [66. Catalog Tables](#arch.catalog)
- [67. Client](#architecture.client)
- [68. Client Request Filters](#client.filter)
- [69. Master](#architecture.master)
- [70. RegionServer](#regionserver.arch)
- [71. Regions](#regions.arch)
- [72. Bulk Loading](#arch.bulk.load)
- [73. HDFS](#arch.hdfs)
- [74. Timeline-consistent High Available Reads](#arch.timelineconsistent.reads)
- [75. Storing Medium-sized Objects (MOB)](#hbase_mob)
- [76. Scan over snapshot](#snapshot_scanner)
- [In-memory Compaction](#inmemory_compaction)
- [77. Overview](#imc.overview)
- [78. Enabling](#_enabling)
- [RegionServer Offheap Read/Write Path](#offheap_read_write)
- [79. Overview](#regionserver.offheap.overview)
- [80. Offheap read-path](#regionserver.offheap.readpath)
- [81. Read block from HDFS to offheap directly](#regionserver.read.hdfs.block.offheap)
- [82. Offheap write-path](#regionserver.offheap.writepath)
- [Backup and Restore](#backuprestore)
- [83. Overview](#br.overview)
- [84. Terminology](#br.terminology)
- [85. Planning](#br.planning)
- [86. First-time configuration steps](#br.initial.setup)
- [87. Backup and Restore commands](#_backup_and_restore_commands)
- [88. Administration of Backup Images](#br.administration)
- [89. Configuration keys](#br.backup.configuration)
- [90. Best Practices](#br.best.practices)
- [91. Scenario: Safeguarding Application Datasets on Amazon S3](#br.s3.backup.scenario)
- [92. Security of Backup Data](#br.data.security)
- [93. Technical Details of Incremental Backup and Restore](#br.technical.details)
- [94. A Warning on File System Growth](#br.filesystem.growth.warning)
- [95. Capacity Planning](#br.backup.capacity.planning)
- [96. Limitations of the Backup and Restore Utility](#br.limitations)
- [Synchronous Replication](#syncreplication)
- [97. Background](#_background)
- [98. Design](#_design)
- [99. Operation and maintenance](#_operation_and_maintenance)
- [Apache HBase APIs](#hbase_apis)
- [100. Examples](#_examples)
- [Apache HBase External APIs](#external_apis)
- [101. REST](#_rest)
- [102. Thrift](#_thrift)
- [103. C/C++ Apache HBase Client](#c)
- [104. Using Java Data Objects (JDO) with HBase](#jdo)
- [105. Scala](#scala)
- [106. Jython](#jython)
- [Thrift API and Filter Language](#thrift)
- [107. Filter Language](#thrift.filter_language)
- [HBase and Spark](#spark)
- [108. Basic Spark](#_basic_spark)
- [109. Spark Streaming](#_spark_streaming)
- [110. Bulk Load](#_bulk_load)
- [111. SparkSQL/DataFrames](#_sparksqldataframes)
- [Apache HBase Coprocessors](#cp)
- [112. Coprocessor Overview](#_coprocessor_overview)
- [113. Types of Coprocessors](#_types_of_coprocessors)
- [114. Loading Coprocessors](#cp_loading)
- [115. Examples](#cp_example)
- [116. Guidelines For Deploying A Coprocessor](#_guidelines_for_deploying_a_coprocessor)
- [117. Restricting Coprocessor Usage](#_restricting_coprocessor_usage)
- [Apache HBase Performance Tuning](#performance)
- [118. Operating System](#perf.os)
- [119. Network](#perf.network)
- [120. Java](#jvm)
- [121. HBase Configurations](#perf.configurations)
- [122. ZooKeeper](#perf.zookeeper)
- [123. Schema Design](#perf.schema)
- [124. HBase General Patterns](#perf.general)
- [125. Writing to HBase](#perf.writing)
- [126. Reading from HBase](#perf.reading)
- [127. Deleting from HBase](#perf.deleting)
- [128. HDFS](#perf.hdfs)
- [129. Amazon EC2](#perf.ec2)
- [130. Collocating HBase and MapReduce](#perf.hbase.mr.cluster)
- [131. Case Studies](#perf.casestudy)
- [Profiler Servlet](#profiler)
- [132. Background](#_background_2)
- [133. Prerequisites](#_prerequisites_2)
- [134. Usage](#_usage)
- [135. UI](#_ui)
- [136. Notes](#_notes_2)
- [Troubleshooting and Debugging Apache HBase](#trouble)
- [137. General Guidelines](#trouble.general)
- [138. Logs](#trouble.log)
- [139. Resources](#trouble.resources)
- [140. Tools](#trouble.tools)
- [141. Client](#trouble.client)
- [142. MapReduce](#trouble.mapreduce)
- [143. NameNode](#trouble.namenode)
- [144. Network](#trouble.network)
- [145. RegionServer](#trouble.rs)
- [146. Master](#trouble.master)
- [147. ZooKeeper](#trouble.zookeeper)
- [148. Amazon EC2](#trouble.ec2)
- [149. HBase and Hadoop version issues](#trouble.versions)
- [150. HBase and HDFS](#_hbase_and_hdfs)
- [151. Running unit or integration tests](#trouble.tests)
- [152. Case Studies](#trouble.casestudy)
- [153. Cryptographic Features](#trouble.crypto)
- [154. Operating System Specific Issues](#_operating_system_specific_issues)
- [155. JDK Issues](#_jdk_issues)
- [Apache HBase Case Studies](#casestudies)
- [156. Overview](#casestudies.overview)
- [157. Schema Design](#casestudies.schema)
- [158. Performance/Troubleshooting](#casestudies.perftroub)
- [Apache HBase Operational Management](#ops_mgt)
- [159. HBase Tools and Utilities](#tools)
- [160. Region Management](#ops.regionmgt)
- [161. Node Management](#node.management)
- [162. HBase Metrics](#hbase_metrics)
- [163. HBase Monitoring](#ops.monitoring)
- [164. Cluster Replication](#_cluster_replication)
- [165. Running Multiple Workloads On a Single Cluster](#_running_multiple_workloads_on_a_single_cluster)
- [166. HBase Backup](#ops.backup)
- [167. HBase Snapshots](#ops.snapshots)
- [168. Storing Snapshots in Microsoft Azure Blob Storage](#snapshots_azure)
- [169. Storing Snapshots in Aliyun Object Storage Service](#snapshots_oss)
- [170. Capacity Planning and Region Sizing](#ops.capacity)
- [171. Table Rename](#table.rename)
- [172. RegionServer Grouping](#rsgroup)
- [173. Region Normalizer](#normalizer)
- [174. Auto Region Reopen](#auto_reopen_regions)
- [Building and Developing Apache HBase](#developer)
- [175. Getting Involved](#getting.involved)
- [176. Apache HBase Repositories](#repos)
- [177. IDEs](#_ides)
- [178. Building Apache HBase](#build)
- [179. Releasing Apache HBase](#releasing)
- [180. Voting on Release Candidates](#hbase.rc.voting)
- [181. Announcing Releases](#hbase.release.announcement)
- [182. Generating the HBase Reference Guide](#documentation)
- [183. Updating hbase.apache.org](#hbase.org)
- [184. Tests](#hbase.tests)
- [185. Developer Guidelines](#developing)
- [Unit Testing HBase Applications](#unit.tests)
- [186. JUnit](#_junit)
- [187. Mockito](#mockito)
- [188. MRUnit](#_mrunit)
- [189. Integration Testing with an HBase Mini-Cluster](#_integration_testing_with_an_hbase_mini_cluster)
- [Protobuf in HBase](#protobuf)
- [190. Protobuf](#_protobuf)
- [Procedure Framework (Pv2): HBASE-12439](#pv2)
- [191. Procedures](#_procedures)
- [192. Subprocedures](#_subprocedures)
- [193. ProcedureExecutor](#_procedureexecutor)
- [194. Nonces](#_nonces)
- [195. Wait/Wake/Suspend/Yield](#_waitwakesuspendyield)
- [196. Locking](#_locking)
- [197. Procedure Types](#_procedure_types)
- [198. References](#_references)
- [AMv2 Description for Devs](#amv2)
- [199. Background](#_background_3)
- [200. New System](#_new_system)
- [201. Procedures Detail](#_procedures_detail)
- [202. UI](#_ui_2)
- [203. Logging](#_logging)
- [204. Implementation Notes](#_implementation_notes)
- [205. New Configs](#_new_configs)
- [206. Tools](#_tools)
- [ZooKeeper](#zookeeper)
- [207. Using existing ZooKeeper ensemble](#_using_existing_zookeeper_ensemble)
- [208. SASL Authentication with ZooKeeper](#zk.sasl.auth)
- [209. TLS connection to ZooKeeper](#_tls_connection_to_zookeeper)
- [Community](#community)
- [210. Decisions](#_decisions)
- [211. Community Roles](#community.roles)
- [212. Commit Message format](#hbase.commit.msg.format)
- [hbtop](#hbtop)
- [213. Overview](#_overview_2)
- [214. Usage](#_usage_2)
- [215. Others](#_others_2)
- [Tracing](#tracing)
- [216. Overview](#_overview_3)
- [217. Usage](#_usage_3)
- [Store File Tracking](#storefiletracking)
- [218. Overview](#_overview_4)
- [219. Available Implementations](#_available_implementations)
- [220. Usage](#_usage_4)
- [Bulk Data Generator Tool](#BulkDataGeneratorTool)
- [221. Usage](#_usage_5)
- [222. Overview](#_overview_5)
- [Appendix](#_appendix)
- [Appendix A: Contributing to Documentation](#appendix_contributing_to_documentation)
- [Appendix B: FAQ](#faq)
- [Appendix C: Access Control Matrix](#appendix_acl_matrix)
- [Appendix D: Compression and Data Block Encoding In HBase](#compression)
- [Appendix E: SQL over HBase](#sql)
- [Appendix F: YCSB](#ycsb)
- [Appendix G: HFile format](#_hfile_format_2)
- [Appendix H: Other Information About HBase](#other.info)
- [Appendix I: HBase History](#hbase.history)
- [Appendix J: HBase and the Apache Software Foundation](#asf)
- [Appendix K: Apache HBase Orca](#orca)
- [Appendix L: 0.95 RPC Specification](#hbase.rpc)
- [Appendix M: Known Incompatibilities Among HBase Versions](#_known_incompatibilities_among_hbase_versions)
- [223. HBase 2.0 Incompatible Changes](#_hbase_2_0_incompatible_changes)
[](/)
## [](#_preface)Preface
This is the official reference guide for the [HBase](/) version it ships with.
Herein you will find either the definitive documentation on an HBase topic as of its
standing when the referenced HBase version shipped, or it will point to the location
in [Javadoc](https://hbase.apache.org/apidocs/index.html) or
[JIRA](https://issues.apache.org/jira/browse/HBASE) where the pertinent information can be found.
About This Guide
This reference guide is a work in progress. The source for this guide can be found in the
_src/main/asciidoc directory of the HBase source. This reference guide is marked up
using [AsciiDoc](http://asciidoc.org/) from which the finished guide is generated as part of the
'site' build target. Run
mvn site
to generate this documentation.
Amendments and improvements to the documentation are welcomed.
Click
[this link](https://issues.apache.org/jira/secure/CreateIssueDetails!init.jspa?pid=12310753&issuetype=1&components=12312132&summary=SHORT+DESCRIPTION)
to file a new documentation bug against Apache HBase with some values pre-selected.
Contributing to the Documentation
For an overview of AsciiDoc and suggestions to get started contributing to the documentation,
see the [relevant section later in this documentation](#appendix_contributing_to_documentation).
Heads-up if this is your first foray into the world of distributed computing…​
If this is your first foray into the wonderful world of Distributed Computing, then you are in for some interesting times.
First off, distributed systems are hard; making a distributed system hum requires a disparate skillset that spans systems (hardware and software) and networking.
Your cluster’s operation can hiccup because of any of a myriad set of reasons from bugs in HBase itself through misconfigurations — misconfiguration of HBase but also operating system misconfigurations — through to hardware problems whether it be a bug in your network card drivers or an underprovisioned RAM bus (to mention two recent examples of hardware issues that manifested as "HBase is slow"). You will also need to do a recalibration if up to this your computing has been bound to a single box.
Here is one good starting point: [Fallacies of Distributed Computing](http://en.wikipedia.org/wiki/Fallacies_of_Distributed_Computing).
That said, you are welcome.
It’s a fun place to be.
Yours, the HBase Community.
Reporting Bugs
Please use [JIRA](https://issues.apache.org/jira/browse/hbase) to report non-security-related bugs.
To protect existing HBase installations from new vulnerabilities, please do not use JIRA to report security-related bugs. Instead, send your report to the mailing list [private@hbase.apache.org](mailto:private@hbase.apache.org), which allows anyone to send messages, but restricts who can read them. Someone on that list will contact you to follow up on your report.
Support and Testing Expectations
The phrases /supported/, /not supported/, /tested/, and /not tested/ occur several
places throughout this guide. In the interest of clarity, here is a brief explanation
of what is generally meant by these phrases, in the context of HBase.
Commercial technical support for Apache HBase is provided by many Hadoop vendors.
This is not the sense in which the term /support/ is used in the context of the
Apache HBase project. The Apache HBase team assumes no responsibility for your
HBase clusters, your configuration, or your data.
Supported
In the context of Apache HBase, /supported/ means that HBase is designed to work
in the way described, and deviation from the defined behavior or functionality should
be reported as a bug.
Not Supported
In the context of Apache HBase, /not supported/ means that a use case or use pattern
is not expected to work and should be considered an antipattern. If you think this
designation should be reconsidered for a given feature or use pattern, file a JIRA
or start a discussion on one of the mailing lists.
Tested
In the context of Apache HBase, /tested/ means that a feature is covered by unit
or integration tests, and has been proven to work as expected.
Not Tested
In the context of Apache HBase, /not tested/ means that a feature or use pattern
may or may not work in a given way, and may or may not corrupt your data or cause
operational issues. It is an unknown, and there are no guarantees. If you can provide
proof that a feature designated as /not tested/ does work in a given way, please
submit the tests and/or the metrics so that other users can gain certainty about
such features or use patterns.
# [](#getting_started)Getting Started
## [](#_introduction)1. Introduction
[Quickstart](#quickstart) will get you up and running on a single-node, standalone instance of HBase.
## [](#quickstart)2. Quick Start - Standalone HBase
This section describes the setup of a single-node standalone HBase.
A standalone instance has all HBase daemons — the Master, RegionServers,
and ZooKeeper — running in a single JVM persisting to the local filesystem.
It is our most basic deploy profile. We will show you how
to create a table in HBase using the hbase shell CLI,
insert rows into the table, perform put and scan operations against the
table, enable or disable the table, and start and stop HBase.
Apart from downloading HBase, this procedure should take less than 10 minutes.
### [](#_jdk_version_requirements)2.1. JDK Version Requirements
HBase requires that a JDK be installed.
See [Java](#java) for information about supported JDK versions.
### [](#_get_started_with_hbase)2.2. Get Started with HBase
Procedure: Download, Configure, and Start HBase in Standalone Mode
-
Choose a download site from this list of [Apache Download Mirrors](https://www.apache.org/dyn/closer.lua/hbase/).
Click on the suggested top link.
This will take you to a mirror of HBase Releases .
Click on the folder named stable and then download the binary file that ends in .tar.gz to your local filesystem.
Do not download the file ending in src.tar.gz for now.
-
Extract the downloaded file, and change to the newly-created directory.
$ tar xzvf hbase-4.0.0-alpha-1-SNAPSHOT-bin.tar.gz
$ cd hbase-4.0.0-alpha-1-SNAPSHOT/
-
You must set the JAVA_HOME environment variable before starting HBase.
To make this easier, HBase lets you set it within the conf/hbase-env.sh file. You must locate where Java is
installed on your machine, and one way to find this is by using the whereis java command. Once you have the location,
edit the conf/hbase-env.sh file and uncomment the line starting with #export JAVA_HOME= , and then set it to your Java installation path.
Example extract from hbase-env.sh where JAVA_HOME is set
# Set environment variables here.
# The java implementation to use.
export JAVA_HOME=/usr/jdk64/jdk1.8.0_112
-
The bin/start-hbase.sh script is provided as a convenient way to start HBase.
Issue the command, and if all goes well, a message is logged to standard output showing that HBase started successfully.
You can use the jps command to verify that you have one running process called HMaster .
In standalone mode HBase runs all daemons within this single JVM, i.e.
the HMaster, a single HRegionServer, and the ZooKeeper daemon.
Go to [http://localhost:16010](http://localhost:16010/) to view the HBase Web UI.
Procedure: Use HBase For the First Time
-
Connect to HBase.
Connect to your running instance of HBase using the hbase shell command, located in the bin/ directory of your HBase install.
In this example, some usage and version information that is printed when you start HBase Shell has been omitted.
The HBase Shell prompt ends with a > character.
$ ./bin/hbase shell
hbase(main): 001 : 0 >
-
Display HBase Shell Help Text.
Type help and press Enter, to display some basic usage information for HBase Shell, as well as several example commands.
Notice that table names, rows, columns all must be enclosed in quote characters.
-
Create a table.
Use the create command to create a new table.
You must specify the table name and the ColumnFamily name.
hbase(main): 001 : 0 > create ' test ' , ' cf '
0 row(s) in 0.4170 seconds
=> Hbase::Table - test
-
List Information About your Table
Use the list command to confirm your table exists
hbase(main): 002 : 0 > list ' test '
TABLE
test
1 row(s) in 0.0180 seconds
=> [ " test " ]
Now use the describe command to see details, including configuration defaults
hbase(main): 003 : 0 > describe ' test '
Table test is ENABLED
test
COLUMN FAMILIES DESCRIPTION
{NAME => ' cf ' , VERSIONS => ' 1 ' , EVICT_BLOCKS_ON_CLOSE => ' false ' , NEW_VERSION_BEHAVIOR => ' false ' , KEEP_DELETED_CELLS => ' FALSE ' , CACHE_DATA_ON_WRITE =>
' false ' , DATA_BLOCK_ENCODING => ' NONE ' , TTL => ' FOREVER ' , MIN_VERSIONS => ' 0 ' , REPLICATION_SCOPE => ' 0 ' , BLOOMFILTER => ' ROW ' , CACHE_INDEX_ON_WRITE => ' f
alse ' , IN_MEMORY => ' false ' , CACHE_BLOOMS_ON_WRITE => ' false ' , PREFETCH_BLOCKS_ON_OPEN => ' false ' , COMPRESSION => ' NONE ' , BLOCKCACHE => ' true ' , BLOCKSIZE
=> ' 65536 ' }
1 row(s)
Took 0.9998 seconds
-
Put data into your table.
To put data into your table, use the put command.
hbase(main): 003 : 0 > put ' test ' , ' row1 ' , ' cf:a ' , ' value1 '
0 row(s) in 0.0850 seconds
hbase(main): 004 : 0 > put ' test ' , ' row2 ' , ' cf:b ' , ' value2 '
0 row(s) in 0.0110 seconds
hbase(main): 005 : 0 > put ' test ' , ' row3 ' , ' cf:c ' , ' value3 '
0 row(s) in 0.0100 seconds
Here, we insert three values, one at a time.
The first insert is at row1 , column cf:a , with a value of value1 .
Columns in HBase are comprised of a column family prefix, cf in this example, followed by a colon and then a column qualifier suffix, a in this case.
-
Scan the table for all data at once.
One of the ways to get data from HBase is to scan.
Use the scan command to scan the table for data.
You can limit your scan, but for now, all data is fetched.
hbase(main): 006 : 0 > scan ' test '
ROW COLUMN+CELL
row1 column=cf:a, timestamp= 1421762485768 , value=value1
row2 column=cf:b, timestamp= 1421762491785 , value=value2
row3 column=cf:c, timestamp= 1421762496210 , value=value3
3 row(s) in 0.0230 seconds
-
Get a single row of data.
To get a single row of data at a time, use the get command.
hbase(main): 007 : 0 > get ' test ' , ' row1 '
COLUMN CELL
cf:a timestamp= 1421762485768 , value=value1
1 row(s) in 0.0350 seconds
-
Disable a table.
If you want to delete a table or change its settings, as well as in some other situations, you need to disable the table first, using the disable command.
You can re-enable it using the enable command.
hbase(main): 008 : 0 > disable ' test '
0 row(s) in 1.1820 seconds
hbase(main): 009 : 0 > enable ' test '
0 row(s) in 0.1770 seconds
Disable the table again if you tested the enable command above:
hbase(main): 010 : 0 > disable ' test '
0 row(s) in 1.1820 seconds
-
Drop the table.
To drop (delete) a table, use the drop command.
hbase(main): 011 : 0 > drop ' test '
0 row(s) in 0.1370 seconds
-
Exit the HBase Shell.
To exit the HBase Shell and disconnect from your cluster, use the quit command.
HBase is still running in the background.
Procedure: Stop HBase
-
In the same way that the bin/start-hbase.sh script is provided to conveniently start all HBase daemons, the bin/stop-hbase.sh script stops them.
$ ./bin/stop-hbase.sh
stopping hbase....................
$
-
After issuing the command, it can take several minutes for the processes to shut down.
Use the jps to be sure that the HMaster and HRegionServer processes are shut down.
The above has shown you how to start and stop a standalone instance of HBase.
In the next sections we give a quick overview of other modes of hbase deploy.
### [](#quickstart_pseudo)2.3. Pseudo-Distributed for Local Testing
After working your way through [quickstart](#quickstart) standalone mode,
you can re-configure HBase to run in pseudo-distributed mode.
Pseudo-distributed mode means that HBase still runs completely on a single host,
but each HBase daemon (HMaster, HRegionServer, and ZooKeeper) runs as a separate process:
in standalone mode all daemons ran in one jvm process/instance.
By default, unless you configure the hbase.rootdir property as described in
[quickstart](#quickstart), your data is still stored in /tmp/ .
In this walk-through, we store your data in HDFS instead, assuming you have HDFS available.
You can skip the HDFS configuration to continue storing your data in the local filesystem.
Hadoop Configuration
This procedure assumes that you have configured Hadoop and HDFS on your local system and/or a remote
system, and that they are running and available. It also assumes you are using Hadoop 2.
The guide on
[Setting up a Single Node Cluster](https://hadoop.apache.org/docs/stable/hadoop-project-dist/hadoop-common/SingleCluster.html)
in the Hadoop documentation is a good starting point.
-
Stop HBase if it is running.
If you have just finished [quickstart](#quickstart) and HBase is still running, stop it.
This procedure will create a totally new directory where HBase will store its data, so any databases you created before will be lost.
-
Configure HBase.
Edit the hbase-site.xml configuration.
First, add the following property which directs HBase to run in distributed mode, with one JVM instance per daemon.
<property>
<name> hbase.cluster.distributed </name>
<value> true </value>
</property>
Next, add a configuration for hbase.rootdir , pointing to the address of your HDFS instance, using the hdfs://// URI syntax.
In this example, HDFS is running on the localhost at port 8020.
<property>
<name> hbase.rootdir </name>
<value> hdfs://localhost:9000/hbase </value>
</property>
You do not need to create the directory in HDFS.
HBase will do this for you. If you create the directory, HBase will attempt to do a migration, which is not what you want.
Finally, remove existing configuration for hbase.tmp.dir and hbase.unsafe.stream.capability.enforce ,
-
Start HBase.
Use the bin/start-hbase.sh command to start HBase.
If your system is configured correctly, the jps command should show the HMaster and HRegionServer processes running.
-
Check the HBase directory in HDFS.
If everything worked correctly, HBase created its directory in HDFS.
In the configuration above, it is stored in /hbase/ on HDFS.
You can use the hadoop fs command in Hadoop’s bin/ directory to list this directory.
$ ./bin/hadoop fs -ls /hbase
Found 7 items
drwxr-xr-x - hbase users 0 2014 - 06 - 25 18 : 58 /hbase/.tmp
drwxr-xr-x - hbase users 0 2014 - 06 - 25 21 : 49 /hbase/WALs
drwxr-xr-x - hbase users 0 2014 - 06 - 25 18 : 48 /hbase/corrupt
drwxr-xr-x - hbase users 0 2014 - 06 - 25 18 : 58 /hbase/data
-rw-r--r-- 3 hbase users 42 2014 - 06 - 25 18 : 41 /hbase/hbase.id
-rw-r--r-- 3 hbase users 7 2014 - 06 - 25 18 : 41 /hbase/hbase.version
drwxr-xr-x - hbase users 0 2014 - 06 - 25 21 : 49 /hbase/oldWALs
-
Create a table and populate it with data.
You can use the HBase Shell to create a table, populate it with data, scan and get values from it, using the same procedure as in [shell exercises](#shell_exercises).
-
Start and stop a backup HBase Master (HMaster) server.
Running multiple HMaster instances on the same hardware does not make sense in a production environment, in the same way that running a pseudo-distributed cluster does not make sense for production.
This step is offered for testing and learning purposes only.
The HMaster server controls the HBase cluster.
You can start up to 9 backup HMaster servers, which makes 10 total HMasters, counting the primary.
To start a backup HMaster, use the local-master-backup.sh .
For each backup master you want to start, add a parameter representing the port offset for that master.
Each HMaster uses two ports (16000 and 16010 by default). The port offset is added to these ports, so using an offset of 2, the backup HMaster would use ports 16002 and 16012.
The following command starts 3 backup servers using ports 16002/16012, 16003/16013, and 16005/16015.
$ ./bin/local-master-backup.sh start 2 3 5
To kill a backup master without killing the entire cluster, you need to find its process ID (PID). The PID is stored in a file with a name like /tmp/hbase-USER-X-master.pid .
The only contents of the file is the PID.
You can use the kill -9 command to kill that PID.
The following command will kill the master with port offset 1, but leave the cluster running:
$ cat /tmp/hbase-testuser- 1 -master.pid |xargs kill - 9
-
Start and stop additional RegionServers
The HRegionServer manages the data in its StoreFiles as directed by the HMaster.
Generally, one HRegionServer runs per node in the cluster.
Running multiple HRegionServers on the same system can be useful for testing in pseudo-distributed mode.
The local-regionservers.sh command allows you to run multiple RegionServers.
It works in a similar way to the local-master-backup.sh command, in that each parameter you provide represents the port offset for an instance.
Each RegionServer requires two ports, and the default ports are 16020 and 16030.
Since HBase version 1.1.0, HMaster doesn’t use region server ports, this leaves 10 ports (16020 to 16029 and 16030 to 16039) to be used for RegionServers.
For supporting additional RegionServers, set environment variables HBASE_RS_BASE_PORT and HBASE_RS_INFO_BASE_PORT to appropriate values before running script local-regionservers.sh .
e.g. With values 16200 and 16300 for base ports, 99 additional RegionServers can be supported, on a server.
The following command starts four additional RegionServers, running on sequential ports starting at 16022/16032 (base ports 16020/16030 plus 2).
$ ./bin/local-regionservers.sh start 2 3 4 5
To stop a RegionServer manually, use the local-regionservers.sh command with the stop parameter and the offset of the server to stop.
$ ./bin/local-regionservers.sh stop 3
-
Stop HBase.
You can stop HBase the same way as in the [quickstart](#quickstart) procedure, using the bin/stop-hbase.sh command.
### [](#quickstart_fully_distributed)2.4. Fully Distributed for Production
In reality, you need a fully-distributed configuration to fully test HBase and to use it in real-world scenarios.
In a distributed configuration, the cluster contains multiple nodes, each of which runs one or more HBase daemon.
These include primary and backup Master instances, multiple ZooKeeper nodes, and multiple RegionServer nodes.
This advanced quickstart adds two more nodes to your cluster.
The architecture will be as follows:
Table 1. Distributed Cluster Demo Architecture
Node Name
Master
ZooKeeper
RegionServer
node-a.example.com
yes
yes
no
node-b.example.com
backup
yes
yes
node-c.example.com
no
yes
yes
This quickstart assumes that each node is a virtual machine and that they are all on the same network.
It builds upon the previous quickstart, [Pseudo-Distributed for Local Testing](#quickstart_pseudo), assuming that the system you configured in that procedure is now node-a .
Stop HBase on node-a before continuing.
Be sure that all the nodes have full access to communicate, and that no firewall rules are in place which could prevent them from talking to each other.
If you see any errors like no route to host , check your firewall.
Procedure: Configure Passwordless SSH Access
node-a needs to be able to log into node-b and node-c (and to itself) in order to start the daemons.
The easiest way to accomplish this is to use the same username on all hosts, and configure password-less SSH login from node-a to each of the others.
-
On node-a , generate a key pair.
While logged in as the user who will run HBase, generate a SSH key pair, using the following command:
$ ssh-keygen -t rsa
If the command succeeds, the location of the key pair is printed to standard output.
The default name of the public key is id_rsa.pub .
-
Create the directory that will hold the shared keys on the other nodes.
On node-b and node-c , log in as the HBase user and create a .ssh/ directory in the user’s home directory, if it does not already exist.
If it already exists, be aware that it may already contain other keys.
-
Copy the public key to the other nodes.
Securely copy the public key from node-a to each of the nodes, by using the scp or some other secure means.
On each of the other nodes, create a new file called .ssh/authorized_keys if it does
not already exist , and append the contents of the id_rsa.pub file to the end of it.
Note that you also need to do this for node-a itself.
$ cat id_rsa.pub >> ~/.ssh/authorized_keys
-
Test password-less login.
If you performed the procedure correctly, you should not be prompted for a password when you SSH from node-a to either of the other nodes using the same username.
-
Since node-b will run a backup Master, repeat the procedure above, substituting node-b everywhere you see node-a .
Be sure not to overwrite your existing .ssh/authorized_keys files, but concatenate the new key onto the existing file using the >> operator rather than the > operator.
Procedure: Prepare node-a
node-a will run your primary master and ZooKeeper processes, but no RegionServers. Stop the RegionServer from starting on node-a .
-
Edit conf/regionservers and remove the line which contains localhost . Add lines with the hostnames or IP addresses for node-b and node-c .
Even if you did want to run a RegionServer on node-a , you should refer to it by the hostname the other servers would use to communicate with it.
In this case, that would be node-a.example.com .
This enables you to distribute the configuration to each node of your cluster any hostname conflicts.
Save the file.
-
Configure HBase to use node-b as a backup master.
Create a new file in conf/ called backup-masters , and add a new line to it with the hostname for node-b .
In this demonstration, the hostname is node-b.example.com .
-
Configure ZooKeeper
In reality, you should carefully consider your ZooKeeper configuration.
You can find out more about configuring ZooKeeper in [zookeeper](#zookeeper) section.
This configuration will direct HBase to start and manage a ZooKeeper instance on each node of the cluster.
On node-a , edit conf/hbase-site.xml and add the following properties.
<property>
<name> hbase.zookeeper.quorum </name>
<value> node-a.example.com,node-b.example.com,node-c.example.com </value>
</property>
<property>
<name> hbase.zookeeper.property.dataDir </name>
<value> /usr/local/zookeeper </value>
</property>
-
Everywhere in your configuration that you have referred to node-a as localhost , change the reference to point to the hostname that the other nodes will use to refer to node-a .
In these examples, the hostname is node-a.example.com .
Procedure: Prepare node-b and node-c
node-b will run a backup master server and a ZooKeeper instance.
-
Download and unpack HBase.
Download and unpack HBase to node-b , just as you did for the standalone and pseudo-distributed quickstarts.
-
Copy the configuration files from node-a to node-b .and node-c .
Each node of your cluster needs to have the same configuration information.
Copy the contents of the conf/ directory to the conf/ directory on node-b and node-c .
Procedure: Start and Test Your Cluster
-
Be sure HBase is not running on any node.
If you forgot to stop HBase from previous testing, you will have errors.
Check to see whether HBase is running on any of your nodes by using the jps command.
Look for the processes HMaster , HRegionServer , and HQuorumPeer .
If they exist, kill them.
-
Start the cluster.
On node-a , issue the start-hbase.sh command.
Your output will be similar to that below.
$ bin/start-hbase.sh
node-c.example.com: starting zookeeper, logging to /home/hbuser/hbase- 0.98 .3 -hadoop2/bin/../logs/hbase-hbuser-zookeeper-node-c.example.com.out
node-a.example.com: starting zookeeper, logging to /home/hbuser/hbase- 0.98 .3 -hadoop2/bin/../logs/hbase-hbuser-zookeeper-node-a.example.com.out
node-b.example.com: starting zookeeper, logging to /home/hbuser/hbase- 0.98 .3 -hadoop2/bin/../logs/hbase-hbuser-zookeeper-node-b.example.com.out
starting master, logging to /home/hbuser/hbase- 0.98 .3 -hadoop2/bin/../logs/hbase-hbuser-master-node-a.example.com.out
node-c.example.com: starting regionserver, logging to /home/hbuser/hbase- 0.98 .3 -hadoop2/bin/../logs/hbase-hbuser-regionserver-node-c.example.com.out
node-b.example.com: starting regionserver, logging to /home/hbuser/hbase- 0.98 .3 -hadoop2/bin/../logs/hbase-hbuser-regionserver-node-b.example.com.out
node-b.example.com: starting master, logging to /home/hbuser/hbase- 0.98 .3 -hadoop2/bin/../logs/hbase-hbuser-master-nodeb.example.com.out
ZooKeeper starts first, followed by the master, then the RegionServers, and finally the backup masters.
-
Verify that the processes are running.
On each node of the cluster, run the jps command and verify that the correct processes are running on each server.
You may see additional Java processes running on your servers as well, if they are used for other purposes.
node-a jps Output
$ jps
20355 Jps
20071 HQuorumPeer
20137 HMaster
node-b jps Output
$ jps
15930 HRegionServer
16194 Jps
15838 HQuorumPeer
16010 HMaster
node-c jps Output
$ jps
13901 Jps
13639 HQuorumPeer
13737 HRegionServer
ZooKeeper Process Name
The HQuorumPeer process is a ZooKeeper instance which is controlled and started by HBase.
If you use ZooKeeper this way, it is limited to one instance per cluster node and is appropriate for testing only.
If ZooKeeper is run outside of HBase, the process is called QuorumPeer .
For more about ZooKeeper configuration, including using an external ZooKeeper instance with HBase, see [zookeeper](#zookeeper) section.
-
Browse to the Web UI.
If everything is set up correctly, you should be able to connect to the UI for the Master
[http://node-a.example.com:16010/](http://node-a.example.com:16010/) or the secondary master at [http://node-b.example.com:16010/](http://node-b.example.com:16010/)
using a web browser.
If you can connect via localhost but not from another host, check your firewall rules.
You can see the web UI for each of the RegionServers at port 16030 of their IP addresses, or by
clicking their links in the web UI for the Master.
-
Test what happens when nodes or services disappear.
With a three-node cluster you have configured, things will not be very resilient.
You can still test the behavior of the primary Master or a RegionServer by killing the associated processes and watching the logs.
### [](#_where_to_go_next)2.5. Where to go next
The next chapter, [configuration](#configuration), gives more information about the different HBase run modes, system requirements for running HBase, and critical configuration areas for setting up a distributed HBase cluster.
# [](#configuration)Apache HBase Configuration
This chapter expands upon the [Getting Started](#getting_started) chapter to further explain configuration of
Apache HBase. Please read this chapter carefully, especially the
[Basic Prerequisites](#basic.prerequisites) to ensure that your HBase testing and deployment goes
smoothly. Familiarize yourself with [Support and Testing Expectations](#hbase_supported_tested_definitions) as well.
## [](#_configuration_files)3. Configuration Files
Apache HBase uses the same configuration system as Apache Hadoop. All configuration files are
located in the conf/ directory, which needs to be kept in sync for each node on your cluster.
HBase Configuration File Descriptions
backup-masters
Not present by default. A plain-text file which lists hosts on which the Master should start a
backup Master process, one host per line.
hadoop-metrics2-hbase.properties
Used to connect HBase Hadoop’s Metrics2 framework.
See the [Hadoop Wiki entry](https://cwiki.apache.org/confluence/display/HADOOP2/HADOOP-6728-MetricsV2)
for more information on Metrics2. Contains only commented-out examples by default.
hbase-env.cmd and hbase-env.sh
Script for Windows and Linux / Unix environments to set up the working environment for HBase,
including the location of Java, Java options, and other environment variables. The file contains
many commented-out examples to provide guidance.
hbase-policy.xml
The default policy configuration file used by RPC servers to make authorization decisions on
client requests. Only used if HBase [security](#security) is enabled.
hbase-site.xml
The main HBase configuration file.
This file specifies configuration options which override HBase’s default configuration.
You can view (but do not edit) the default configuration file at hbase-common/src/main/resources/hbase-default.xml .
You can also view the entire effective configuration for your cluster (defaults and overrides) in
the HBase Configuration tab of the HBase Web UI.
log4j2.properties
Configuration file for HBase logging via log4j2 .
regionservers
A plain-text file containing a list of hosts which should run a RegionServer in your HBase cluster.
By default, this file contains the single entry localhost .
It should contain a list of hostnames or IP addresses, one per line, and should only contain
localhost if each node in your cluster will run a RegionServer on its localhost interface.
Checking XML Validity
When you edit XML, it is a good idea to use an XML-aware editor to be sure that your syntax is
correct and your XML is well-formed. You can also use the xmllint utility to check that your XML
is well-formed. By default, xmllint re-flows and prints the XML to standard output. To check for
well-formedness and only print output if errors exist, use the command xmllint -noout filename.xml .
Keep Configuration In Sync Across the Cluster
When running in distributed mode, after you make an edit to an HBase configuration, make sure you
copy the contents of the conf/ directory to all nodes of the cluster. HBase will not do this for
you. Use a configuration management tool for managing and copying the configuration files to your
nodes. For most configurations, a restart is needed for servers to pick up changes. Dynamic
configuration is an exception to this, to be described later below.
## [](#basic.prerequisites)4. Basic Prerequisites
This section lists required services and some required system configuration.
Java
HBase runs on the Java Virtual Machine, thus all HBase deployments require a JVM runtime.
The following table summarizes the recommendations of the HBase community with respect to running
on various Java versions. The symbol indicates a base level of
testing and willingness to help diagnose and address issues you might run into; these are the
expected deployment combinations. An entry of
means that there may be challenges with this combination, and you should look for more information
before deciding to pursue this as your deployment strategy. The means
this combination does not work; either an older Java version is considered deprecated by the HBase
community, or this combination is known to not work. For combinations of newer JDK with older HBase
releases, it’s likely there are known compatibility issues that cannot be addressed under our
compatibility guarantees, making the combination impossible. In some cases, specific guidance on
limitations (e.g. whether compiling / unit tests work, specific operational issues, etc) are also
noted. Assume any combination not listed here is considered .
Long-Term Support JDKs are Recommended
HBase recommends downstream users rely only on JDK releases that are marked as Long-Term Supported
(LTS), either from the OpenJDK project or vendors. At the time of this writing, the following JDK
releases are NOT LTS releases and are NOT tested or advocated for use by the Apache HBase
community: JDK9, JDK10, JDK12, JDK13, and JDK14. Community discussion around this decision is
recorded on [HBASE-20264](https://issues.apache.org/jira/browse/HBASE-20264).
HotSpot vs. OpenJ9
At this time, all testing performed by the Apache HBase project runs on the HotSpot variant of the
JVM. When selecting your JDK distribution, please take this into consideration.
Table 2. Java support by release line
HBase Version
JDK 6
JDK 7
JDK 8
JDK 11
JDK 17
HBase 2.6
HBase 2.5
*
HBase 2.4
HBase 2.3
*
HBase 2.0-2.2
HBase 1.2+
HBase 1.0-1.1
HBase 0.98
HBase 0.94
A Note on JDK11/JDK17 *
Preliminary support for JDK11 is introduced with HBase 2.3.0, and for JDK17 is introduced with
HBase 2.5.x. We will compile and run test suites with JDK11/17 in pre commit checks and nightly
checks. We will mark the support as as long as we have run some
ITs with the JDK version and also there are users in the community use the JDK version in real
production clusters.
For JDK11/JDK17 support in HBase, please refer to
[HBASE-22972](https://issues.apache.org/jira/browse/HBASE-22972) and
[HBASE-26038](https://issues.apache.org/jira/browse/HBASE-26038)
For JDK11/JDK17 support in Hadoop, which may also affect HBase, please refer to
[HADOOP-15338](https://issues.apache.org/jira/browse/HADOOP-15338) and
[HADOOP-17177](https://issues.apache.org/jira/browse/HADOOP-17177)
You must set JAVA_HOME on each node of your cluster. hbase-env.sh provides a handy
mechanism to do this.
Operating System Utilities
ssh
HBase uses the Secure Shell (ssh) command and utilities extensively to communicate between
cluster nodes. Each server in the cluster must be running ssh so that the Hadoop and HBase
daemons can be managed. You must be able to connect to all nodes via SSH, including the local
node, from the Master as well as any backup Master, using a shared key rather than a password.
You can see the basic methodology for such a set-up in Linux or Unix systems at
"[Procedure: Configure Passwordless SSH Access](#passwordless.ssh.quickstart)". If your cluster nodes use OS X, see the section,
[SSH: Setting up Remote Desktop and Enabling Self-Login](https://cwiki.apache.org/confluence/pages/viewpage.action?pageId=120730246#RunningHadoopOnOSX10.564-bit(Single-NodeCluster)-SSH:SettingupRemoteDesktopandEnablingSelf-Login)
on the Hadoop wiki.
DNS
HBase uses the local hostname to self-report its IP address.
NTP
The clocks on cluster nodes should be synchronized. A small amount of variation is acceptable,
but larger amounts of skew can cause erratic and unexpected behavior. Time synchronization is one
of the first things to check if you see unexplained problems in your cluster. It is recommended
that you run a Network Time Protocol (NTP) service, or another time-synchronization mechanism on
your cluster and that all nodes look to the same service for time synchronization. See the
[Basic NTP Configuration](http://www.tldp.org/LDP/sag/html/basic-ntp-config.html) at
The Linux Documentation Project (TLDP) to set up NTP.
Limits on Number of Files and Processes (ulimit)
Apache HBase is a database. It requires the ability to open a large number of files at once. Many
Linux distributions limit the number of files a single user is allowed to open to 1024 (or 256
on older versions of OS X). You can check this limit on your servers by running the command
ulimit -n when logged in as the user which runs HBase. See
[the Troubleshooting section](#trouble.rs.runtime.filehandles) for some of the problems you may
experience if the limit is too low. You may also notice errors such as the following:
2010 - 04 - 06 03 : 04 : 37 , 542 INFO org.apache.hadoop.hdfs.DFSClient: Exception increateBlockOutputStream java.io.EOFException
2010 - 04 - 06 03 : 04 : 37 , 542 INFO org.apache.hadoop.hdfs.DFSClient: Abandoning block blk_- 6935524980745310745 _1391901
It is recommended to raise the ulimit to at least 10,000, but more likely 10,240, because the value
is usually expressed in multiples of 1024. Each ColumnFamily has at least one StoreFile, and
possibly more than six StoreFiles if the region is under load. The number of open files required
depends upon the number of ColumnFamilies and the number of regions. The following is a rough
formula for calculating the potential number of open files on a RegionServer.
Calculate the Potential Number of Open Files
(StoreFiles per ColumnFamily) x (regions per RegionServer)
For example, assuming that a schema had 3 ColumnFamilies per region with an average of 3 StoreFiles
per ColumnFamily, and there are 100 regions per RegionServer, the JVM will open 3 * 3 * 100 = 900
file descriptors, not counting open JAR files, configuration files, and others. Opening a file does
not take many resources, and the risk of allowing a user to open too many files is minimal.
Another related setting is the number of processes a user is allowed to run at once. In Linux and
Unix, the number of processes is set using the ulimit -u command. This should not be confused
with the nproc command, which controls the number of CPUs available to a given user. Under load,
a ulimit -u that is too low can cause OutOfMemoryError exceptions.
Configuring the maximum number of file descriptors and processes for the user who is running the
HBase process is an operating system configuration, rather than an HBase configuration. It is also
important to be sure that the settings are changed for the user that actually runs HBase. To see
which user started HBase, and that user’s ulimit configuration, look at the first line of the
HBase log for that instance.
Example 1. ulimit Settings on Ubuntu
To configure ulimit settings on Ubuntu, edit /etc/security/limits.conf , which is a
space-delimited file with four columns. Refer to the man page for limits.conf for details about
the format of this file. In the following example, the first line sets both soft and hard limits
for the number of open files (nofile) to 32768 for the operating system user with the username
hadoop. The second line sets the number of processes to 32000 for the same user.
hadoop - nofile 32768
hadoop - nproc 32000
The settings are only applied if the Pluggable Authentication Module (PAM) environment is directed
to use them. To configure PAM to use these limits, be sure that the /etc/pam.d/common-session
file contains the following line:
session required pam_limits.so
Linux Shell
All of the shell scripts that come with HBase rely on the
[GNU Bash](http://www.gnu.org/software/bash) shell.
Windows
Running production systems on Windows machines is not recommended.
### [](#hadoop)4.1. [Hadoop](https://hadoop.apache.org/)
The following table summarizes the versions of Hadoop supported with each version of HBase. Older
versions not appearing in this table are considered unsupported and likely missing necessary
features, while newer versions are untested but may be suitable.
Based on the version of HBase, you should select the most appropriate version of Hadoop. You can
use Apache Hadoop, or a vendor’s distribution of Hadoop. No distinction is made here. See
[the Hadoop wiki](https://cwiki.apache.org/confluence/display/HADOOP2/Distributions+and+Commercial+Support)
for information about vendors of Hadoop.
Hadoop 3.x is recommended.
Comparing to Hadoop 1.x, Hadoop 2.x is faster and includes features, such as short-circuit reads
(see [Leveraging local data](#perf.hdfs.configs.localread)), which will help improve your HBase random read profile.
Hadoop 2.x also includes important bug fixes that will improve your overall HBase experience. HBase
does not support running with earlier versions of Hadoop. See the table below for requirements
specific to different HBase versions.
Today, Hadoop 3.x is recommended as the last Hadoop 2.x release 2.10.2 was released years ago, and
there is no release for Hadoop 2.x for a very long time, although the Hadoop community does not
officially EOL Hadoop 2.x yet.
Use the following legend to interpret these tables:
-
= Tested to be fully-functional
-
= Known to not be fully-functional, or there are
[CVEs](https://hadoop.apache.org/cve_list.html) so we drop the support in newer minor releases
-
= Not tested, may/may-not function
Table 3. Hadoop version support matrix for active release lines
HBase-2.5.x
HBase-2.6.x
Hadoop-2.10.[0-1]
Hadoop-2.10.2+
Hadoop-3.1.0
Hadoop-3.1.1+
Hadoop-3.2.[0-2]
Hadoop-3.2.3+
Hadoop-3.3.[0-1]
Hadoop-3.3.[2-4]
Hadoop-3.3.5+
Hadoop-3.4.0+
(2.5.11+)
(2.6.2+)
Table 4. Hadoop version support matrix for EOM 2.3+ release lines
HBase-2.3.x
HBase-2.4.x
Hadoop-2.10.x
Hadoop-3.1.0
Hadoop-3.1.1+
Hadoop-3.2.x
Hadoop-3.3.x
Table 5. Hadoop version support matrix for EOM 2.x release lines
HBase-2.0.x
HBase-2.1.x
HBase-2.2.x
Hadoop-2.6.1+
Hadoop-2.7.[0-6]
Hadoop-2.7.7+
Hadoop-2.8.[0-2]
Hadoop-2.8.[3-4]
Hadoop-2.8.5+
Hadoop-2.9.[0-1]
Hadoop-2.9.2+
Hadoop-3.0.[0-2]
Hadoop-3.0.3+
Hadoop-3.1.0
Hadoop-3.1.1+
Table 6. Hadoop version support matrix for EOM 1.5+ release lines
HBase-1.5.x
HBase-1.6.x
HBase-1.7.x
Hadoop-2.7.7+
Hadoop-2.8.[0-4]
Hadoop-2.8.5+
Hadoop-2.9.[0-1]
Hadoop-2.9.2+
Hadoop-2.10.x
Table 7. Hadoop version support matrix for EOM 1.x release lines
HBase-1.0.x (Hadoop 1.x is NOT supported)
HBase-1.1.x
HBase-1.2.x
HBase-1.3.x
HBase-1.4.x
Hadoop-2.4.x
Hadoop-2.5.x
Hadoop-2.6.0
Hadoop-2.6.1+
Hadoop-2.7.0
Hadoop-2.7.1+
Table 8. Hadoop version support matrix for EOM pre-1.0 release lines
HBase-0.92.x
HBase-0.94.x
HBase-0.96.x
HBase-0.98.x (Support for Hadoop 1.1+ is deprecated.)
Hadoop-0.20.205
Hadoop-0.22.x
Hadoop-1.0.x
Hadoop-1.1.x
Hadoop-0.23.x
Hadoop-2.0.x-alpha
Hadoop-2.1.0-beta
Hadoop-2.2.0
Hadoop-2.3.x
Hadoop-2.4.x
Hadoop-2.5.x
Hadoop 2.y.0 Releases
Starting around the time of Hadoop version 2.7.0, the Hadoop PMC got into the habit of calling out
new minor releases on their major version 2 release line as not stable / production ready. As such,
HBase expressly advises downstream users to avoid running on top of these releases. Note that
additionally the 2.8.1 release was given the same caveat by the Hadoop PMC. For reference, see the
release announcements for [Apache Hadoop 2.7.0](https://s.apache.org/hadoop-2.7.0-announcement),
[Apache Hadoop 2.8.0](https://s.apache.org/hadoop-2.8.0-announcement),
[Apache Hadoop 2.8.1](https://s.apache.org/hadoop-2.8.1-announcement), and
[Apache Hadoop 2.9.0](https://s.apache.org/hadoop-2.9.0-announcement).
Hadoop 3.1.0 Release
The Hadoop PMC called out the 3.1.0 release as not stable / production ready. As such, HBase
expressly advises downstream users to avoid running on top of this release. For reference, see
the [release announcement for Hadoop 3.1.0](https://s.apache.org/hadoop-3.1.0-announcement).
Replace the Hadoop Bundled With HBase!
Because HBase depends on Hadoop, it bundles Hadoop jars under its lib directory. The bundled jars
are ONLY for use in stand-alone mode. In distributed mode, it is critical that the version of
Hadoop that is out on your cluster match what is under HBase. Replace the hadoop jars found in the
HBase lib directory with the equivalent hadoop jars from the version you are running on your
cluster to avoid version mismatch issues. Make sure you replace the jars under HBase across your
whole cluster. Hadoop version mismatch issues have various manifestations. Check for mismatch if
HBase appears hung.
#### [](#binary_release_hadoop_version)4.1.1. Hadoop 3 Support for the HBase Binary Releases and Maven Artifacts
For HBase 2.5.1 and earlier, the official HBase binary releases and Maven artifacts were built with Hadoop 2.x.
Starting with HBase 2.5.2, HBase provides binary releases and Maven artifacts built with both Hadoop 2.x and Hadoop 3.x.
The Hadoop 2 artifacts do not have any version suffix, the Hadoop 3 artifacts add the -hadoop-3 suffix to the version.
i.e. hbase-2.5.2-bin.tar.gz.asc is the Binary release built with Hadoop2, and hbase-2.5.2-hadoop3-bin.tar.gz is the
release built with Hadoop 3.
#### [](#default_hadoop_version_policy)4.1.2. Hadoop 3 version policy
Each HBase release has a default Hadoop 3 version. This is used when the Hadoop 3 version is not specified during build,
and for building the official binary releases and artifacts. Generally when a new minor version is released
(i.e. 2.5.0) the default version is set to the latest supported Hadoop 3 version at the start of the release
process.
Up to HBase 2.5.10 and 2.6.1 even if HBase added support for newer Hadoop 3 releases in a patch release,
the default Hadoop 3 version (and the one used in the official binary releases) was not updated.
This simplified upgrading, but meant that HBase releases often included old unfixed CVEs both from Hadoop and Hadoop’s
dependencies, even when newer Hadoop releases with fixes were available.
Starting with HBase 2.5.11 and 2.6.2, the default Hadoop 3 version is always set to the latest supported Hadoop 3 version,
and is also used for the -hadoop3 binary releases and artifacts. This will drastically reduce the number of known CVEs
shipped in the HBase binary releases, and make sure that all fixes and improvements in Hadoop are included.
#### [](#dfs.datanode.max.transfer.threads)4.1.3. dfs.datanode.max.transfer.threads
An HDFS DataNode has an upper bound on the number of files that it will serve at any one time.
Before doing any loading, make sure you have configured Hadoop’s conf/hdfs-site.xml , setting the
dfs.datanode.max.transfer.threads value to at least the following:
<property>
<name> dfs.datanode.max.transfer.threads </name>
<value> 4096 </value>
</property>
Be sure to restart your HDFS after making the above configuration.
Not having this configuration in place makes for strange-looking failures.
One manifestation is a complaint about missing blocks.
For example:
10 / 12 / 08 20 : 10 : 31 INFO hdfs.DFSClient: Could not obtain block
blk_XXXXXXXXXXXXXXXXXXXXXX_YYYYYYYY from any node: java.io.IOException: No live nodes
contain current block. Will get new block locations from namenode and retry...
See also [casestudies.max.transfer.threads](#casestudies.max.transfer.threads) and note that this
property was previously known as dfs.datanode.max.xcievers (e.g.
[Hadoop HDFS: Deceived by Xciever](http://ccgtech.blogspot.com/2010/02/hadoop-hdfs-deceived-by-xciever.html)).
### [](#zookeeper.requirements)4.2. ZooKeeper Requirements
An Apache ZooKeeper quorum is required. The exact version depends on your version of HBase, though
the minimum ZooKeeper version is 3.4.x due to the useMulti feature made default in 1.0.0
(see [HBASE-16598](https://issues.apache.org/jira/browse/HBASE-16598)).
## [](#standalone_dist)5. HBase run modes: Standalone and Distributed
HBase has two run modes: [standalone](#standalone) and [distributed](#distributed).
Out of the box, HBase runs in standalone mode.
Whatever your mode, you will need to configure HBase by editing files in the HBase conf directory.
At a minimum, you must edit conf/hbase-env.sh to tell HBase which java to use.
In this file you set HBase environment variables such as the heapsize and other options for the
JVM , the preferred location for log files, etc. Set JAVA_HOME to point at the root of
your java install.
### [](#standalone)5.1. Standalone HBase
This is the default mode.
Standalone mode is what is described in the [quickstart](#quickstart) section.
In standalone mode, HBase does not use HDFS — it uses the local filesystem instead — and it runs
all HBase daemons and a local ZooKeeper all up in the same JVM. ZooKeeper binds to a well-known
port so clients may talk to HBase.
#### [](#standalone.over.hdfs)5.1.1. Standalone HBase over HDFS
A sometimes useful variation on standalone hbase has all daemons running inside the
one JVM but rather than persist to the local filesystem, instead
they persist to an HDFS instance.
You might consider this profile when you are intent on
a simple deploy profile, the loading is light, but the
data must persist across node comings and goings. Writing to
HDFS where data is replicated ensures the latter.
To configure this standalone variant, edit your hbase-site.xml
setting hbase.rootdir to point at a directory in your
HDFS instance but then set hbase.cluster.distributed
to false . For example:
<configuration>
<property>
<name> hbase.rootdir </name>
<value> hdfs://namenode.example.org:9000/hbase </value>
</property>
<property>
<name> hbase.cluster.distributed </name>
<value> false </value>
</property>
</configuration>
### [](#distributed)5.2. Distributed
Distributed mode can be subdivided into distributed but all daemons run on a single node — a.k.a.
pseudo-distributed  — and fully-distributed where the daemons are spread across all nodes in
the cluster. The pseudo-distributed vs. fully-distributed nomenclature comes from Hadoop.
Pseudo-distributed mode can run against the local filesystem or it can run against an instance of
the Hadoop Distributed File System (HDFS). Fully-distributed mode can ONLY run on HDFS.
See the Hadoop [documentation](https://hadoop.apache.org/docs/current/) for how to set up HDFS.
A good walk-through for setting up HDFS on Hadoop 2 can be found at
[https://web.archive.org/web/20221007121526/https://www.alexjf.net/blog/distributed-systems/hadoop-yarn-installation-definitive-guide/](https://web.archive.org/web/20221007121526/https://www.alexjf.net/blog/distributed-systems/hadoop-yarn-installation-definitive-guide/).
#### [](#pseudo)5.2.1. Pseudo-distributed
Pseudo-Distributed Quickstart
A quickstart has been added to the [quickstart](#quickstart) chapter.
See [quickstart-pseudo](#quickstart_pseudo).
Some of the information that was originally in this section has been moved there.
A pseudo-distributed mode is simply a fully-distributed mode run on a single host.
Use this HBase configuration for testing and prototyping purposes only.
Do not use this configuration for production or for performance evaluation.
### [](#fully_dist)5.3. Fully-distributed
By default, HBase runs in stand-alone mode. Both stand-alone mode and pseudo-distributed mode are
provided for the purposes of small-scale testing. For a production environment, distributed mode
is advised. In distributed mode, multiple instances of HBase daemons run on multiple servers in the
cluster.
Just as in pseudo-distributed mode, a fully distributed configuration requires that you set the
hbase.cluster.distributed property to true . Typically, the hbase.rootdir is configured to
point to a highly-available HDFS filesystem.
In addition, the cluster is configured so that multiple cluster nodes enlist as RegionServers,
ZooKeeper QuorumPeers, and backup HMaster servers. These configuration basics are all demonstrated
in [quickstart-fully-distributed](#quickstart_fully_distributed).
Distributed RegionServers
Typically, your cluster will contain multiple RegionServers all running on different servers, as
well as primary and backup Master and ZooKeeper daemons. The conf/regionservers file on the
master server contains a list of hosts whose RegionServers are associated with this cluster.
Each host is on a separate line. All hosts listed in this file will have their RegionServer
processes started and stopped when the
master server starts or stops.
ZooKeeper and HBase
See the [ZooKeeper](#zookeeper) section for ZooKeeper setup instructions for HBase.
Example 2. Example Distributed HBase Cluster
This is a bare-bones conf/hbase-site.xml for a distributed HBase cluster.
A cluster that is used for real-world work would contain more custom configuration parameters.
Most HBase configuration directives have default values, which are used unless the value is
overridden in the hbase-site.xml . See "[Configuration Files](#config.files)" for more information.
<configuration>
<property>
<name> hbase.rootdir </name>
<value> hdfs://namenode.example.org:9000/hbase </value>
</property>
<property>
<name> hbase.cluster.distributed </name>
<value> true </value>
</property>
<property>
<name> hbase.zookeeper.quorum </name>
<value> node-a.example.com,node-b.example.com,node-c.example.com </value>
</property>
</configuration>
This is an example conf/regionservers file, which contains a list of nodes that should run a
RegionServer in the cluster. These nodes need HBase installed and they need to use the same
contents of the conf/ directory as the Master server.
node-a.example.com
node-b.example.com
node-c.example.com
This is an example conf/backup-masters file, which contains a list of each node that should run
a backup Master instance. The backup Master instances will sit idle unless the main Master becomes
unavailable.
node-b.example.com
node-c.example.com
Distributed HBase Quickstart
See [quickstart-fully-distributed](#quickstart_fully_distributed) for a walk-through of a simple
three-node cluster configuration with multiple ZooKeeper, backup HMaster, and RegionServer
instances.
Procedure: HDFS Client Configuration
-
Of note, if you have made HDFS client configuration changes on your Hadoop cluster, such as
configuration directives for HDFS clients, as opposed to server-side configurations, you must use
one of the following methods to enable HBase to see and use these configuration changes:
-
Add a pointer to your HADOOP_CONF_DIR to the HBASE_CLASSPATH environment variable in
hbase-env.sh .
-
Add a copy of hdfs-site.xml (or hadoop-site.xml ) or, better, symlinks, under
${HBASE_HOME}/conf , or
-
if only a small set of HDFS client configurations, add them to hbase-site.xml .
An example of such an HDFS client configuration is dfs.replication .
If for example, you want to run with a replication factor of 5, HBase will create files with the
default of 3 unless you do the above to make the configuration available to HBase.
### [](#byo-hadoop-assembly)5.4. Choosing between the Classic Package and the BYO Hadoop Package
Starting with HBase 3.0, HBase includes two binary packages. The classic package
includes both the HBase and Hadoop components, while the Hadoop-less "Bring Your Own Hadoop"
package omits the Hadoop components, and uses the files from an existing Hadoop installation.
The classic binary package filename is named hbase-<version>-bin.tar.gz i.e.
hbase-3.0.0-bin.tar.gz , while the Hadoop-less package is
hbase-byo-hadoop-<version>-bin.tar.gz i.e. hbase-byo-hadoop-3.0.0-bin.tar.gz .
If the cluster nodes already have Hadoop installed, you can use the Hadoop-less package.
In this case you need to make sure that the HADOOP_HOME environment variable is set and
points to the Hadoop installation.
The easiest way to ensure this is to set it in hbase-env.sh . You still need to make sure that
the Hadoop configuration files are present on the HBase classpath, as described above.
Advantages of the BYO Hadoop package
-
There is no need to replace the Hadoop libraries, as noted [above](#note_replace_hadoop).
-
It is easier to upgrade Hadoop and HBase independently (as long as compatible versions are used).
-
Both the package and installed size are about 100 MB smaller.
## [](#confirm)6. Running and Confirming Your Installation
Make sure HDFS is running first.
Start and stop the Hadoop HDFS daemons by running bin/start-hdfs.sh over in the HADOOP_HOME
directory. You can ensure it started properly by testing the put and get of files into the
Hadoop filesystem. HBase does not normally use the MapReduce or YARN daemons. These do not need to
be started.
If you are managing your own ZooKeeper, start it and confirm it’s running, else HBase will start
up ZooKeeper for you as part of its start process.
Start HBase with the following command:
bin/start-hbase.sh
Run the above from the HBASE_HOME directory.
You should now have a running HBase instance.
HBase logs can be found in the logs subdirectory.
Check them out especially if HBase had trouble starting.
HBase also puts up a UI listing vital attributes.
By default it’s deployed on the Master host at port 16010 (HBase RegionServers listen on port 16020
by default and put up an informational HTTP server at port 16030). If the Master is running on a
host named master.example.org on the default port, point your browser at
http://master.example.org:16010 to see the web interface.
Once HBase has started, see the [shell exercises](#shell_exercises) section for how to create
tables, add data, scan your insertions, and finally disable and drop your tables.
To stop HBase after exiting the HBase shell enter
$ ./bin/stop-hbase.sh
stopping hbase...............
Shutdown can take a moment to complete.
It can take longer if your cluster is comprised of many machines.
If you are running a distributed operation, be sure to wait until HBase has shut down completely
before stopping the Hadoop daemons.
## [](#config.files)7. Default Configuration
### [](#hbase.site)7.1. hbase-site.xml and hbase-default.xml
Just as in Hadoop where you add site-specific HDFS configuration to the hdfs-site.xml file, for
HBase, site specific customizations go into the file conf/hbase-site.xml . For the list of
configurable properties, see [hbase default configurations](#hbase_default_configurations) below
or view the raw hbase-default.xml source file in the HBase source code at src/main/resources .
Not all configuration options make it out to hbase-default.xml .
Some configurations would only appear in source code; the only way to identify these changes are
through code review.
Currently, changes here will require a cluster restart for HBase to notice the change.
### [](#hbase_default_configurations)7.2. HBase Default Configuration
The documentation below is generated using the default hbase configuration file, hbase-default.xml , as source.
hbase.tmp.dir
Description
Temporary directory on the local filesystem. Change this setting to point to a location more permanent than '/tmp', the usual resolve for java.io.tmpdir, as the '/tmp' directory is cleared on machine restart.
Default
${java.io.tmpdir}/hbase-${user.name}
hbase.rootdir
Description
The directory shared by region servers and into which HBase persists. The URL should be 'fully-qualified' to include the filesystem scheme. For example, to specify the HDFS directory '/hbase' where the HDFS instance’s namenode is running at namenode.example.org on port 9000, set this value to: hdfs://namenode.example.org:9000/hbase. By default, we write to whatever ${hbase.tmp.dir} is set too — usually /tmp — so change this configuration or else all data will be lost on machine restart.
Default
${hbase.tmp.dir}/hbase
hbase.cluster.distributed
Description
The mode the cluster will be in. Possible values are false for standalone mode and true for distributed mode. If false, startup will run all HBase and ZooKeeper daemons together in the one JVM.
Default
false
hbase.zookeeper.quorum
Description
Comma separated list of servers in the ZooKeeper ensemble (This config. should have been named hbase.zookeeper.ensemble). For example, "host1.mydomain.com,host2.mydomain.com,host3.mydomain.com". By default this is set to localhost for local and pseudo-distributed modes of operation. For a fully-distributed setup, this should be set to a full list of ZooKeeper ensemble servers. If HBASE_MANAGES_ZK is set in hbase-env.sh this is the list of servers which hbase will start/stop ZooKeeper on as part of cluster start/stop. Client-side, we will take this list of ensemble members and put it together with the hbase.zookeeper.property.clientPort config. and pass it into zookeeper constructor as the connectString parameter.
Default
127.0.0.1
zookeeper.recovery.retry.maxsleeptime
Description
Max sleep time before retry zookeeper operations in milliseconds, a max time is needed here so that sleep time won’t grow unboundedly
Default
60000
hbase.local.dir
Description
Directory on the local filesystem to be used as a local storage.
Default
${hbase.tmp.dir}/local/
hbase.master.port
Description
The port the HBase Master should bind to.
Default
16000
hbase.master.info.port
Description
The port for the HBase Master web UI. Set to -1 if you do not want a UI instance run.
Default
16010
hbase.master.info.bindAddress
Description
The bind address for the HBase Master web UI
Default
0.0.0.0
hbase.master.logcleaner.plugins
Description
A comma-separated list of BaseLogCleanerDelegate invoked by the LogsCleaner service. These WAL cleaners are called in order, so put the cleaner that prunes the most files in front. To implement your own BaseLogCleanerDelegate, just put it in HBase’s classpath and add the fully qualified class name here. Always add the above default log cleaners in the list.
Default
org.apache.hadoop.hbase.master.cleaner.TimeToLiveLogCleaner,org.apache.hadoop.hbase.master.cleaner.TimeToLiveProcedureWALCleaner,org.apache.hadoop.hbase.master.cleaner.TimeToLiveMasterLocalStoreWALCleaner
hbase.master.logcleaner.ttl
Description
How long a WAL remain in the archive ({hbase.rootdir}/oldWALs) directory, after which it will be cleaned by a Master thread. The value is in milliseconds.
Default
600000
hbase.master.hfilecleaner.plugins
Description
A comma-separated list of BaseHFileCleanerDelegate invoked by the HFileCleaner service. These HFiles cleaners are called in order, so put the cleaner that prunes the most files in front. To implement your own BaseHFileCleanerDelegate, just put it in HBase’s classpath and add the fully qualified class name here. Always add the above default hfile cleaners in the list as they will be overwritten in hbase-site.xml.
Default
org.apache.hadoop.hbase.master.cleaner.TimeToLiveHFileCleaner,org.apache.hadoop.hbase.master.cleaner.TimeToLiveMasterLocalStoreHFileCleaner
hbase.master.infoserver.redirect
Description
Whether or not the Master listens to the Master web UI port (hbase.master.info.port) and redirects requests to the web UI server shared by the Master and RegionServer. Config. makes sense when Master is serving Regions (not the default).
Default
true
hbase.master.fileSplitTimeout
Description
Splitting a region, how long to wait on the file-splitting step before aborting the attempt. Default: 600000. This setting used to be known as hbase.regionserver.fileSplitTimeout in hbase-1.x. Split is now run master-side hence the rename (If a 'hbase.master.fileSplitTimeout' setting found, will use it to prime the current 'hbase.master.fileSplitTimeout' Configuration.
Default
600000
hbase.regionserver.port
Description
The port the HBase RegionServer binds to.
Default
16020
hbase.regionserver.info.port
Description
The port for the HBase RegionServer web UI Set to -1 if you do not want the RegionServer UI to run.
Default
16030
hbase.regionserver.info.bindAddress
Description
The address for the HBase RegionServer web UI
Default
0.0.0.0
hbase.regionserver.info.port.auto
Description
Whether or not the Master or RegionServer UI should search for a port to bind to. Enables automatic port search if hbase.regionserver.info.port is already in use. Useful for testing, turned off by default.
Default
false
hbase.regionserver.handler.count
Description
Count of RPC Listener instances spun up on RegionServers. Same property is used by the Master for count of master handlers. Too many handlers can be counter-productive. Make it a multiple of CPU count. If mostly read-only, handlers count close to cpu count does well. Start with twice the CPU count and tune from there.
Default
30
hbase.ipc.server.callqueue.handler.factor
Description
Factor to determine the number of call queues. A value of 0 means a single queue shared between all the handlers. A value of 1 means that each handler has its own queue.
Default
0.1
hbase.ipc.server.callqueue.read.ratio
Description
Split the call queues into read and write queues. The specified interval (which should be between 0.0 and 1.0) will be multiplied by the number of call queues. A value of 0 indicate to not split the call queues, meaning that both read and write requests will be pushed to the same set of queues. A value lower than 0.5 means that there will be less read queues than write queues. A value of 0.5 means there will be the same number of read and write queues. A value greater than 0.5 means that there will be more read queues than write queues. A value of 1.0 means that all the queues except one are used to dispatch read requests. Example: Given the total number of call queues being 10 a read.ratio of 0 means that: the 10 queues will contain both read/write requests. a read.ratio of 0.3 means that: 3 queues will contain only read requests and 7 queues will contain only write requests. a read.ratio of 0.5 means that: 5 queues will contain only read requests and 5 queues will contain only write requests. a read.ratio of 0.8 means that: 8 queues will contain only read requests and 2 queues will contain only write requests. a read.ratio of 1 means that: 9 queues will contain only read requests and 1 queues will contain only write requests.
Default
0
hbase.ipc.server.callqueue.scan.ratio
Description
Given the number of read call queues, calculated from the total number of call queues multiplied by the callqueue.read.ratio, the scan.ratio property will split the read call queues into small-read and long-read queues. A value lower than 0.5 means that there will be less long-read queues than short-read queues. A value of 0.5 means that there will be the same number of short-read and long-read queues. A value greater than 0.5 means that there will be more long-read queues than short-read queues A value of 0 or 1 indicate to use the same set of queues for gets and scans. Example: Given the total number of read call queues being 8 a scan.ratio of 0 or 1 means that: 8 queues will contain both long and short read requests. a scan.ratio of 0.3 means that: 2 queues will contain only long-read requests and 6 queues will contain only short-read requests. a scan.ratio of 0.5 means that: 4 queues will contain only long-read requests and 4 queues will contain only short-read requests. a scan.ratio of 0.8 means that: 6 queues will contain only long-read requests and 2 queues will contain only short-read requests.
Default
0
hbase.regionserver.msginterval
Description
Interval between messages from the RegionServer to Master in milliseconds.
Default
3000
hbase.regionserver.logroll.period
Description
Period at which we will roll the commit log regardless of how many edits it has.
Default
3600000
hbase.regionserver.logroll.errors.tolerated
Description
The number of consecutive WAL close errors we will allow before triggering a server abort. A setting of 0 will cause the region server to abort if closing the current WAL writer fails during log rolling. Even a small value (2 or 3) will allow a region server to ride over transient HDFS errors.
Default
2
hbase.regionserver.free.heap.min.memory.size
Description
Defines the minimum amount of heap memory that must remain free for the RegionServer to start, specified in bytes or human-readable formats like '512m' for megabytes or '4g' for gigabytes. If not set, the default is 20% of the total heap size. To disable the check entirely, set this value to 0. If the combined memory usage of memstore and block cache exceeds (total heap - this value), the RegionServer will fail to start.
Default
none
hbase.regionserver.global.memstore.size
Description
Maximum size of all memstores in a region server before new updates are blocked and flushes are forced. Defaults to 40% of heap (0.4). Updates are blocked and flushes are forced until size of all memstores in a region server hits hbase.regionserver.global.memstore.size.lower.limit. The default value in this configuration has been intentionally left empty in order to honor the old hbase.regionserver.global.memstore.upperLimit property if present.
Default
none
hbase.regionserver.global.memstore.size.lower.limit
Description
Maximum size of all memstores in a region server before flushes are forced. Defaults to 95% of hbase.regionserver.global.memstore.size (0.95). A 100% value for this value causes the minimum possible flushing to occur when updates are blocked due to memstore limiting. The default value in this configuration has been intentionally left empty in order to honor the old hbase.regionserver.global.memstore.lowerLimit property if present.
Default
none
hbase.systemtables.compacting.memstore.type
Description
Determines the type of memstore to be used for system tables like META, namespace tables etc. By default NONE is the type and hence we use the default memstore for all the system tables. If we need to use compacting memstore for system tables then set this property to BASIC/EAGER
Default
NONE
hbase.regionserver.optionalcacheflushinterval
Description
Maximum amount of time an edit lives in memory before being automatically flushed. Default 1 hour. Set it to 0 to disable automatic flushing.
Default
3600000
hbase.regionserver.dns.interface
Description
The name of the Network Interface from which a region server should report its IP address.
Default
default
hbase.regionserver.dns.nameserver
Description
The host name or IP address of the name server (DNS) which a region server should use to determine the host name used by the master for communication and display purposes.
Default
default
hbase.regionserver.region.split.policy
Description
A split policy determines when a region should be split. The various other split policies that are available currently are BusyRegionSplitPolicy, ConstantSizeRegionSplitPolicy, DisabledRegionSplitPolicy, DelimitedKeyPrefixRegionSplitPolicy, KeyPrefixRegionSplitPolicy, and SteppingSplitPolicy. DisabledRegionSplitPolicy blocks manual region splitting.
Default
org.apache.hadoop.hbase.regionserver.SteppingSplitPolicy
hbase.regionserver.regionSplitLimit
Description
Limit for the number of regions after which no more region splitting should take place. This is not hard limit for the number of regions but acts as a guideline for the regionserver to stop splitting after a certain limit. Default is set to 1000.
Default
1000
zookeeper.session.timeout
Description
ZooKeeper session timeout in milliseconds. It is used in two different ways. First, this value is used in the ZK client that HBase uses to connect to the ensemble. It is also used by HBase when it starts a ZK server and it is passed as the 'maxSessionTimeout'. See [https://zookeeper.apache.org/doc/current/zookeeperProgrammers.html#ch_zkSessions](https://zookeeper.apache.org/doc/current/zookeeperProgrammers.html#ch_zkSessions). For example, if an HBase region server connects to a ZK ensemble that’s also managed by HBase, then the session timeout will be the one specified by this configuration. But, a region server that connects to an ensemble managed with a different configuration will be subjected that ensemble’s maxSessionTimeout. So, even though HBase might propose using 90 seconds, the ensemble can have a max timeout lower than this and it will take precedence. The current default maxSessionTimeout that ZK ships with is 40 seconds, which is lower than HBase’s.
Default
90000
zookeeper.znode.parent
Description
Root ZNode for HBase in ZooKeeper. All of HBase’s ZooKeeper files that are configured with a relative path will go under this node. By default, all of HBase’s ZooKeeper file paths are configured with a relative path, so they will all go under this directory unless changed.
Default
/hbase
zookeeper.znode.acl.parent
Description
Root ZNode for access control lists.
Default
acl
hbase.zookeeper.dns.interface
Description
The name of the Network Interface from which a ZooKeeper server should report its IP address.
Default
default
hbase.zookeeper.dns.nameserver
Description
The host name or IP address of the name server (DNS) which a ZooKeeper server should use to determine the host name used by the master for communication and display purposes.
Default
default
hbase.zookeeper.peerport
Description
Port used by ZooKeeper peers to talk to each other. See [https://zookeeper.apache.org/doc/r3.4.10/zookeeperStarted.html#sc_RunningReplicatedZooKeeper](https://zookeeper.apache.org/doc/r3.4.10/zookeeperStarted.html#sc_RunningReplicatedZooKeeper) for more information.
Default
2888
hbase.zookeeper.leaderport
Description
Port used by ZooKeeper for leader election. See [https://zookeeper.apache.org/doc/r3.4.10/zookeeperStarted.html#sc_RunningReplicatedZooKeeper](https://zookeeper.apache.org/doc/r3.4.10/zookeeperStarted.html#sc_RunningReplicatedZooKeeper) for more information.
Default
3888
hbase.zookeeper.property.initLimit
Description
Property from ZooKeeper’s config zoo.cfg. The number of ticks that the initial synchronization phase can take.
Default
10
hbase.zookeeper.property.syncLimit
Description
Property from ZooKeeper’s config zoo.cfg. The number of ticks that can pass between sending a request and getting an acknowledgment.
Default
5
hbase.zookeeper.property.dataDir
Description
Property from ZooKeeper’s config zoo.cfg. The directory where the snapshot is stored.
Default
${hbase.tmp.dir}/zookeeper
hbase.zookeeper.property.clientPort
Description
Property from ZooKeeper’s config zoo.cfg. The port at which the clients will connect.
Default
2181
hbase.zookeeper.property.maxClientCnxns
Description
Property from ZooKeeper’s config zoo.cfg. Limit on number of concurrent connections (at the socket level) that a single client, identified by IP address, may make to a single member of the ZooKeeper ensemble. Set high to avoid zk connection issues running standalone and pseudo-distributed.
Default
300
hbase.client.write.buffer
Description
Default size of the BufferedMutator write buffer in bytes. A bigger buffer takes more memory — on both the client and server side since server instantiates the passed write buffer to process it — but a larger buffer size reduces the number of RPCs made. For an estimate of server-side memory-used, evaluate hbase.client.write.buffer * hbase.regionserver.handler.count
Default
2097152
hbase.client.pause
Description
General client pause value. Used mostly as value to wait before running a retry of a failed get, region lookup, etc. See hbase.client.retries.number for description of how we backoff from this initial pause amount and how this pause works w/ retries.
Default
100
hbase.client.pause.server.overloaded
Description
Pause time when encountering an exception indicating a server is overloaded, CallQueueTooBigException or CallDroppedException. Set this property to a higher value than hbase.client.pause if you observe frequent CallQueueTooBigException or CallDroppedException from the same RegionServer and the call queue there keeps filling up. This config used to be called hbase.client.pause.cqtbe, which has been deprecated as of 2.5.0.
Default
none
hbase.client.retries.number
Description
Maximum retries. Used as maximum for all retryable operations such as the getting of a cell’s value, starting a row update, etc. Retry interval is a rough function based on hbase.client.pause. At first we retry at this interval but then with backoff, we pretty quickly reach retrying every ten seconds. See HConstants#RETRY_BACKOFF for how the backup ramps up. Change this setting and hbase.client.pause to suit your workload.
Default
15
hbase.client.max.total.tasks
Description
The maximum number of concurrent mutation tasks a single HTable instance will send to the cluster.
Default
100
hbase.client.max.perserver.tasks
Description
The maximum number of concurrent mutation tasks a single HTable instance will send to a single region server.
Default
2
hbase.client.max.perregion.tasks
Description
The maximum number of concurrent mutation tasks the client will maintain to a single Region. That is, if there is already hbase.client.max.perregion.tasks writes in progress for this region, new puts won’t be sent to this region until some writes finishes.
Default
1
hbase.client.perserver.requests.threshold
Description
The max number of concurrent pending requests for one server in all client threads (process level). Exceeding requests will be thrown ServerTooBusyException immediately to prevent user’s threads being occupied and blocked by only one slow region server. If you use a fix number of threads to access HBase in a synchronous way, set this to a suitable value which is related to the number of threads will help you. See [https://issues.apache.org/jira/browse/HBASE-16388](https://issues.apache.org/jira/browse/HBASE-16388) for details.
Default
2147483647
hbase.client.scanner.caching
Description
Number of rows that we try to fetch when calling next on a scanner if it is not served from (local, client) memory. This configuration works together with hbase.client.scanner.max.result.size to try and use the network efficiently. The default value is Integer.MAX_VALUE by default so that the network will fill the chunk size defined by hbase.client.scanner.max.result.size rather than be limited by a particular number of rows since the size of rows varies table to table. If you know ahead of time that you will not require more than a certain number of rows from a scan, this configuration should be set to that row limit via Scan#setCaching. Higher caching values will enable faster scanners but will eat up more memory and some calls of next may take longer and longer times when the cache is empty. Do not set this value such that the time between invocations is greater than the scanner timeout; i.e. hbase.client.scanner.timeout.period
Default
2147483647
hbase.client.keyvalue.maxsize
Description
Specifies the combined maximum allowed size of a KeyValue instance. This is to set an upper boundary for a single entry saved in a storage file. Since they cannot be split it helps avoiding that a region cannot be split any further because the data is too large. It seems wise to set this to a fraction of the maximum region size. Setting it to zero or less disables the check.
Default
10485760
hbase.server.keyvalue.maxsize
Description
Maximum allowed size of an individual cell, inclusive of value and all key components. A value of 0 or less disables the check. The default value is 10MB. This is a safety setting to protect the server from OOM situations.
Default
10485760
hbase.client.scanner.timeout.period
Description
Client scanner lease period in milliseconds.
Default
60000
hbase.client.localityCheck.threadPoolSize
Default
2
hbase.bulkload.retries.number
Description
Maximum retries. This is maximum number of iterations to atomic bulk loads are attempted in the face of splitting operations 0 means never give up.
Default
10
hbase.compaction.after.bulkload.enable
Description
Request Compaction after bulkload immediately. If bulkload is continuous, the triggered compactions may increase load, bring about performance side effect.
Default
false
hbase.master.balancer.maxRitPercent
Description
The max percent of regions in transition when balancing. The default value is 1.0. So there are no balancer throttling. If set this config to 0.01, It means that there are at most 1% regions in transition when balancing. Then the cluster’s availability is at least 99% when balancing.
Default
1.0
hbase.balancer.period
Description
Period at which the region balancer runs in the Master, in milliseconds.
Default
300000
hbase.master.oldwals.dir.updater.period
Description
Period at which the oldWALs directory size calculator/updater will run in the Master, in milliseconds.
Default
300000
hbase.regions.slop
Description
The load balancer can trigger for several reasons. This value controls one of those reasons. Run the balancer if any regionserver has a region count outside the range of average +/- (average * slop) regions. If the value of slop is negative, disable sloppiness checks. The balancer can still run for other reasons, but sloppiness will not be one of them. If the value of slop is 0, run the balancer if any server has a region count more than 1 from the average. If the value of slop is 100, run the balancer if any server has a region count greater than 101 times the average. The default value of this parameter is 0.2, which runs the balancer if any server has a region count less than 80% of the average, or greater than 120% of the average. Note that for the default StochasticLoadBalancer, this does not guarantee any balancing actions will be taken, but only that the balancer will attempt to run.
Default
0.2
hbase.normalizer.period
Description
Period at which the region normalizer runs in the Master, in milliseconds.
Default
300000
hbase.normalizer.split.enabled
Description
Whether to split a region as part of normalization.
Default
true
hbase.normalizer.merge.enabled
Description
Whether to merge a region as part of normalization.
Default
true
hbase.normalizer.merge.min.region.count
Description
The minimum number of regions in a table to consider it for merge normalization.
Default
3
hbase.normalizer.merge.min_region_age.days
Description
The minimum age for a region to be considered for a merge, in days.
Default
3
hbase.normalizer.merge.min_region_size.mb
Description
The minimum size for a region to be considered for a merge, in whole MBs.
Default
1
hbase.normalizer.merge.merge_request_max_number_of_regions
Description
The maximum number of region count in a merge request for merge normalization.
Default
100
hbase.table.normalization.enabled
Description
This config is used to set default behaviour of normalizer at table level. To override this at table level one can set NORMALIZATION_ENABLED at table descriptor level and that property will be honored
Default
false
hbase.server.thread.wakefrequency
Description
In master side, this config is the period used for FS related behaviors: checking if hdfs is out of safe mode, setting or checking hbase.version file, setting or checking hbase.id file. Using default value should be fine. In regionserver side, this config is used in several places: flushing check interval, compaction check interval, wal rolling check interval. Specially, admin can tune flushing and compaction check interval by hbase.regionserver.flush.check.period and hbase.regionserver.compaction.check.period. (in milliseconds)
Default
10000
hbase.regionserver.flush.check.period
Description
It determines the flushing check period of PeriodicFlusher in regionserver. If unset, it uses hbase.server.thread.wakefrequency as default value. (in milliseconds)
Default
${hbase.server.thread.wakefrequency}
hbase.regionserver.compaction.check.period
Description
It determines the compaction check period of CompactionChecker in regionserver. If unset, it uses hbase.server.thread.wakefrequency as default value. (in milliseconds)
Default
${hbase.server.thread.wakefrequency}
hbase.server.versionfile.writeattempts
Description
How many times to retry attempting to write a version file before just aborting. Each attempt is separated by the hbase.server.thread.wakefrequency milliseconds.
Default
3
hbase.hregion.memstore.flush.size
Description
Memstore will be flushed to disk if size of the memstore exceeds this number of bytes. Value is checked by a thread that runs every hbase.server.thread.wakefrequency.
Default
134217728
hbase.hregion.percolumnfamilyflush.size.lower.bound.min
Description
If FlushLargeStoresPolicy is used and there are multiple column families, then every time that we hit the total memstore limit, we find out all the column families whose memstores exceed a "lower bound" and only flush them while retaining the others in memory. The "lower bound" will be "hbase.hregion.memstore.flush.size / column_family_number" by default unless value of this property is larger than that. If none of the families have their memstore size more than lower bound, all the memstores will be flushed (just as usual).
Default
16777216
hbase.hregion.preclose.flush.size
Description
If the memstores in a region are this size or larger when we go to close, run a "pre-flush" to clear out memstores before we put up the region closed flag and take the region offline. On close, a flush is run under the close flag to empty memory. During this time the region is offline and we are not taking on any writes. If the memstore content is large, this flush could take a long time to complete. The preflush is meant to clean out the bulk of the memstore before putting up the close flag and taking the region offline so the flush that runs under the close flag has little to do.
Default
5242880
hbase.hregion.memstore.block.multiplier
Description
Block updates if memstore has hbase.hregion.memstore.block.multiplier times hbase.hregion.memstore.flush.size bytes. Useful preventing runaway memstore during spikes in update traffic. Without an upper-bound, memstore fills such that when it flushes the resultant flush files take a long time to compact or split, or worse, we OOME.
Default
4
hbase.hregion.memstore.mslab.enabled
Description
Enables the MemStore-Local Allocation Buffer, a feature which works to prevent heap fragmentation under heavy write loads. This can reduce the frequency of stop-the-world GC pauses on large heaps.
Default
true
hbase.hregion.memstore.mslab.chunksize
Description
The maximum byte size of a chunk in the MemStoreLAB. Unit: bytes
Default
2097152
hbase.regionserver.offheap.global.memstore.size
Description
The amount of off-heap memory all MemStores in a RegionServer may use. A value of 0 means that no off-heap memory will be used and all chunks in MSLAB will be HeapByteBuffer, otherwise the non-zero value means how many megabyte of off-heap memory will be used for chunks in MSLAB and all chunks in MSLAB will be DirectByteBuffer. Unit: megabytes.
Default
0
hbase.hregion.memstore.mslab.max.allocation
Description
The maximal size of one allocation in the MemStoreLAB, if the desired byte size exceed this threshold then it will be just allocated from JVM heap rather than MemStoreLAB.
Default
262144
hbase.hregion.max.filesize
Description
Maximum file size. If the sum of the sizes of a region’s HFiles has grown to exceed this value, the region is split in two. There are two choices of how this option works, the first is when any store’s size exceed the threshold then split, and the other is overall region’s size exceed the threshold then split, it can be configed by hbase.hregion.split.overallfiles.
Default
10737418240
hbase.hregion.split.overallfiles
Description
If we should sum overall region files size when check to split.
Default
true
hbase.hregion.majorcompaction
Description
Time between major compactions, expressed in milliseconds. Set to 0 to disable time-based automatic major compactions. User-requested and size-based major compactions will still run. This value is multiplied by hbase.hregion.majorcompaction.jitter to cause compaction to start at a somewhat-random time during a given window of time. The default value is 7 days, expressed in milliseconds. If major compactions are causing disruption in your environment, you can configure them to run at off-peak times for your deployment, or disable time-based major compactions by setting this parameter to 0, and run major compactions in a cron job or by another external mechanism.
Default
604800000
hbase.hregion.majorcompaction.jitter
Description
A multiplier applied to hbase.hregion.majorcompaction to cause compaction to occur a given amount of time either side of hbase.hregion.majorcompaction. The smaller the number, the closer the compactions will happen to the hbase.hregion.majorcompaction interval.
Default
0.50
hbase.hstore.compactionThreshold
Description
If more than or equal to this number of StoreFiles exist in any one Store (one StoreFile is written per flush of MemStore), a compaction is run to rewrite all StoreFiles into a single StoreFile. Larger values delay compaction, but when compaction does occur, it takes longer to complete.
Default
3
hbase.regionserver.compaction.enabled
Description
Enable/disable compactions on by setting true/false. We can further switch compactions dynamically with the compaction_switch shell command.
Default
true
hbase.hstore.flusher.count
Description
The number of flush threads. With fewer threads, the MemStore flushes will be queued. With more threads, the flushes will be executed in parallel, increasing the load on HDFS, and potentially causing more compactions.
Default
2
hbase.hstore.blockingStoreFiles
Description
If more than this number of StoreFiles exist in any one Store (one StoreFile is written per flush of MemStore), updates are blocked for this region until a compaction is completed, or until hbase.hstore.blockingWaitTime has been exceeded.
Default
16
hbase.hstore.blockingWaitTime
Description
The time for which a region will block updates after reaching the StoreFile limit defined by hbase.hstore.blockingStoreFiles. After this time has elapsed, the region will stop blocking updates even if a compaction has not been completed.
Default
90000
hbase.hstore.compaction.min
Description
The minimum number of StoreFiles which must be eligible for compaction before compaction can run. The goal of tuning hbase.hstore.compaction.min is to avoid ending up with too many tiny StoreFiles to compact. Setting this value to 2 would cause a minor compaction each time you have two StoreFiles in a Store, and this is probably not appropriate. If you set this value too high, all the other values will need to be adjusted accordingly. For most cases, the default value is appropriate (empty value here, results in 3 by code logic). In previous versions of HBase, the parameter hbase.hstore.compaction.min was named hbase.hstore.compactionThreshold.
Default
none
hbase.hstore.compaction.max
Description
The maximum number of StoreFiles which will be selected for a single minor compaction, regardless of the number of eligible StoreFiles. Effectively, the value of hbase.hstore.compaction.max controls the length of time it takes a single compaction to complete. Setting it larger means that more StoreFiles are included in a compaction. For most cases, the default value is appropriate.
Default
10
hbase.hstore.compaction.min.size
Description
A StoreFile (or a selection of StoreFiles, when using ExploringCompactionPolicy) smaller than this size will always be eligible for minor compaction. HFiles this size or larger are evaluated by hbase.hstore.compaction.ratio to determine if they are eligible. Because this limit represents the "automatic include" limit for all StoreFiles smaller than this value, this value may need to be reduced in write-heavy environments where many StoreFiles in the 1-2 MB range are being flushed, because every StoreFile will be targeted for compaction and the resulting StoreFiles may still be under the minimum size and require further compaction. If this parameter is lowered, the ratio check is triggered more quickly. This addressed some issues seen in earlier versions of HBase but changing this parameter is no longer necessary in most situations. Default: 128 MB expressed in bytes.
Default
134217728
hbase.hstore.compaction.max.size
Description
A StoreFile (or a selection of StoreFiles, when using ExploringCompactionPolicy) larger than this size will be excluded from compaction. The effect of raising hbase.hstore.compaction.max.size is fewer, larger StoreFiles that do not get compacted often. If you feel that compaction is happening too often without much benefit, you can try raising this value. Default: the value of LONG.MAX_VALUE, expressed in bytes.
Default
9223372036854775807
hbase.hstore.compaction.ratio
Description
For minor compaction, this ratio is used to determine whether a given StoreFile which is larger than hbase.hstore.compaction.min.size is eligible for compaction. Its effect is to limit compaction of large StoreFiles. The value of hbase.hstore.compaction.ratio is expressed as a floating-point decimal. A large ratio, such as 10, will produce a single giant StoreFile. Conversely, a low value, such as .25, will produce behavior similar to the BigTable compaction algorithm, producing four StoreFiles. A moderate value of between 1.0 and 1.4 is recommended. When tuning this value, you are balancing write costs with read costs. Raising the value (to something like 1.4) will have more write costs, because you will compact larger StoreFiles. However, during reads, HBase will need to seek through fewer StoreFiles to accomplish the read. Consider this approach if you cannot take advantage of Bloom filters. Otherwise, you can lower this value to something like 1.0 to reduce the background cost of writes, and use Bloom filters to control the number of StoreFiles touched during reads. For most cases, the default value is appropriate.
Default
1.2F
hbase.hstore.compaction.ratio.offpeak
Description
Allows you to set a different (by default, more aggressive) ratio for determining whether larger StoreFiles are included in compactions during off-peak hours. Works in the same way as hbase.hstore.compaction.ratio. Only applies if hbase.offpeak.start.hour and hbase.offpeak.end.hour are also enabled.
Default
5.0F
hbase.hstore.time.to.purge.deletes
Description
The amount of time to delay purging of delete markers with future timestamps. If unset, or set to 0, all delete markers, including those with future timestamps, are purged during the next major compaction. Otherwise, a delete marker is kept until the major compaction which occurs after the marker’s timestamp plus the value of this setting, in milliseconds.
Default
0
hbase.offpeak.start.hour
Description
The start of off-peak hours, expressed as an integer between 0 and 23, inclusive. Set to -1 to disable off-peak.
Default
-1
hbase.offpeak.end.hour
Description
The end of off-peak hours, expressed as an integer between 0 and 23, inclusive. Set to -1 to disable off-peak.
Default
-1
hbase.regionserver.thread.compaction.throttle
Description
There are two different thread pools for compactions, one for large compactions and the other for small compactions. This helps to keep compaction of lean tables (such as hbase:meta) fast. If a compaction is larger than this threshold, it goes into the large compaction pool. In most cases, the default value is appropriate. Default: 2 x hbase.hstore.compaction.max x hbase.hregion.memstore.flush.size (which defaults to 128MB). The value field assumes that the value of hbase.hregion.memstore.flush.size is unchanged from the default.
Default
2684354560
hbase.regionserver.majorcompaction.pagecache.drop
Description
Specifies whether to drop pages read/written into the system page cache by major compactions. Setting it to true helps prevent major compactions from polluting the page cache, which is almost always required, especially for clusters with low/moderate memory to storage ratio.
Default
true
hbase.regionserver.minorcompaction.pagecache.drop
Description
Specifies whether to drop pages read/written into the system page cache by minor compactions. Setting it to true helps prevent minor compactions from polluting the page cache, which is most beneficial on clusters with low memory to storage ratio or very write heavy clusters. You may want to set it to false under moderate to low write workload when bulk of the reads are on the most recently written data.
Default
true
hbase.hstore.compaction.kv.max
Description
The maximum number of KeyValues to read and then write in a batch when flushing or compacting. Set this lower if you have big KeyValues and problems with Out Of Memory Exceptions Set this higher if you have wide, small rows.
Default
10
hbase.storescanner.parallel.seek.enable
Description
Enables StoreFileScanner parallel-seeking in StoreScanner, a feature which can reduce response latency under special conditions.
Default
false
hbase.storescanner.parallel.seek.threads
Description
The default thread pool size if parallel-seeking feature enabled.
Default
10
hfile.block.cache.policy
Description
The eviction policy for the L1 block cache (LRU or TinyLFU).
Default
LRU
hfile.block.cache.size
Description
Percentage of maximum heap (-Xmx setting) to allocate to block cache used by a StoreFile. Default of 0.4 means allocate 40%. Set to 0 to disable but it’s not recommended; you need at least enough cache to hold the storefile indices.
Default
0.4
hfile.block.cache.memory.size
Description
Defines the maximum heap memory allocated for the HFile block cache, specified in bytes or human-readable formats like '10m' for megabytes or '10g' for gigabytes. This configuration allows setting an absolute memory size instead of a percentage of the maximum heap. Takes precedence over hfile.block.cache.size if both are specified.
Default
none
hfile.block.index.cacheonwrite
Description
This allows to put non-root multi-level index blocks into the block cache at the time the index is being written.
Default
false
hfile.index.block.max.size
Description
When the size of a leaf-level, intermediate-level, or root-level index block in a multi-level block index grows to this size, the block is written out and a new block is started.
Default
131072
hbase.bucketcache.ioengine
Description
Where to store the contents of the bucketcache. One of: offheap, file, files, mmap or pmem. If a file or files, set it to file(s):PATH_TO_FILE. mmap means the content will be in an mmaped file. Use mmap:PATH_TO_FILE. 'pmem' is bucket cache over a file on the persistent memory device. Use pmem:PATH_TO_FILE. See [offheap.blockcache](#offheap.blockcache) for more information.
Default
none
hbase.hstore.compaction.throughput.lower.bound
Description
The target lower bound on aggregate compaction throughput, in bytes/sec. Allows you to tune the minimum available compaction throughput when the PressureAwareCompactionThroughputController throughput controller is active. (It is active by default.)
Default
52428800
hbase.hstore.compaction.throughput.higher.bound
Description
The target upper bound on aggregate compaction throughput, in bytes/sec. Allows you to control aggregate compaction throughput demand when the PressureAwareCompactionThroughputController throughput controller is active. (It is active by default.) The maximum throughput will be tuned between the lower and upper bounds when compaction pressure is within the range [0.0, 1.0]. If compaction pressure is 1.0 or greater the higher bound will be ignored until pressure returns to the normal range.
Default
104857600
hbase.bucketcache.size
Description
It is the total capacity in megabytes of BucketCache. Default: 0.0
Default
none
hbase.bucketcache.bucket.sizes
Description
A comma-separated list of sizes for buckets for the bucketcache. Can be multiple sizes. List block sizes in order from smallest to largest. The sizes you use will depend on your data access patterns. Must be a multiple of 256 else you will run into 'java.io.IOException: Invalid HFile block magic' when you go to read from cache. If you specify no values here, then you pick up the default bucketsizes set in code (See BucketAllocator#DEFAULT_BUCKET_SIZES).
Default
none
hfile.format.version
Description
The HFile format version to use for new files. Version 3 adds support for tags in hfiles (See [#hbase.tags](#hbase.tags)). Also see the configuration 'hbase.replication.rpc.codec'.
Default
3
hfile.block.bloom.cacheonwrite
Description
Enables cache-on-write for inline blocks of a compound Bloom filter.
Default
false
io.storefile.bloom.block.size
Description
The size in bytes of a single block ("chunk") of a compound Bloom filter. This size is approximate, because Bloom blocks can only be inserted at data block boundaries, and the number of keys per data block varies.
Default
131072
hbase.rs.cacheblocksonwrite
Description
Whether an HFile block should be added to the block cache when the block is finished.
Default
false
hbase.rpc.timeout
Description
This is for the RPC layer to define how long (millisecond) HBase client applications take for a remote call to time out. It uses pings to check connections but will eventually throw a TimeoutException.
Default
60000
hbase.client.operation.timeout
Description
Operation timeout is a top-level restriction (millisecond) that makes sure a blocking operation in Table will not be blocked more than this. In each operation, if rpc request fails because of timeout or other reason, it will retry until success or throw RetriesExhaustedException. But if the total time being blocking reach the operation timeout before retries exhausted, it will break early and throw SocketTimeoutException.
Default
1200000
hbase.client.connection.metacache.invalidate-interval.ms
Description
Interval in milliseconds of checking and invalidating meta cache when table disabled or dropped, when set to zero means disable checking, suggest set it to 24h or a higher value, because disable/delete table usually not very frequently.
Default
0
hbase.cells.scanned.per.heartbeat.check
Description
The number of cells scanned in between heartbeat checks. Heartbeat checks occur during the processing of scans to determine whether or not the server should stop scanning in order to send back a heartbeat message to the client. Heartbeat messages are used to keep the client-server connection alive during long running scans. Small values mean that the heartbeat checks will occur more often and thus will provide a tighter bound on the execution time of the scan. Larger values mean that the heartbeat checks occur less frequently
Default
10000
hbase.rpc.shortoperation.timeout
Description
This is another version of "hbase.rpc.timeout". For those RPC operation within cluster, we rely on this configuration to set a short timeout limitation for short operation. For example, short rpc timeout for region server’s trying to report to active master can benefit quicker master failover process.
Default
10000
hbase.ipc.client.tcpnodelay
Description
Set no delay on rpc socket connections. See [http://docs.oracle.com/javase/1.5.0/docs/api/java/net/Socket.html#getTcpNoDelay(](http://docs.oracle.com/javase/1.5.0/docs/api/java/net/Socket.html#getTcpNoDelay())
Default
true
hbase.unsafe.regionserver.hostname
Description
This config is for experts: don’t set its value unless you really know what you are doing. When set to a non-empty value, this represents the (external facing) hostname for the underlying server. See [https://issues.apache.org/jira/browse/HBASE-12954](https://issues.apache.org/jira/browse/HBASE-12954) for details.
Default
none
hbase.unsafe.regionserver.hostname.disable.master.reversedns
Description
This config is for experts: don’t set its value unless you really know what you are doing. When set to true, regionserver will use the current node hostname for the servername and HMaster will skip reverse DNS lookup and use the hostname sent by regionserver instead. Note that this config and hbase.unsafe.regionserver.hostname are mutually exclusive. See [https://issues.apache.org/jira/browse/HBASE-18226](https://issues.apache.org/jira/browse/HBASE-18226) for more details.
Default
false
hbase.master.keytab.file
Description
Full path to the kerberos keytab file to use for logging in the configured HMaster server principal.
Default
none
hbase.master.kerberos.principal
Description
Ex. "hbase/_HOST@EXAMPLE.COM". The kerberos principal name that should be used to run the HMaster process. The principal name should be in the form: user/hostname@DOMAIN. If "_HOST" is used as the hostname portion, it will be replaced with the actual hostname of the running instance.
Default
none
hbase.regionserver.keytab.file
Description
Full path to the kerberos keytab file to use for logging in the configured HRegionServer server principal.
Default
none
hbase.regionserver.kerberos.principal
Description
Ex. "hbase/_HOST@EXAMPLE.COM". The kerberos principal name that should be used to run the HRegionServer process. The principal name should be in the form: user/hostname@DOMAIN. If "_HOST" is used as the hostname portion, it will be replaced with the actual hostname of the running instance. An entry for this principal must exist in the file specified in hbase.regionserver.keytab.file
Default
none
hadoop.policy.file
Description
The policy configuration file used by RPC servers to make authorization decisions on client requests. Only used when HBase security is enabled.
Default
hbase-policy.xml
hbase.superuser
Description
List of users or groups (comma-separated), who are allowed full privileges, regardless of stored ACLs, across the cluster. Only used when HBase security is enabled. Group names should be prefixed with "@".
Default
none
hbase.auth.key.update.interval
Description
The update interval for master key for authentication tokens in servers in milliseconds. Only used when HBase security is enabled.
Default
86400000
hbase.auth.token.max.lifetime
Description
The maximum lifetime in milliseconds after which an authentication token expires. Only used when HBase security is enabled.
Default
604800000
hbase.ipc.client.fallback-to-simple-auth-allowed
Description
When a client is configured to attempt a secure connection, but attempts to connect to an insecure server, that server may instruct the client to switch to SASL SIMPLE (unsecure) authentication. This setting controls whether or not the client will accept this instruction from the server. When false (the default), the client will not allow the fallback to SIMPLE authentication, and will abort the connection.
Default
false
hbase.ipc.server.fallback-to-simple-auth-allowed
Description
When a server is configured to require secure connections, it will reject connection attempts from clients using SASL SIMPLE (unsecure) authentication. This setting allows secure servers to accept SASL SIMPLE connections from clients when the client requests. When false (the default), the server will not allow the fallback to SIMPLE authentication, and will reject the connection. WARNING: This setting should ONLY be used as a temporary measure while converting clients over to secure authentication. It MUST BE DISABLED for secure operation.
Default
false
hbase.unsafe.client.kerberos.hostname.disable.reversedns
Description
This config is for experts: don’t set its value unless you really know what you are doing. When set to true, HBase client using SASL Kerberos will skip reverse DNS lookup and use provided hostname of the destination for the principal instead. See [https://issues.apache.org/jira/browse/HBASE-25665](https://issues.apache.org/jira/browse/HBASE-25665) for more details.
Default
false
hbase.display.keys
Description
When this is set to true the webUI and such will display all start/end keys as part of the table details, region names, etc. When this is set to false, the keys are hidden.
Default
true
hbase.coprocessor.enabled
Description
Enables or disables coprocessor loading. If 'false' (disabled), any other coprocessor related configuration will be ignored.
Default
true
hbase.coprocessor.user.enabled
Description
Enables or disables user (aka. table) coprocessor loading. If 'false' (disabled), any table coprocessor attributes in table descriptors will be ignored. If "hbase.coprocessor.enabled" is 'false' this setting has no effect.
Default
true
hbase.coprocessor.region.classes
Description
A comma-separated list of region observer or endpoint coprocessors that are loaded by default on all tables. For any override coprocessor method, these classes will be called in order. After implementing your own Coprocessor, add it to HBase’s classpath and add the fully qualified class name here. A coprocessor can also be loaded on demand by setting HTableDescriptor or the HBase shell.
Default
none
hbase.coprocessor.master.classes
Description
A comma-separated list of org.apache.hadoop.hbase.coprocessor.MasterObserver coprocessors that are loaded by default on the active HMaster process. For any implemented coprocessor methods, the listed classes will be called in order. After implementing your own MasterObserver, just put it in HBase’s classpath and add the fully qualified class name here.
Default
none
hbase.coprocessor.abortonerror
Description
Set to true to cause the hosting server (master or regionserver) to abort if a coprocessor fails to load, fails to initialize, or throws an unexpected Throwable object. Setting this to false will allow the server to continue execution but the system wide state of the coprocessor in question will become inconsistent as it will be properly executing in only a subset of servers, so this is most useful for debugging only.
Default
true
hbase.rest.port
Description
The port for the HBase REST server.
Default
8080
hbase.rest.readonly
Description
Defines the mode the REST server will be started in. Possible values are: false: All HTTP methods are permitted - GET/PUT/POST/DELETE. true: Only the GET method is permitted.
Default
false
hbase.rest.threads.max
Description
The maximum number of threads of the REST server thread pool. Threads in the pool are reused to process REST requests. This controls the maximum number of requests processed concurrently. It may help to control the memory used by the REST server to avoid OOM issues. If the thread pool is full, incoming requests will be queued up and wait for some free threads.
Default
100
hbase.rest.threads.min
Description
The minimum number of threads of the REST server thread pool. The thread pool always has at least these number of threads so the REST server is ready to serve incoming requests.
Default
2
hbase.rest.support.proxyuser
Description
Enables running the REST server to support proxy-user mode.
Default
false
hbase.defaults.for.version.skip
Description
Set to true to skip the 'hbase.defaults.for.version' check. Setting this to true can be useful in contexts other than the other side of a maven generation; i.e. running in an IDE. You’ll want to set this boolean to true to avoid seeing the RuntimeException complaint: "hbase-default.xml file seems to be for and old version of HBase (\${hbase.version}), this version is X.X.X-SNAPSHOT"
Default
false
hbase.table.lock.enable
Description
Set to true to enable locking the table in zookeeper for schema change operations. Table locking from master prevents concurrent schema modifications to corrupt table state.
Default
true
hbase.table.max.rowsize
Description
Maximum size of single row in bytes (default is 1 Gb) for Get’ting or Scan’ning without in-row scan flag set. If row size exceeds this limit RowTooBigException is thrown to client.
Default
1073741824
hbase.thrift.minWorkerThreads
Description
The "core size" of the thread pool. New threads are created on every connection until this many threads are created.
Default
16
hbase.thrift.maxWorkerThreads
Description
The maximum size of the thread pool. When the pending request queue overflows, new threads are created until their number reaches this number. After that, the server starts dropping connections.
Default
1000
hbase.thrift.maxQueuedRequests
Description
The maximum number of pending Thrift connections waiting in the queue. If there are no idle threads in the pool, the server queues requests. Only when the queue overflows, new threads are added, up to hbase.thrift.maxQueuedRequests threads.
Default
1000
hbase.regionserver.thrift.framed
Description
Use Thrift TFramedTransport on the server side. This is the recommended transport for thrift servers and requires a similar setting on the client side. Changing this to false will select the default transport, vulnerable to DoS when malformed requests are issued due to THRIFT-601.
Default
false
hbase.regionserver.thrift.framed.max_frame_size_in_mb
Description
Default frame size when using framed transport, in MB
Default
2
hbase.regionserver.thrift.compact
Description
Use Thrift TCompactProtocol binary serialization protocol.
Default
false
hbase.rootdir.perms
Description
FS Permissions for the root data subdirectory in a secure (kerberos) setup. When master starts, it creates the rootdir with this permissions or sets the permissions if it does not match.
Default
700
hbase.wal.dir.perms
Description
FS Permissions for the root WAL directory in a secure(kerberos) setup. When master starts, it creates the WAL dir with this permissions or sets the permissions if it does not match.
Default
700
hbase.data.umask.enable
Description
Enable, if true, that file permissions should be assigned to the files written by the regionserver
Default
false
hbase.data.umask
Description
File permissions that should be used to write data files when hbase.data.umask.enable is true
Default
000
hbase.snapshot.enabled
Description
Set to true to allow snapshots to be taken / restored / cloned.
Default
true
hbase.snapshot.restore.take.failsafe.snapshot
Description
Set to true to take a snapshot before the restore operation. The snapshot taken will be used in case of failure, to restore the previous state. At the end of the restore operation this snapshot will be deleted
Default
true
hbase.snapshot.restore.failsafe.name
Description
Name of the failsafe snapshot taken by the restore operation. You can use the {snapshot.name}, {table.name} and {restore.timestamp} variables to create a name based on what you are restoring.
Default
hbase-failsafe-{snapshot.name}-{restore.timestamp}
hbase.snapshot.working.dir
Description
Location where the snapshotting process will occur. The location of the completed snapshots will not change, but the temporary directory where the snapshot process occurs will be set to this location. This can be a separate filesystem than the root directory, for performance increase purposes. See HBASE-21098 for more information
Default
none
hbase.server.compactchecker.interval.multiplier
Description
The number that determines how often we scan to see if compaction is necessary. Normally, compactions are done after some events (such as memstore flush), but if region didn’t receive a lot of writes for some time, or due to different compaction policies, it may be necessary to check it periodically. The interval between checks is hbase.server.compactchecker.interval.multiplier multiplied by hbase.server.thread.wakefrequency.
Default
1000
hbase.lease.recovery.timeout
Description
How long we wait on dfs lease recovery in total before giving up.
Default
900000
hbase.lease.recovery.dfs.timeout
Description
How long between dfs recover lease invocations. Should be larger than the sum of the time it takes for the namenode to issue a block recovery command as part of datanode; dfs.heartbeat.interval and the time it takes for the primary datanode, performing block recovery to timeout on a dead datanode; usually dfs.client.socket-timeout. See the end of HBASE-8389 for more.
Default
64000
hbase.column.max.version
Description
New column family descriptors will use this value as the default number of versions to keep.
Default
1
dfs.client.read.shortcircuit
Description
If set to true, this configuration parameter enables short-circuit local reads.
Default
none
dfs.domain.socket.path
Description
This is a path to a UNIX domain socket that will be used for communication between the DataNode and local HDFS clients, if dfs.client.read.shortcircuit is set to true. If the string "_PORT" is present in this path, it will be replaced by the TCP port of the DataNode. Be careful about permissions for the directory that hosts the shared domain socket; dfsclient will complain if open to other users than the HBase user.
Default
none
hbase.dfs.client.read.shortcircuit.buffer.size
Description
If the DFSClient configuration dfs.client.read.shortcircuit.buffer.size is unset, we will use what is configured here as the short circuit read default direct byte buffer size. DFSClient native default is 1MB; HBase keeps its HDFS files open so number of file blocks * 1MB soon starts to add up and threaten OOME because of a shortage of direct memory. So, we set it down from the default. Make it > the default hbase block size set in the HColumnDescriptor which is usually 64k.
Default
131072
hbase.regionserver.checksum.verify
Description
If set to true (the default), HBase verifies the checksums for hfile blocks. HBase writes checksums inline with the data when it writes out hfiles. HDFS (as of this writing) writes checksums to a separate file than the data file necessitating extra seeks. Setting this flag saves some on i/o. Checksum verification by HDFS will be internally disabled on hfile streams when this flag is set. If the hbase-checksum verification fails, we will switch back to using HDFS checksums (so do not disable HDFS checksums! And besides this feature applies to hfiles only, not to WALs). If this parameter is set to false, then hbase will not verify any checksums, instead it will depend on checksum verification being done in the HDFS client.
Default
true
hbase.hstore.bytes.per.checksum
Description
Number of bytes in a newly created checksum chunk for HBase-level checksums in hfile blocks.
Default
16384
hbase.hstore.checksum.algorithm
Description
Name of an algorithm that is used to compute checksums. Possible values are NULL, CRC32, CRC32C.
Default
CRC32C
hbase.client.scanner.max.result.size
Description
Maximum number of bytes returned when calling a scanner’s next method. Note that when a single row is larger than this limit the row is still returned completely. The default value is 2MB, which is good for 1ge networks. With faster and/or high latency networks this value should be increased.
Default
2097152
hbase.server.scanner.max.result.size
Description
Maximum number of bytes returned when calling a scanner’s next method. Note that when a single row is larger than this limit the row is still returned completely. The default value is 100MB. This is a safety setting to protect the server from OOM situations.
Default
104857600
hbase.status.published
Description
This setting activates the publication by the master of the status of the region server. When a region server dies and its recovery starts, the master will push this information to the client application, to let them cut the connection immediately instead of waiting for a timeout.
Default
false
hbase.status.publisher.class
Description
Implementation of the status publication with a multicast message.
Default
org.apache.hadoop.hbase.master.ClusterStatusPublisher$MulticastPublisher
hbase.status.listener.class
Description
Implementation of the status listener with a multicast message.
Default
org.apache.hadoop.hbase.client.ClusterStatusListener$MulticastListener
hbase.status.multicast.address.ip
Description
Multicast address to use for the status publication by multicast.
Default
226.1.1.3
hbase.status.multicast.address.port
Description
Multicast port to use for the status publication by multicast.
Default
16100
hbase.dynamic.jars.dir
Description
The directory from which the custom filter JARs can be loaded dynamically by the region server without the need to restart. However, an already loaded filter/co-processor class would not be un-loaded. See HBASE-1936 for more details. Does not apply to coprocessors.
Default
${hbase.rootdir}/lib
hbase.security.authentication
Description
Controls whether or not secure authentication is enabled for HBase. Possible values are 'simple' (no authentication), and 'kerberos'.
Default
simple
hbase.rest.filter.classes
Description
Servlet filters for REST service.
Default
org.apache.hadoop.hbase.rest.filter.GzipFilter
hbase.master.loadbalancer.class
Description
Class used to execute the regions balancing when the period occurs. See the class comment for more on how it works [http://hbase.apache.org/devapidocs/org/apache/hadoop/hbase/master/balancer/StochasticLoadBalancer.html](http://hbase.apache.org/devapidocs/org/apache/hadoop/hbase/master/balancer/StochasticLoadBalancer.html) It replaces the DefaultLoadBalancer as the default (since renamed as the SimpleLoadBalancer).
Default
org.apache.hadoop.hbase.master.balancer.StochasticLoadBalancer
hbase.master.loadbalance.bytable
Description
Factor Table name when the balancer runs. Default: false.
Default
false
hbase.master.normalizer.class
Description
Class used to execute the region normalization when the period occurs. See the class comment for more on how it works [http://hbase.apache.org/devapidocs/org/apache/hadoop/hbase/master/normalizer/SimpleRegionNormalizer.html](http://hbase.apache.org/devapidocs/org/apache/hadoop/hbase/master/normalizer/SimpleRegionNormalizer.html)
Default
org.apache.hadoop.hbase.master.normalizer.SimpleRegionNormalizer
hbase.rest.csrf.enabled
Description
Set to true to enable protection against cross-site request forgery (CSRF)
Default
false
hbase.rest-csrf.browser-useragents-regex
Description
A comma-separated list of regular expressions used to match against an HTTP request’s User-Agent header when protection against cross-site request forgery (CSRF) is enabled for REST server by setting hbase.rest.csrf.enabled to true. If the incoming User-Agent matches any of these regular expressions, then the request is considered to be sent by a browser, and therefore CSRF prevention is enforced. If the request’s User-Agent does not match any of these regular expressions, then the request is considered to be sent by something other than a browser, such as scripted automation. In this case, CSRF is not a potential attack vector, so the prevention is not enforced. This helps achieve backwards-compatibility with existing automation that has not been updated to send the CSRF prevention header.
Default
Mozilla. , Opera.
hbase.security.exec.permission.checks
Description
If this setting is enabled and ACL based access control is active (the AccessController coprocessor is installed either as a system coprocessor or on a table as a table coprocessor) then you must grant all relevant users EXEC privilege if they require the ability to execute coprocessor endpoint calls. EXEC privilege, like any other permission, can be granted globally to a user, or to a user on a per table or per namespace basis. For more information on coprocessor endpoints, see the coprocessor section of the HBase online manual. For more information on granting or revoking permissions using the AccessController, see the security section of the HBase online manual.
Default
false
hbase.procedure.regionserver.classes
Description
A comma-separated list of org.apache.hadoop.hbase.procedure.RegionServerProcedureManager procedure managers that are loaded by default on the active HRegionServer process. The lifecycle methods (init/start/stop) will be called by the active HRegionServer process to perform the specific globally barriered procedure. After implementing your own RegionServerProcedureManager, just put it in HBase’s classpath and add the fully qualified class name here.
Default
none
hbase.procedure.master.classes
Description
A comma-separated list of org.apache.hadoop.hbase.procedure.MasterProcedureManager procedure managers that are loaded by default on the active HMaster process. A procedure is identified by its signature and users can use the signature and an instant name to trigger an execution of a globally barriered procedure. After implementing your own MasterProcedureManager, just put it in HBase’s classpath and add the fully qualified class name here.
Default
none
hbase.coordinated.state.manager.class
Description
Fully qualified name of class implementing coordinated state manager.
Default
org.apache.hadoop.hbase.coordination.ZkCoordinatedStateManager
hbase.regionserver.storefile.refresh.period
Description
The period (in milliseconds) for refreshing the store files for the secondary regions. 0 means this feature is disabled. Secondary regions sees new files (from flushes and compactions) from primary once the secondary region refreshes the list of files in the region (there is no notification mechanism). But too frequent refreshes might cause extra Namenode pressure. If the files cannot be refreshed for longer than HFile TTL (hbase.master.hfilecleaner.ttl) the requests are rejected. Configuring HFile TTL to a larger value is also recommended with this setting.
Default
0
hbase.region.replica.replication.enabled
Description
Whether asynchronous WAL replication to the secondary region replicas is enabled or not. We have a separated implementation for replicating the WAL without using the general inter-cluster replication framework, so now we will not add any replication peers.
Default
false
hbase.http.filter.initializers
Description
A comma separated list of class names. Each class in the list must extend org.apache.hadoop.hbase.http.FilterInitializer. The corresponding Filter will be initialized. Then, the Filter will be applied to all user facing jsp and servlet web pages. The ordering of the list defines the ordering of the filters. The default StaticUserWebFilter add a user principal as defined by the hbase.http.staticuser.user property.
Default
org.apache.hadoop.hbase.http.lib.StaticUserWebFilter
hbase.security.visibility.mutations.checkauths
Description
This property if enabled, will check whether the labels in the visibility expression are associated with the user issuing the mutation
Default
false
hbase.http.max.threads
Description
The maximum number of threads that the HTTP Server will create in its ThreadPool.
Default
16
hbase.http.metrics.servlets
Description
Comma separated list of servlet names to enable for metrics collection. Supported servlets are jmx, metrics, prometheus
Default
jmx,metrics,prometheus
hbase.replication.rpc.codec
Description
The codec that is to be used when replication is enabled so that the tags are also replicated. This is used along with HFileV3 which supports tags in them. If tags are not used or if the hfile version used is HFileV2 then KeyValueCodec can be used as the replication codec. Note that using KeyValueCodecWithTags for replication when there are no tags causes no harm.
Default
org.apache.hadoop.hbase.codec.KeyValueCodecWithTags
hbase.replication.source.maxthreads
Description
The maximum number of threads any replication source will use for shipping edits to the sinks in parallel. This also limits the number of chunks each replication batch is broken into. Larger values can improve the replication throughput between the master and slave clusters. The default of 10 will rarely need to be changed.
Default
10
hbase.http.staticuser.user
Description
The user name to filter as, on static web filters while rendering content. An example use is the HDFS web UI (user to be used for browsing files).
Default
dr.stack
hbase.regionserver.handler.abort.on.error.percent
Description
The percent of region server RPC threads failed to abort RS. -1 Disable aborting; 0 Abort if even a single handler has died; 0.x Abort only when this percent of handlers have died; 1 Abort only all of the handers have died.
Default
0.5
hbase.mob.file.cache.size
Description
Number of opened file handlers to cache. A larger value will benefit reads by providing more file handlers per mob file cache and would reduce frequent file opening and closing. However, if this is set too high, this could lead to a "too many opened file handlers" The default value is 1000.
Default
1000
hbase.mob.cache.evict.period
Description
The amount of time in seconds before the mob cache evicts cached mob files. The default value is 3600 seconds.
Default
3600
hbase.mob.cache.evict.remain.ratio
Description
The ratio (between 0.0 and 1.0) of files that remains cached after an eviction is triggered when the number of cached mob files exceeds the hbase.mob.file.cache.size. The default value is 0.5f.
Default
0.5f
hbase.master.mob.cleaner.period
Description
The period that MobFileCleanerChore runs. The unit is second. The default value is one day. The MOB file name uses only the date part of the file creation time in it. We use this time for deciding TTL expiry of the files. So the removal of TTL expired files might be delayed. The max delay might be 24 hrs.
Default
86400
hbase.mob.major.compaction.region.batch.size
Description
The max number of a MOB table regions that is allowed in a batch of the mob compaction. By setting this number to a custom value, users can control the overall effect of a major compaction of a large MOB-enabled table. Default is 0 - means no limit - all regions of a MOB table will be compacted at once
Default
0
hbase.mob.compaction.chore.period
Description
The period that MobCompactionChore runs. The unit is second. The default value is one week.
Default
604800
hbase.snapshot.master.timeout.millis
Description
Timeout for master for the snapshot procedure execution.
Default
300000
hbase.snapshot.region.timeout
Description
Timeout for regionservers to keep threads in snapshot request pool waiting.
Default
300000
hbase.rpc.rows.warning.threshold
Description
Number of rows in a batch operation above which a warning will be logged. If hbase.client.write.buffer.maxmutations is not set, this will be used as fallback for that setting.
Default
5000
hbase.master.wait.on.service.seconds
Description
Default is 5 minutes. Make it 30 seconds for tests. See HBASE-19794 for some context.
Default
30
hbase.master.cleaner.snapshot.interval
Description
Snapshot Cleanup chore interval in milliseconds. The cleanup thread keeps running at this interval to find all snapshots that are expired based on TTL and delete them.
Default
1800000
hbase.master.snapshot.ttl
Description
Default Snapshot TTL to be considered when the user does not specify TTL while creating snapshot. Default value 0 indicates FOREVERE - snapshot should not be automatically deleted until it is manually deleted
Default
0
hbase.master.regions.recovery.check.interval
Description
Regions Recovery Chore interval in milliseconds. This chore keeps running at this interval to find all regions with configurable max store file ref count and reopens them.
Default
1200000
hbase.regions.recovery.store.file.ref.count
Description
Very large number of ref count on a compacted store file indicates that it is a ref leak on that object(compacted store file). Such files can not be removed after it is invalidated via compaction. Only way to recover in such scenario is to reopen the region which can release all resources, like the refcount, leases, etc. This config represents Store files Ref Count threshold value considered for reopening regions. Any region with compacted store files ref count > this value would be eligible for reopening by master. Here, we get the max refCount among all refCounts on all compacted away store files that belong to a particular region. Default value -1 indicates this feature is turned off. Only positive integer value should be provided to enable this feature.
Default
-1
hbase.regionserver.slowlog.ringbuffer.size
Description
Default size of ringbuffer to be maintained by each RegionServer in order to store online slowlog responses. This is an in-memory ring buffer of requests that were judged to be too slow in addition to the responseTooSlow logging. The in-memory representation would be complete. For more details, please look into Doc Section: Get Slow Response Log from shell
Default
256
hbase.regionserver.slowlog.buffer.enabled
Description
Indicates whether RegionServers have ring buffer running for storing Online Slow logs in FIFO manner with limited entries. The size of the ring buffer is indicated by config: hbase.regionserver.slowlog.ringbuffer.size The default value is false, turn this on and get latest slowlog responses with complete data.
Default
false
hbase.regionserver.slowlog.systable.enabled
Description
Should be enabled only if hbase.regionserver.slowlog.buffer.enabled is enabled. If enabled (true), all slow/large RPC logs would be persisted to system table hbase:slowlog (in addition to in-memory ring buffer at each RegionServer). The records are stored in increasing order of time. Operators can scan the table with various combination of ColumnValueFilter. More details are provided in the doc section: "Get Slow/Large Response Logs from System table hbase:slowlog"
Default
false
hbase.master.metafixer.max.merge.count
Description
Maximum regions to merge at a time when we fix overlaps noted in CJ consistency report, but avoid merging 100 regions in one go!
Default
64
hbase.rpc.rows.size.threshold.reject
Description
If value is true, RegionServer will abort batch requests of Put/Delete with number of rows in a batch operation exceeding threshold defined by value of config: hbase.rpc.rows.warning.threshold. The default value is false and hence, by default, only warning will be logged. This config should be turned on to prevent RegionServer from serving very large batch size of rows and this way we can improve CPU usages by discarding too large batch request.
Default
false
hbase.namedqueue.provider.classes
Description
Default values for NamedQueueService implementors. This comma separated full class names represent all implementors of NamedQueueService that we would like to be invoked by LogEvent handler service. One example of NamedQueue service is SlowLogQueueService which is used to store slow/large RPC logs in ringbuffer at each RegionServer. All implementors of NamedQueueService should be found under package: "org.apache.hadoop.hbase.namequeues.impl"
Default
org.apache.hadoop.hbase.namequeues.impl.SlowLogQueueService,org.apache.hadoop.hbase.namequeues.impl.BalancerDecisionQueueService,org.apache.hadoop.hbase.namequeues.impl.BalancerRejectionQueueService,org.apache.hadoop.hbase.namequeues.WALEventTrackerQueueService
hbase.master.balancer.decision.buffer.enabled
Description
Indicates whether active HMaster has ring buffer running for storing balancer decisions in FIFO manner with limited entries. The size of the ring buffer is indicated by config: hbase.master.balancer.decision.queue.size
Default
false
hbase.master.balancer.rejection.buffer.enabled
Description
Indicates whether active HMaster has ring buffer running for storing balancer rejection in FIFO manner with limited entries. The size of the ring buffer is indicated by config: hbase.master.balancer.rejection.queue.size
Default
false
hbase.locality.inputstream.derive.enabled
Description
If true, derive StoreFile locality metrics from the underlying DFSInputStream backing reads for that StoreFile. This value will update as the DFSInputStream’s block locations are updated over time. Otherwise, locality is computed on StoreFile open, and cached until the StoreFile is closed.
Default
false
hbase.locality.inputstream.derive.cache.period
Description
If deriving StoreFile locality metrics from the underlying DFSInputStream, how long should the derived values be cached for. The derivation process may involve hitting the namenode, if the DFSInputStream’s block list is incomplete.
Default
60000
### [](#hbase.env.sh)7.3. hbase-env.sh
Set HBase environment variables in this file. Examples include options to pass the JVM on start of
an HBase daemon such as heap size and garbage collector configs.
You can also set configurations for HBase configuration, log directories, niceness, ssh options,
where to locate process pid files, etc. Open the file at conf/hbase-env.sh and peruse its content.
Each option is fairly well documented. Add your own environment variables here if you want them
read by HBase daemons on startup.
Changes here will require a cluster restart for HBase to notice the change.
### [](#log4j)7.4. log4j2.properties
Since version 2.5.0, HBase has upgraded to Log4j2, so the configuration file name and format has changed. Read more in [Apache Log4j2](https://logging.apache.org/log4j/2.x/index.html).
Edit this file to change rate at which HBase files are rolled and to change the level at which
HBase logs messages.
Changes here will require a cluster restart for HBase to notice the change though log levels can
be changed for particular daemons via the HBase UI.
### [](#client_dependencies)7.5. Client configuration and dependencies connecting to an HBase cluster
If you are running HBase in standalone mode, you don’t need to configure anything for your client
to work provided that they are all on the same machine.
Starting release 3.0.0, the default connection registry has been switched to a rpc based
implementation. Refer to [Rpc Connection Registry (new as of 2.5.0)](#client.rpcconnectionregistry) for more details about what a connection
registry is and implications of this change. Depending on your HBase version, following is the
expected minimal client configuration.
#### [](#_up_until_2_x_y_releases)7.5.1. Up until 2.x.y releases
In 2.x.y releases, the default connection registry was based on ZooKeeper as the source of truth.
This means that the clients always looked up ZooKeeper znodes to fetch the required metadata. For
example, if an active master crashed and the a new master is elected, clients looked up the master
znode to fetch the active master address (similarly for meta locations). This meant that the
clients needed to have access to ZooKeeper and need to know the ZooKeeper ensemble information
before they can do anything. This can be configured in the client configuration xml as follows:
<?xml version="1.0"?>
<?xml-stylesheet type="text/xsl" href="configuration.xsl"?>
<configuration>
<property>
<name> hbase.zookeeper.quorum </name>
<value> example1,example2,example3 </value>
<description> Zookeeper ensemble information </description>
</property>
</configuration>
#### [](#_starting_from_3_0_0_release)7.5.2. Starting from 3.0.0 release
The default implementation was switched to a rpc based connection registry. With this
implementation, by default clients contact the active or stand-by master RPC end points to fetch
the connection registry information. This means that the clients should have access to the list of
active and master end points before they can do anything. This can be configured in the client
configuration xml as follows:
<?xml version="1.0"?>
<?xml-stylesheet type="text/xsl" href="configuration.xsl"?>
<configuration>
<property>
<name> hbase.masters </name>
<value> example1,example2,example3 </value>
<description> List of master rpc end points for the hbase cluster. </description>
</property>
</configuration>
The configuration value for hbase.masters is a comma separated list of host:port values. If no
port value is specified, the default of 16000 is assumed.
Of course you are free to specify bootstrap nodes other than masters, like:
<?xml version="1.0"?>
<?xml-stylesheet type="text/xsl" href="configuration.xsl"?>
<property>
<name> hbase.client.bootstrap.servers </name>
<value> server1:16020,server2:16020,server3:16020 </value>
</property>
The configuration value for hbase.client.bootstrap.servers is a comma separated list of
host:port values. Notice that port must be specified here.
Usually these configurations are kept out in the hbase-site.xml and is picked up by the client
from the CLASSPATH .
If you are configuring an IDE to run an HBase client, you should include the conf/ directory on
your classpath so hbase-site.xml settings can be found (or add src/test/resources to pick up
the hbase-site.xml used by tests).
For Java applications using Maven, including the hbase-shaded-client module is the recommended
dependency when connecting to a cluster:
<dependency>
<groupId> org.apache.hbase </groupId>
<artifactId> hbase-shaded-client </artifactId>
<version> 2.0.0 </version>
</dependency>
#### [](#java.client.config)7.5.3. Java client configuration
The configuration used by a Java client is kept in an
[HBaseConfiguration](https://hbase.apache.org/devapidocs/org/apache/hadoop/hbase/HBaseConfiguration)
instance.
The factory method on HBaseConfiguration, HBaseConfiguration.create(); , on invocation, will read
in the content of the first hbase-site.xml found on the client’s CLASSPATH , if one is present
(Invocation will also factor in any hbase-default.xml found; an hbase-default.xml ships inside
the hbase.X.X.X.jar ). It is also possible to specify configuration directly without having to
read from a hbase-site.xml .
For example, to set the ZooKeeper ensemble or bootstrap nodes for the cluster programmatically
do as follows:
Configuration config = HBaseConfiguration.create();
config.set( " hbase.zookeeper.quorum " , " localhost " ); // Until 2.x.y versions
// ---- or ----
config.set( " hbase.client.bootstrap.servers " , " localhost:1234 " ); // Starting 3.0.0 version
### [](#config_timeouts)7.6. Timeout settings
HBase provides a wide variety of timeout settings to limit the execution time of various remote
operations.
-
hbase.rpc.timeout
-
hbase.rpc.read.timeout
-
hbase.rpc.write.timeout
-
hbase.client.operation.timeout
-
hbase.client.meta.operation.timeout
-
hbase.client.scanner.timeout.period
The hbase.rpc.timeout property limits how long a single RPC call can run before timing out.
To fine tune read or write related RPC timeouts set hbase.rpc.read.timeout and
hbase.rpc.write.timeout configuration properties. In the absence of these properties
hbase.rpc.timeout will be used.
A higher-level timeout is hbase.client.operation.timeout which is valid for each client call.
When an RPC call fails for instance for a timeout due to hbase.rpc.timeout it will be retried
until hbase.client.operation.timeout is reached. Client operation timeout for system tables can
be fine tuned by setting hbase.client.meta.operation.timeout configuration value.
When this is not set its value will use hbase.client.operation.timeout .
Timeout for scan operations is controlled differently. Use hbase.client.scanner.timeout.period
property to set this timeout.
## [](#example_config)8. Example Configurations
### [](#_basic_distributed_hbase_install)8.1. Basic Distributed HBase Install
Here is a basic configuration example for a distributed ten node cluster:
* The nodes are named example0 , example1 , etc., through node example9 in this example.
* The HBase Master and the HDFS NameNode are running on the node example0 .
* RegionServers run on nodes example1 - example9 .
* A 3-node ZooKeeper ensemble runs on example1 , example2 , and example3 on the default ports.
* ZooKeeper data is persisted to the directory /export/zookeeper .
Below we show what the main configuration files —  hbase-site.xml , regionservers , and
hbase-env.sh  — found in the HBase conf directory might look like.
#### [](#hbase_site)8.1.1. hbase-site.xml
<?xml version="1.0"?>
<?xml-stylesheet type="text/xsl" href="configuration.xsl"?>
<configuration>
<property>
<name> hbase.zookeeper.quorum </name>
<value> example1,example2,example3 </value>
<description> The directory shared by RegionServers.
</description>
</property>
<property>
<name> hbase.zookeeper.property.dataDir </name>
<value> /export/zookeeper </value>
<description> Property from ZooKeeper config zoo.cfg.
The directory where the snapshot is stored.
</description>
</property>
<property>
<name> hbase.rootdir </name>
<value> hdfs://example0:9000/hbase </value>
<description> The directory shared by RegionServers.
</description>
</property>
<property>
<name> hbase.cluster.distributed </name>
<value> true </value>
<description> The mode the cluster will be in. Possible values are
false: standalone and pseudo-distributed setups with managed ZooKeeper
true: fully-distributed with unmanaged ZooKeeper Quorum (see hbase-env.sh)
</description>
</property>
</configuration>
#### [](#regionservers)8.1.2. regionservers
In this file you list the nodes that will run RegionServers.
In our case, these nodes are example1 - example9 .
example1
example2
example3
example4
example5
example6
example7
example8
example9
#### [](#hbase_env)8.1.3. hbase-env.sh
The following lines in the hbase-env.sh file show how to set the JAVA_HOME environment variable
(required for HBase) and set the heap to 4 GB (rather than the default value of 1 GB). If you copy
and paste this example, be sure to adjust the JAVA_HOME to suit your environment.
# The java implementation to use.
export JAVA_HOME=/usr/java/jdk1 .8 .0 /
# The maximum amount of heap to use. Default is left to JVM default .
export HBASE_HEAPSIZE= 4 G
Use rsync to copy the content of the conf directory to all nodes of the cluster.
## [](#important_configurations)9. The Important Configurations
Below we list some important configurations.
We’ve divided this section into required configuration and worth-a-look recommended configs.
### [](#required_configuration)9.1. Required Configurations
Review the [os](#os) and [hadoop](#hadoop) sections.
#### [](#big.cluster.config)9.1.1. Big Cluster Configurations
If you have a cluster with a lot of regions, it is possible that a Regionserver checks in briefly
after the Master starts while all the remaining RegionServers lag behind. This first server to
check in will be assigned all regions which is not optimal. To prevent the above scenario from
happening, up the hbase.master.wait.on.regionservers.mintostart property from its default value
of 1. See [HBASE-6389 Modify the
conditions to ensure that Master waits for sufficient number of Region Servers before
starting region assignments](https://issues.apache.org/jira/browse/HBASE-6389) for more detail.
### [](#recommended_configurations)9.2. Recommended Configurations
#### [](#recommended_configurations.zk)9.2.1. ZooKeeper Configuration
##### [](#sect.zookeeper.session.timeout) zookeeper.session.timeout
The default timeout is 90 seconds (specified in milliseconds). This means that if a server crashes,
it will be 90 seconds before the Master notices the crash and starts recovery. You might need to
tune the timeout down to a minute or even less so the Master notices failures sooner. Before
changing this value, be sure you have your JVM garbage collection configuration under control,
otherwise, a long garbage collection that lasts beyond the ZooKeeper session timeout will take out
your RegionServer. (You might be fine with this — you probably want recovery to start on the
server if a RegionServer has been in GC for a long period of time).
To change this configuration, edit hbase-site.xml , copy the changed file across the cluster and
restart.
We set this value high to save our having to field questions up on the mailing lists asking why a
RegionServer went down during a massive import. The usual cause is that their JVM is untuned and
they are running into long GC pauses. Our thinking is that while users are getting familiar with
HBase, we’d save them having to know all of its intricacies. Later when they’ve built some
confidence, then they can play with configuration such as this.
##### [](#zookeeper.instances)Number of ZooKeeper Instances
See [zookeeper](#zookeeper).
#### [](#recommended.configurations.hdfs)9.2.2. HDFS Configurations
##### [](#dfs.datanode.failed.volumes.tolerated) dfs.datanode.failed.volumes.tolerated
This is the "…​number of volumes that are allowed to fail before a DataNode stops offering
service. By default, any volume failure will cause a datanode to shutdown" from the
hdfs-default.xml description. You might want to set this to about half the amount of your
available disks.
##### [](#hbase.regionserver.handler.count) hbase.regionserver.handler.count
This setting defines the number of threads that are kept open to answer incoming requests to user
tables. The rule of thumb is to keep this number low when the payload per request approaches the MB
(big puts, scans using a large cache) and high when the payload is small (gets, small puts, ICVs,
deletes). The total size of the queries in progress is limited by the setting
hbase.ipc.server.max.callqueue.size .
It is safe to set that number to the maximum number of incoming clients if their payload is small,
the typical example being a cluster that serves a website since puts aren’t typically buffered and
most of the operations are gets.
The reason why it is dangerous to keep this setting high is that the aggregate size of all the puts
that are currently happening in a region server may impose too much pressure on its memory, or even
trigger an OutOfMemoryError. A RegionServer running on low memory will trigger its JVM’s garbage
collector to run more frequently up to a point where GC pauses become noticeable (the reason being
that all the memory used to keep all the requests' payloads cannot be trashed, no matter how hard
the garbage collector tries). After some time, the overall cluster throughput is affected since
every request that hits that RegionServer will take longer, which exacerbates the problem even more.
You can get a sense of whether you have too little or too many handlers by
[rpc.logging](#rpc.logging) on an individual RegionServer then tailing its logs (Queued requests
consume memory).
#### [](#big_memory)9.2.3. Configuration for large memory machines
HBase ships with a reasonable, conservative configuration that will work on nearly all machine
types that people might want to test with. If you have larger machines — HBase has 8G and larger
heap — you might find the following configuration options helpful.
TODO.
#### [](#config.compression)9.2.4. Compression
You should consider enabling ColumnFamily compression.
There are several options that are near-frictionless and in most all cases boost performance by
reducing the size of StoreFiles and thus reducing I/O.
See [compression](#compression) for more information.
#### [](#config.wals)9.2.5. Configuring the size and number of WAL files
HBase uses [wal](#wal) to recover the memstore data that has not been flushed to disk in case of
an RS failure. These WAL files should be configured to be slightly smaller than HDFS block (by
default a HDFS block is 64Mb and a WAL file is ~60Mb).
HBase also has a limit on the number of WAL files, designed to ensure there’s never too much data
that needs to be replayed during recovery. This limit needs to be set according to memstore
configuration, so that all the necessary data would fit. It is recommended to allocate enough WAL
files to store at least that much data (when all memstores are close to full). For example, with
16Gb RS heap, default memstore settings (0.4), and default WAL file size (~60Mb), 16Gb*0.4/60, the
starting point for WAL file count is ~109. However, as all memstores are not expected to be full
all the time, less WAL files can be allocated.
#### [](#disable.splitting)9.2.6. Managed Splitting
HBase generally handles splitting of your regions based upon the settings in your
hbase-default.xml and hbase-site.xml configuration files. Important settings include
hbase.regionserver.region.split.policy , hbase.hregion.max.filesize ,
hbase.regionserver.regionSplitLimit . A simplistic view of splitting is that when a region grows
to hbase.hregion.max.filesize , it is split. For most usage patterns, you should use automatic
splitting. See [manual region splitting decisions](#manual_region_splitting_decisions) for more
information about manual region splitting.
Instead of allowing HBase to split your regions automatically, you can choose to manage the
splitting yourself. Manually managing splits works if you know your keyspace well, otherwise let
HBase figure where to split for you. Manual splitting can mitigate region creation and movement
under load. It also makes it so region boundaries are known and invariant (if you disable region
splitting). If you use manual splits, it is easier doing staggered, time-based major compactions
to spread out your network IO load.
Disable Automatic Splitting
To disable automatic splitting, you can set region split policy in either cluster configuration
or table configuration to be org.apache.hadoop.hbase.regionserver.DisabledRegionSplitPolicy
Automatic Splitting Is Recommended
If you disable automatic splits to diagnose a problem or during a period of fast data growth, it
is recommended to re-enable them when your situation becomes more stable. The potential benefits
of managing region splits yourself are not undisputed.
Determine the Optimal Number of Pre-Split Regions
The optimal number of pre-split regions depends on your application and environment. A good rule of
thumb is to start with 10 pre-split regions per server and watch as data grows over time. It is
better to err on the side of too few regions and perform rolling splits later. The optimal number
of regions depends upon the largest StoreFile in your region. The size of the largest StoreFile
will increase with time if the amount of data grows. The goal is for the largest region to be just
large enough that the compaction selection algorithm only compacts it during a timed major
compaction. Otherwise, the cluster can be prone to compaction storms with a large number of regions
under compaction at the same time. It is important to understand that the data growth causes
compaction storms and not the manual split decision.
If the regions are split into too many large regions, you can increase the major compaction
interval by configuring HConstants.MAJOR_COMPACTION_PERIOD . The
org.apache.hadoop.hbase.util.RegionSplitter utility also provides a network-IO-safe rolling
split of all regions.
#### [](#managed.compactions)9.2.7. Managed Compactions
By default, major compactions are scheduled to run once in a 7-day period.
If you need to control exactly when and how often major compaction runs, you can disable managed
major compactions. See the entry for hbase.hregion.majorcompaction in the
[compaction.parameters](#compaction.parameters) table for details.
Do Not Disable Major Compactions
Major compactions are absolutely necessary for StoreFile clean-up. Do not disable them altogether.
You can run major compactions manually via the HBase shell or via the
[Admin API](https://hbase.apache.org/devapidocs/org/apache/hadoop/hbase/client/Admin.html#majorCompact(org.apache.hadoop.hbase.TableName)).
For more information about compactions and the compaction file selection process, see
[compaction](#compaction)
#### [](#spec.ex)9.2.8. Speculative Execution
Speculative Execution of MapReduce tasks is on by default, and for HBase clusters it is generally
advised to turn off Speculative Execution at a system-level unless you need it for a specific case,
where it can be configured per-job. Set the properties mapreduce.map.speculative and
mapreduce.reduce.speculative to false.
### [](#other_configuration)9.3. Other Configurations
#### [](#balancer_config)9.3.1. Balancer
The balancer is a periodic operation which is run on the master to redistribute regions on the
cluster. It is configured via hbase.balancer.period and defaults to 300000 (5 minutes).
See [master.processes.loadbalancer](#master.processes.loadbalancer) for more information on the
LoadBalancer.
#### [](#disabling.blockcache)9.3.2. Disabling Blockcache
Do not turn off block cache (You’d do it by setting hfile.block.cache.size to zero). Currently,
we do not do well if you do this because the RegionServer will spend all its time loading HFile
indices over and over again. If your working set is such that block cache does you no good, at
least size the block cache such that HFile indices will stay up in the cache (you can get a rough
idea on the size you need by surveying RegionServer UIs; you’ll see index block size accounted near
the top of the webpage).
#### [](#nagles)9.3.3. [Nagle’s](https://en.wikipedia.org/wiki/Nagle%27s_algorithm) or the small package problem
If a big 40ms or so occasional delay is seen in operations against HBase, try the Nagles' setting.
For example, see the user mailing list thread,
[Inconsistent scan performance with caching set to 1](https://lists.apache.org/thread.html/3d7ceb41c04a955b1b1c80480cdba95208ca3e97bf6895a40e0c1bbb%401346186127%40%3Cuser.hbase.apache.org%3E)
and the issue cited therein where setting notcpdelay improved scan speeds. You might also see the
graphs on the tail of
[HBASE-7008 Set scanner caching to a better default](https://issues.apache.org/jira/browse/HBASE-7008)
where our Lars Hofhansl tries various data sizes w/ Nagle’s on and off measuring the effect.
#### [](#mttr)9.3.4. Better Mean Time to Recover (MTTR)
This section is about configurations that will make servers come back faster after a fail. See the
Deveraj Das and Nicolas Liochon blog post
[Introduction to HBase Mean Time to Recover (MTTR)](http://hortonworks.com/blog/introduction-to-hbase-mean-time-to-recover-mttr/)
for a brief introduction.
The issue
[HBASE-8354 forces Namenode into loop with lease recovery requests](https://issues.apache.org/jira/browse/HBASE-8389)
is messy but has a bunch of good discussion toward the end on low timeouts and how to cause faster
recovery including citation of fixes added to HDFS. Read the Varun Sharma comments. The below
suggested configurations are Varun’s suggestions distilled and tested. Make sure you are running
on a late-version HDFS so you have the fixes he refers to and himself adds to HDFS that help HBase
MTTR (e.g. HDFS-3703, HDFS-3712, and HDFS-4791 — Hadoop 2 for sure has them and late Hadoop 1 has
some). Set the following in the RegionServer.
<property>
<name> hbase.lease.recovery.dfs.timeout </name>
<value> 23000 </value>
<description> How much time we allow elapse between calls to recover lease.
Should be larger than the dfs timeout. </description>
</property>
<property>
<name> dfs.client.socket-timeout </name>
<value> 10000 </value>
<description> Down the DFS timeout from 60 to 10 seconds. </description>
</property>
And on the NameNode/DataNode side, set the following to enable 'staleness' introduced in HDFS-3703,
HDFS-3912.
<property>
<name> dfs.client.socket-timeout </name>
<value> 10000 </value>
<description> Down the DFS timeout from 60 to 10 seconds. </description>
</property>
<property>
<name> dfs.datanode.socket.write.timeout </name>
<value> 10000 </value>
<description> Down the DFS timeout from 8 * 60 to 10 seconds. </description>
</property>
<property>
<name> ipc.client.connect.timeout </name>
<value> 3000 </value>
<description> Down from 60 seconds to 3. </description>
</property>
<property>
<name> ipc.client.connect.max.retries.on.timeouts </name>
<value> 2 </value>
<description> Down from 45 seconds to 3 (2 == 3 retries). </description>
</property>
<property>
<name> dfs.namenode.avoid.read.stale.datanode </name>
<value> true </value>
<description> Enable stale state in hdfs </description>
</property>
<property>
<name> dfs.namenode.stale.datanode.interval </name>
<value> 20000 </value>
<description> Down from default 30 seconds </description>
</property>
<property>
<name> dfs.namenode.avoid.write.stale.datanode </name>
<value> true </value>
<description> Enable stale state in hdfs </description>
</property>
#### [](#jmx_config)9.3.5. JMX
JMX (Java Management Extensions) provides built-in instrumentation that enables you to monitor and
manage the Java VM. To enable monitoring and management from remote systems, you need to set system
property com.sun.management.jmxremote.port (the port number through which you want to enable JMX
RMI connections) when you start the Java VM. See the
[official documentation](http://docs.oracle.com/javase/8/docs/technotes/guides/management/agent.html)
for more information. Historically, besides above port mentioned, JMX opens two additional random
TCP listening ports, which could lead to port conflict problem. (See
[HBASE-10289](https://issues.apache.org/jira/browse/HBASE-10289) for details)
As an alternative, you can use the coprocessor-based JMX implementation provided by HBase. To
enable it, add below property in hbase-site.xml :
<property>
<name> hbase.coprocessor.regionserver.classes </name>
<value> org.apache.hadoop.hbase.JMXListener </value>
</property>
DO NOT set com.sun.management.jmxremote.port for Java VM at the same time.
Currently it supports Master and RegionServer Java VM.
By default, the JMX listens on TCP port 10102, you can further configure the port using below
properties:
<property>
<name> regionserver.rmi.registry.port </name>
<value> 61130 </value>
</property>
<property>
<name> regionserver.rmi.connector.port </name>
<value> 61140 </value>
</property>
The registry port can be shared with connector port in most cases, so you only need to configure
regionserver.rmi.registry.port . However, if you want to use SSL communication, the 2 ports must
be configured to different values.
By default the password authentication and SSL communication is disabled.
To enable password authentication, you need to update hbase-env.sh like below:
export HBASE_JMX_BASE="-Dcom.sun.management.jmxremote.authenticate=true \
-Dcom.sun.management.jmxremote.password.file=your_password_file \
-Dcom.sun.management.jmxremote.access.file=your_access_file"
export HBASE_MASTER_OPTS="$HBASE_MASTER_OPTS $HBASE_JMX_BASE "
export HBASE_REGIONSERVER_OPTS="$HBASE_REGIONSERVER_OPTS $HBASE_JMX_BASE "
See example password/access file under $JRE_HOME/lib/management .
To enable SSL communication with password authentication, follow below steps:
#1. generate a key pair, stored in myKeyStore
keytool -genkey -alias jconsole -keystore myKeyStore
#2. export it to file jconsole.cert
keytool -export -alias jconsole -keystore myKeyStore -file jconsole.cert
#3. copy jconsole.cert to jconsole client machine, import it to jconsoleKeyStore
keytool -import -alias jconsole -keystore jconsoleKeyStore -file jconsole.cert
And then update hbase-env.sh like below:
export HBASE_JMX_BASE="-Dcom.sun.management.jmxremote.ssl=true \
-Djavax.net.ssl.keyStore=/home/tianq/myKeyStore \
-Djavax.net.ssl.keyStorePassword=your_password_in_step_1 \
-Dcom.sun.management.jmxremote.authenticate=true \
-Dcom.sun.management.jmxremote.password.file=your_password file \
-Dcom.sun.management.jmxremote.access.file=your_access_file"
export HBASE_MASTER_OPTS="$HBASE_MASTER_OPTS $HBASE_JMX_BASE "
export HBASE_REGIONSERVER_OPTS="$HBASE_REGIONSERVER_OPTS $HBASE_JMX_BASE "
Finally start jconsole on the client using the key store:
jconsole -J-Djavax.net.ssl.trustStore=/home/tianq/jconsoleKeyStore
To enable the HBase JMX implementation on Master, you also need to add below property in
hbase-site.xml :
<property>
<name> hbase.coprocessor.master.classes </name>
<value> org.apache.hadoop.hbase.JMXListener </value>
</property>
The corresponding properties for port configuration are master.rmi.registry.port (by default
10101) and master.rmi.connector.port (by default the same as registry.port)
## [](#dyn_config)10. Dynamic Configuration
It is possible to change a subset of the configuration without requiring a server restart. In the
HBase shell, the operations update_config , update_all_config and update_rsgroup_config
will prompt a server, all servers or all servers in the RSGroup to reload configuration.
Only a subset of all configurations can currently be changed in the running server.
Here are those configurations:
Table 9. Configurations that support dynamic change
Key
hbase.balancer.tablesOnMaster
hbase.balancer.tablesOnMaster.systemTablesOnly
hbase.cleaner.scan.dir.concurrent.size
hbase.coprocessor.master.classes
hbase.coprocessor.region.classes
hbase.coprocessor.regionserver.classes
hbase.coprocessor.user.region.classes
hbase.hregion.majorcompaction
hbase.hregion.majorcompaction.jitter
hbase.hstore.compaction.date.tiered.incoming.window.min
hbase.hstore.compaction.date.tiered.max.storefile.age.millis
hbase.hstore.compaction.date.tiered.single.output.for.minor.compaction
hbase.hstore.compaction.date.tiered.window.factory.class
hbase.hstore.compaction.date.tiered.window.policy.class
hbase.hstore.compaction.max
hbase.hstore.compaction.max.size
hbase.hstore.compaction.max.size.offpeak
hbase.hstore.compaction.min
hbase.hstore.compaction.min.size
hbase.hstore.compaction.ratio
hbase.hstore.compaction.ratio.offpeak
hbase.hstore.min.locality.to.skip.major.compact
hbase.ipc.server.callqueue.codel.interval
hbase.ipc.server.callqueue.codel.lifo.threshold
hbase.ipc.server.callqueue.codel.target.delay
hbase.ipc.server.callqueue.type
hbase.ipc.server.fallback-to-simple-auth-allowed
hbase.ipc.server.max.callqueue.length
hbase.ipc.server.priority.max.callqueue.length
hbase.master.balancer.stochastic.localityCost
hbase.master.balancer.stochastic.maxMovePercent
hbase.master.balancer.stochastic.maxRunningTime
hbase.master.balancer.stochastic.maxSteps
hbase.master.balancer.stochastic.memstoreSizeCost
hbase.master.balancer.stochastic.minCostNeedBalance
hbase.master.balancer.stochastic.moveCost
hbase.master.balancer.stochastic.moveCost.offpeak
hbase.master.balancer.stochastic.numRegionLoadsToRemember
hbase.master.balancer.stochastic.primaryRegionCountCost
hbase.master.balancer.stochastic.rackLocalityCost
hbase.master.balancer.stochastic.readRequestCost
hbase.master.balancer.stochastic.regionCountCost
hbase.master.balancer.stochastic.regionReplicaHostCostKey
hbase.master.balancer.stochastic.regionReplicaRackCostKey
hbase.master.balancer.stochastic.runMaxSteps
hbase.master.balancer.stochastic.stepsPerRegion
hbase.master.balancer.stochastic.storefileSizeCost
hbase.master.balancer.stochastic.tableSkewCost
hbase.master.balancer.stochastic.writeRequestCost
hbase.master.loadbalance.bytable
hbase.master.regions.recovery.check.interval
hbase.offpeak.end.hour
hbase.offpeak.start.hour
hbase.oldwals.cleaner.thread.check.interval.msec
hbase.oldwals.cleaner.thread.size
hbase.oldwals.cleaner.thread.timeout.msec
hbase.procedure.worker.add.stuck.percentage
hbase.procedure.worker.keep.alive.time.msec
hbase.procedure.worker.monitor.interval.msec
hbase.procedure.worker.stuck.threshold.msec
hbase.regionserver.flush.throughput.controller
hbase.regionserver.hfilecleaner.large.queue.size
hbase.regionserver.hfilecleaner.large.thread.count
hbase.regionserver.hfilecleaner.small.queue.size
hbase.regionserver.hfilecleaner.small.thread.count
hbase.regionserver.hfilecleaner.thread.check.interval.msec
hbase.regionserver.hfilecleaner.thread.timeout.msec
hbase.regionserver.thread.compaction.large
hbase.regionserver.thread.compaction.small
hbase.regionserver.thread.compaction.throttle
hbase.regionserver.thread.hfilecleaner.throttle
hbase.regionserver.thread.split
hbase.regionserver.throughput.controller
hbase.regions.overallSlop
hbase.regions.recovery.store.file.ref.count
hbase.regions.slop
hbase.rsgroup.fallback.enable
hbase.util.ip.to.rack.determiner
# [](#upgrading)Upgrading
You cannot skip major versions when upgrading. If you are upgrading from version 0.98.x to 2.x, you must first go from 0.98.x to 1.2.x and then go from 1.2.x to 2.x.
Review [Apache HBase Configuration](#configuration), in particular [Hadoop](#hadoop). Familiarize yourself with [Support and Testing Expectations](#hbase_supported_tested_definitions).
## [](#hbase.versioning)11. HBase version number and compatibility
### [](#hbase.versioning.post10)11.1. Aspirational Semantic Versioning
Starting with the 1.0.0 release, HBase is working towards [Semantic Versioning](http://semver.org/) for its release versioning. In summary:
Given a version number MAJOR.MINOR.PATCH, increment the:
-
MAJOR version when you make incompatible API changes,
-
MINOR version when you add functionality in a backwards-compatible manner, and
-
PATCH version when you make backwards-compatible bug fixes.
-
Additional labels for pre-release and build metadata are available as extensions to the MAJOR.MINOR.PATCH format.
Compatibility Dimensions
In addition to the usual API versioning considerations HBase has other compatibility dimensions that we need to consider.
Client-Server wire protocol compatibility
-
Allows updating client and server out of sync.
-
We could only allow upgrading the server first. I.e. the server would be backward compatible to an old client, that way new APIs are OK.
-
Example: A user should be able to use an old client to connect to an upgraded cluster.
Server-Server protocol compatibility
-
Servers of different versions can co-exist in the same cluster.
-
The wire protocol between servers is compatible.
-
Workers for distributed tasks, such as replication and log splitting, can co-exist in the same cluster.
-
Dependent protocols (such as using ZK for coordination) will also not be changed.
-
Example: A user can perform a rolling upgrade.
File format compatibility
-
Support file formats backward and forward compatible
-
Example: File, ZK encoding, directory layout is upgraded automatically as part of an HBase upgrade. User can downgrade to the older version and everything will continue to work.
Client API compatibility
-
Allow changing or removing existing client APIs.
-
An API needs to be deprecated for a whole major version before we will change/remove it.
-
An example: An API was deprecated in 2.0.1 and will be marked for deletion in 4.0.0. On the other hand, an API deprecated in 2.0.0 can be removed in 3.0.0.
-
Occasionally mistakes are made and internal classes are marked with a higher access level than they should. In these rare circumstances, we will accelerate the deprecation schedule to the next major version (i.e., deprecated in 2.2.x, marked IA.Private 3.0.0). Such changes are communicated and explained via release note in Jira.
-
APIs available in a patch version will be available in all later patch versions. However, new APIs may be added which will not be available in earlier patch versions.
-
New APIs introduced in a patch version will only be added in a source compatible way [[1](#_footnotedef_1)] : i.e. code that implements public APIs will continue to compile.
-
Example: A user using a newly deprecated API does not need to modify application code with HBase API calls until the next major version.
*
Client Binary compatibility
-
Client code written to APIs available in a given patch release can run unchanged (no recompilation needed) against the new jars of later patch versions.
-
Client code written to APIs available in a given patch release might not run against the old jars from an earlier patch version.
-
Example: Old compiled client code will work unchanged with the new jars.
-
If a Client implements an HBase Interface, a recompile MAY be required upgrading to a newer minor version (See release notes
for warning about incompatible changes). All effort will be made to provide a default implementation so this case should not arise.
Server-Side Limited API compatibility (taken from Hadoop)
-
Internal APIs are marked as Stable, Evolving, or Unstable
-
This implies binary compatibility for coprocessors and plugins (pluggable classes, including replication) as long as these are only using marked interfaces/classes.
-
Example: Old compiled Coprocessor, Filter, or Plugin code will work unchanged with the new jars.
Dependency Compatibility
-
An upgrade of HBase will not require an incompatible upgrade of a dependent project, except for Apache Hadoop.
-
An upgrade of HBase will not require an incompatible upgrade of the Java runtime.
-
Example: Upgrading HBase to a version that supports Dependency Compatibility won’t require that you upgrade your Apache ZooKeeper service.
-
Example: If your current version of HBase supported running on JDK 8, then an upgrade to a version that supports Dependency Compatibility will also run on JDK 8.
Hadoop Versions
Previously, we tried to maintain dependency compatibility for the underly Hadoop service but over the last few years this has proven untenable. While the HBase project attempts to maintain support for older versions of Hadoop, we drop the "supported" designator for minor versions that fail to continue to see releases. Additionally, the Hadoop project has its own set of compatibility guidelines, which means in some cases having to update to a newer supported minor release might break some of our compatibility promises.
Operational Compatibility
-
Metric changes
-
Behavioral changes of services
-
JMX APIs exposed via the /jmx/ endpoint
Summary
-
A patch upgrade is a drop-in replacement. Any change that is not Java binary and source compatible would not be allowed. [[2](#_footnotedef_2)] Downgrading versions within patch releases may not be compatible.
-
A minor upgrade requires no application/client code modification. Ideally it would be a drop-in replacement but client code, coprocessors, filters, etc might have to be recompiled if new jars are used.
-
A major upgrade allows the HBase community to make breaking changes.
Table 10. Compatibility Matrix [[3](#_footnotedef_3)]
Major
Minor
Patch
Client-Server wire Compatibility
N
Y
Y
Server-Server Compatibility
N
Y
Y
File Format Compatibility
N [[4](#_footnotedef_4)]
Y
Y
Client API Compatibility
N
Y
Y
Client Binary Compatibility
N
N
Y
Server-Side Limited API Compatibility
Stable
N
Y
Y
Evolving
N
N
Y
Unstable
N
N
N
Dependency Compatibility
N
Y
Y
Operational Compatibility
N
N
Y
HBase 1.7.0 release violated client-server wire compatibility guarantees and was subsequently
withdrawn after the incompatibilities were reported and fixed in 1.7.1. If you are considering an
upgrade to 1.7.x line, see [Upgrading to 1.7.1+](#upgrade1.7.x).
#### [](#hbase.client.api.surface)11.1.1. HBase API Surface
HBase has a lot of API points, but for the compatibility matrix above, we differentiate between Client API, Limited Private API, and Private API. HBase uses [Apache Yetus Audience Annotations](https://yetus.apache.org/documentation/in-progress/interface-classification/) to guide downstream expectations for stability.
-
InterfaceAudience ([javadocs](https://yetus.apache.org/documentation/in-progress/javadocs/org/apache/yetus/audience/InterfaceAudience.html)): captures the intended audience, possible values include:
-
Public: safe for end users and external projects
-
LimitedPrivate: used for internals we expect to be pluggable, such as coprocessors
-
Private: strictly for use within HBase itself
Classes which are defined as IA.Private may be used as parameters or return values for interfaces which are declared IA.LimitedPrivate . Treat the IA.Private object as opaque; do not try to access its methods or fields directly.
-
InterfaceStability ([javadocs](https://yetus.apache.org/documentation/in-progress/javadocs/org/apache/yetus/audience/InterfaceStability.html)): describes what types of interface changes are permitted. Possible values include:
-
Stable: the interface is fixed and is not expected to change
-
Evolving: the interface may change in future minor versions
-
Unstable: the interface may change at any time
Please keep in mind the following interactions between the InterfaceAudience and InterfaceStability annotations within the HBase project:
-
IA.Public classes are inherently stable and adhere to our stability guarantees relating to the type of upgrade (major, minor, or patch).
-
IA.LimitedPrivate classes should always be annotated with one of the given InterfaceStability values. If they are not, you should presume they are IS.Unstable .
-
IA.Private classes should be considered implicitly unstable, with no guarantee of stability between releases.
HBase Client API
HBase Client API consists of all the classes or methods that are marked with InterfaceAudience.Public interface. All main classes in hbase-client and dependent modules have either InterfaceAudience.Public, InterfaceAudience.LimitedPrivate, or InterfaceAudience.Private marker. Not all classes in other modules (hbase-server, etc) have the marker. If a class is not annotated with one of these, it is assumed to be a InterfaceAudience.Private class.
HBase LimitedPrivate API
LimitedPrivate annotation comes with a set of target consumers for the interfaces. Those consumers are coprocessors, phoenix, replication endpoint implementations or similar. At this point, HBase only guarantees source and binary compatibility for these interfaces between patch versions.
HBase Private API
All classes annotated with InterfaceAudience.Private or all classes that do not have the annotation are for HBase internal use only. The interfaces and method signatures can change at any point in time. If you are relying on a particular interface that is marked Private, you should open a jira to propose changing the interface to be Public or LimitedPrivate, or an interface exposed for this purpose.
Binary Compatibility
When we say two HBase versions are compatible, we mean that the versions are wire and binary compatible. Compatible HBase versions means that clients can talk to compatible but differently versioned servers. It means too that you can just swap out the jars of one version and replace them with the jars of another, compatible version and all will just work. Unless otherwise specified, HBase point versions are (mostly) binary compatible. You can safely do rolling upgrades between binary compatible versions; i.e. across maintenance releases: e.g. from 1.4.4 to 1.4.6. See [Does compatibility between versions also mean binary compatibility?](/book.html) discussion on the HBase dev mailing list.
### [](#hbase.rolling.upgrade)11.2. Rolling Upgrades
A rolling upgrade is the process by which you update the servers in your cluster a server at a time. You can rolling upgrade across HBase versions if they are binary or wire compatible. See [Rolling Upgrade Between Versions that are Binary/Wire Compatible](#hbase.rolling.restart) for more on what this means. Coarsely, a rolling upgrade is a graceful stop each server, update the software, and then restart. You do this for each server in the cluster. Usually you upgrade the Master first and then the RegionServers. See [Rolling Restart](#rolling) for tools that can help use the rolling upgrade process.
For example, in the below, HBase was symlinked to the actual HBase install. On upgrade, before running a rolling restart over the cluster, we changed the symlink to point at the new HBase software version and then ran
$ HADOOP_HOME=~/hadoop-2.6.0-CRC-SNAPSHOT ~/hbase/bin/rolling-restart.sh --config ~/conf_hbase
The rolling-restart script will first gracefully stop and restart the master, and then each of the RegionServers in turn. Because the symlink was changed, on restart the server will come up using the new HBase version. Check logs for errors as the rolling upgrade proceeds.
Rolling Upgrade Between Versions that are Binary/Wire Compatible
Unless otherwise specified, HBase minor versions are binary compatible. You can do a [Rolling Upgrades](#hbase.rolling.upgrade) between HBase point versions. For example, you can go to 1.4.4 from 1.4.6 by doing a rolling upgrade across the cluster replacing the 1.4.4 binary with a 1.4.6 binary.
In the minor version-particular sections below, we call out where the versions are wire/protocol compatible and in this case, it is also possible to do a [Rolling Upgrades](#hbase.rolling.upgrade).
## [](#_rollback)12. Rollback
Sometimes things don’t go as planned when attempting an upgrade. This section explains how to perform a rollback to an earlier HBase release. Note that this should only be needed between Major and some Minor releases. You should always be able to downgrade between HBase Patch releases within the same Minor version. These instructions may require you to take steps before you start the upgrade process, so be sure to read through this section beforehand.
### [](#_caveats)12.1. Caveats
Rollback vs Downgrade
This section describes how to perform a rollback on an upgrade between HBase minor and major versions. In this document, rollback refers to the process of taking an upgraded cluster and restoring it to the old version while losing all changes that have occurred since upgrade . By contrast, a cluster downgrade would restore an upgraded cluster to the old version while maintaining any data written since the upgrade. We currently only offer instructions to rollback HBase clusters. Further, rollback only works when these instructions are followed prior to performing the upgrade.
When these instructions talk about rollback vs downgrade of prerequisite cluster services (i.e. HDFS), you should treat leaving the service version the same as a degenerate case of downgrade.
Replication
Unless you are doing an all-service rollback, the HBase cluster will lose any configured peers for HBase replication. If your cluster is configured for HBase replication, then prior to following these instructions you should document all replication peers. After performing the rollback you should then add each documented peer back to the cluster. For more information on enabling HBase replication, listing peers, and adding a peer see [Managing and Configuring Cluster Replication](#hbase.replication.management). Note also that data written to the cluster since the upgrade may or may not have already been replicated to any peers. Determining which, if any, peers have seen replication data as well as rolling back the data in those peers is out of the scope of this guide.
Data Locality
Unless you are doing an all-service rollback, going through a rollback procedure will likely destroy all locality for Region Servers. You should expect degraded performance until after the cluster has had time to go through compactions to restore data locality. Optionally, you can force a compaction to speed this process up at the cost of generating cluster load.
Configurable Locations
The instructions below assume default locations for the HBase data directory and the HBase znode. Both of these locations are configurable and you should verify the value used in your cluster before proceeding. In the event that you have a different value, just replace the default with the one found in your configuration
* HBase data directory is configured via the key 'hbase.rootdir' and has a default value of '/hbase'.
* HBase znode is configured via the key 'zookeeper.znode.parent' and has a default value of '/hbase'.
### [](#_all_service_rollback)12.2. All service rollback
If you will be performing a rollback of both the HDFS and ZooKeeper services, then HBase’s data will be rolled back in the process.
Requirements
-
Ability to rollback HDFS and ZooKeeper
Before upgrade
No additional steps are needed pre-upgrade. As an extra precautionary measure, you may wish to use distcp to back up the HBase data off of the cluster to be upgraded. To do so, follow the steps in the 'Before upgrade' section of 'Rollback after HDFS downgrade' but copy to another HDFS instance instead of within the same instance.
Performing a rollback
-
Stop HBase
-
Perform a rollback for HDFS and ZooKeeper (HBase should remain stopped)
-
Change the installed version of HBase to the previous version
-
Start HBase
-
Verify HBase contents—use the HBase shell to list tables and scan some known values.
### [](#_rollback_after_hdfs_rollback_and_zookeeper_downgrade)12.3. Rollback after HDFS rollback and ZooKeeper downgrade
If you will be rolling back HDFS but going through a ZooKeeper downgrade, then HBase will be in an inconsistent state. You must ensure the cluster is not started until you complete this process.
Requirements
-
Ability to rollback HDFS
-
Ability to downgrade ZooKeeper
Before upgrade
No additional steps are needed pre-upgrade. As an extra precautionary measure, you may wish to use distcp to back up the HBase data off of the cluster to be upgraded. To do so, follow the steps in the 'Before upgrade' section of 'Rollback after HDFS downgrade' but copy to another HDFS instance instead of within the same instance.
Performing a rollback
-
Stop HBase
-
Perform a rollback for HDFS and a downgrade for ZooKeeper (HBase should remain stopped)
-
Change the installed version of HBase to the previous version
-
Clean out ZooKeeper information related to HBase. WARNING: This step will permanently destroy all replication peers. Please see the section on HBase Replication under Caveats for more information.
Clean HBase information out of ZooKeeper
[hpnewton@gateway_node.example.com ~]$ zookeeper-client -server zookeeper1.example.com:2181,zookeeper2.example.com:2181,zookeeper3.example.com:2181
Welcome to ZooKeeper!
JLine support is disabled
rmr /hbase
quit
Quitting...
-
Start HBase
-
Verify HBase contents—use the HBase shell to list tables and scan some known values.
### [](#_rollback_after_hdfs_downgrade)12.4. Rollback after HDFS downgrade
If you will be performing an HDFS downgrade, then you’ll need to follow these instructions regardless of whether ZooKeeper goes through rollback, downgrade, or reinstallation.
Requirements
-
Ability to downgrade HDFS
-
Pre-upgrade cluster must be able to run MapReduce jobs
-
HDFS super user access
-
Sufficient space in HDFS for at least two copies of the HBase data directory
Before upgrade
Before beginning the upgrade process, you must take a complete backup of HBase’s backing data. The following instructions cover backing up the data within the current HDFS instance. Alternatively, you can use the distcp command to copy the data to another HDFS cluster.
-
Stop the HBase cluster
-
Copy the HBase data directory to a backup location using the [distcp command](https://hadoop.apache.org/docs/current/hadoop-distcp/DistCp.html) as the HDFS super user (shown below on a security enabled cluster)
Using distcp to backup the HBase data directory
[hpnewton@gateway_node.example.com ~]$ kinit -k -t hdfs.keytab hdfs@EXAMPLE.COM
[hpnewton@gateway_node.example.com ~]$ hadoop distcp /hbase /hbase-pre-upgrade-backup
-
Distcp will launch a mapreduce job to handle copying the files in a distributed fashion. Check the output of the distcp command to ensure this job completed successfully.
Performing a rollback
-
Stop HBase
-
Perform a downgrade for HDFS and a downgrade/rollback for ZooKeeper (HBase should remain stopped)
-
Change the installed version of HBase to the previous version
-
Restore the HBase data directory from prior to the upgrade as the HDFS super user (shown below on a security enabled cluster). If you backed up your data on another HDFS cluster instead of locally, you will need to use the distcp command to copy it back to the current HDFS cluster.
Restore the HBase data directory
[hpnewton@gateway_node.example.com ~]$ kinit -k -t hdfs.keytab hdfs@EXAMPLE.COM
[hpnewton@gateway_node.example.com ~]$ hdfs dfs -mv /hbase /hbase-upgrade-rollback
[hpnewton@gateway_node.example.com ~]$ hdfs dfs -mv /hbase-pre-upgrade-backup /hbase
-
Clean out ZooKeeper information related to HBase. WARNING: This step will permanently destroy all replication peers. Please see the section on HBase Replication under Caveats for more information.
Clean HBase information out of ZooKeeper
[hpnewton@gateway_node.example.com ~]$ zookeeper-client -server zookeeper1.example.com:2181,zookeeper2.example.com:2181,zookeeper3.example.com:2181
Welcome to ZooKeeper!
JLine support is disabled
rmr /hbase
quit
Quitting...
-
Start HBase
-
Verify HBase contents–use the HBase shell to list tables and scan some known values.
## [](#_upgrade_paths)13. Upgrade Paths
### [](#upgrade3.0)13.1. Upgrade from 2.x to 3.x
The RegionServer Grouping feature has been reimplemented. See section
[Migrating From Old Implementation](#migrating.rsgroup) in [Apache HBase Operational Management](#ops_mgt) for more details.
The hbase:namespace table has been removed and fold into hbase:meta . See section
[About hbase:namespace table](#namespace_table) in [Data Model](#datamodel) for more details.
There is no special consideration upgrading to hbase-2.4.x from 2.3.x. And for earlier versions,
just follow the [Upgrade from 2.0.x-2.2.x to 2.3+](#upgrade2.3) guide. In general, 2.2.x should be rolling upgradeable, for 2.1.x
or 2.0.x, you will need to clear the [Upgrade from 2.0 or 2.1 to 2.2+](#upgrade2.2) hurdle first.
### [](#upgrade2.3)13.2. Upgrade from 2.0.x-2.2.x to 2.3+
There is no special consideration upgrading to hbase-2.3.x from earlier versions. From 2.2.x, it should be
rolling upgradeable. From 2.1.x or 2.0.x, you will need to clear the [Upgrade from 2.0 or 2.1 to 2.2+](#upgrade2.2) hurdle first.
#### [](#upgrade2.3_zookeeper)13.2.1. Upgraded ZooKeeper Dependency Version
Our dependency on Apache ZooKeeper has been upgraded to 3.5.7
([HBASE-24132](https://issues.apache.org/jira/browse/HBASE-24132)), as 3.4.x is EOL. The newer 3.5.x
client is compatible with the older 3.4.x server. However, if you’re using HBase in stand-alone
mode and perform an in-place upgrade, there are some upgrade steps
[documented by the ZooKeeper community](https:/