# mysql内核学习
## MySQL插件plugin
* ### 资源
  * \plugin 目录下定义了插件例子 daemon_example
  * [插件在mysql运行中作用的位置](https://www.cnblogs.com/FateTHarlaown/p/8718602.html)
  * [~~简易自定义插件方法~~](https://baijiahao.baidu.com/s?id=1641643231166978250&wfr=spider&for=pc) 
* ### 半同步复制插件如何在mysql中生效     
    半同步复制以插件形式支持，开启后可设置 `rpl_semi_sync_master_wait_point = WAIT_AFTER_SYNC`，此时事务同步binlog后才开始接收从库ack。   
    开启binlog后，`MYSQL_BIN_LOG::ordered_commit()`进行事务提交操作
    ```
    sql\binlog.cc   MYSQL_BIN_LOG::ordered_commit()
    sql\binlog.cc       call_after_sync_hook(commit_queue);
    sql\binlog.cc           RUN_HOOK() #宏
    sql\rpl_handler.cc         Binlog_storage_delegate::after_sync()
    sql\rpl_handler.cc             FOREACH_OBSERVER() #宏
    sql\rpl_handler.cc                 observer->after_sync()
    ```
    * `RUN_HOOK()`是宏，展开后： `binlog_storage_delegate->is_empty() ? 0 : binlog_storage_delegate->after_sync()`，
    * `binlog_storage_delegate` 指针在 `delegates_init()`中设置，mysql 启动后会初始化：`mysqld_main()`$\to$ `init_server_components()`$\to$ `delegates_init()`   
  * `Binlog_storage_delegate` 类   
    - 基类：`Delegate`，包含了`observer_info_list` 链表以及对该链表的一系列操作函数，链表元素为 `Observer_info` 类型   
    - `after_sync()`：成员函数，调用宏 `FOREACH_OBSERVER()`，该宏遍历 `observer_info_list` 链表，取出表中每个元素 `observer`，然后调用 `observer` 的成员函数 `after_sync` 进行半同步复制的等待。   

   半同步复制插件定义了一个 `observer`：`storage_observer`，然后调用 `sql\rpl_handler.cc` 文件中的函数 `'register_binlog_storage_observer(arg)'` 将该实例注册到 `binlog_storage_delegate` 的链表中。   
    因此，mysql 将事务提交过程分段完成，段间提供了调用插件的接口，因此半同步复制可以以插件形式运行。   
    若在分布式事务开始、访问新节点、提交的实现函数中也提供了类似的接口，则Distributed SI可以插件形式完成。

# MySQL源码阅读
* 官方文档
  * [文档](https://dev.mysql.com/doc/)
  * [扩展：Extending Mysql 8.0](https://dev.mysql.com/doc/extending-mysql/8.0/en/)
  * [代码导航：MySQL Internals](https://dev.mysql.com/doc/internals/en/)
* 网络资源
  * [MySQL源码阅读1234](https://www.zhihu.com/people/wenguangliu/posts)
  * [mysql8.0关键函数和执行流程](https://blog.csdn.net/jygqm/article/details/82620112)
  * [源代码阅读笔记-博客](https://blog.csdn.net/theorytree)
  * [编译运行-阅读入口](https://blog.csdn.net/happylzs2008/article/details/88252821)
  * [源码分析入门](https://blog.csdn.net/feivirus/article/details/83716680?utm_medium=distribute.pc_relevant.none-task-blog-searchFromBaidu-1.control&depth_1-utm_source=distribute.pc_relevant.none-task-blog-searchFromBaidu-1.control)
  * [src layouts](https://oxnz.github.io/2016/07/20/mysql-primer-source)
  * [CSDN博主 冰河 - 分布式事务相关文章](https://blog.csdn.net/l1028386804/category_9755213.html?spm=1001.2014.3001.5482)
  * [淘宝数据库月报](http://mysql.taobao.org/monthly/)
  * [从源码角度轻松认识mysql整体框架图](https://mp.weixin.qq.com/s?__biz=MzAwNTMxMzg1MA==&mid=2654078593&idx=4&sn=2a033dc472838b0123a403d1d6255077&chksm=80d822d4b7afabc2ae245cac55ee33f07dee162775732d02f2d773587348c02055c425b35538&mpshare=1&scene=23&srcid=0303DcHINzIJ0DtbKeuDixNs&sharer_sharetime=1614758474236&sharer_shareid=dd2be4103c603bc61de89fb0f23e10e6#rd)
* 书籍
  * [MySQL运维内参](../ref/MySQL运维内参：MySQL、Galera、Inception核心原理与最佳实践.pdf)
  * [2007年分析书籍：Understanding MySQL Internals](../ref/Understanding.MySQL.Internals.Apr.2007.pdf)
* 
# 目录
  * client：客户端工具
    * `mysql.cc` 命令行工具
    * `mysqladmin.cc` 数据库维护
    * `mysqlshow.cc` 数据库展示
    * ...
  * storage/myisam：一种存储引擎，其目录结构近似为模板，所有存储引擎的源代码在此storage目录
    * mi开头的文件较为重要
    * 文件处理程序：`mi_open.cc,mi_close.cc,...`
    * 行处理程序：`mi_delete.cc,mi_write.cc,...`
    * key处理程序：`mi_key.cc,mi_rkey.cc,...`
  * mysys：MySQL System Library，工具库
  * sql：mysql服务器主要代码，包含了main
    * parser：`sql_lex.cc,sql_yacc.yy,...`
    * handler
  * vio：virtual I/O，不同协议的网络I/O接口
  * sql-common：存放部分服务器端和客户端都会用到的代码
  * unittest：单元测试文件目录
  * 
## 代码流程(从client开始，未完成)：
win的vscode设置c_cpp_properties.json的"compilerPath"为cgwin的g++，使得代码智能显示为 `!_WIN32`
* 启动
```
sql/main.cc     main()
```
* 目录流程
```
 User enters "INSERT" statement     /* client */   
 |
 Message goes over TCP/IP line      /* vio, various */
 |
 Server parses statement            /* sql */
 |
 Server calls low-level functions   /* mysys */
 |
 Handler stores in file             /* myisam */
```
* 执行流程 
  * `mysql/mysql.cc:main()`：命令行工具
  ```c++
  int main(int argc, char *argv[]) {

    if (get_options(argc, (char **)argv)) {  //获取user, pwd等
        my_end(0);
        return EXIT_FAILURE;
    }
    
    //连接服务器
    if (sql_connect(current_host, current_db, current_user, opt_password,opt_silent)) {  				
    	quick = 1;  // Avoid history
    	status.exit_status = 1;
    	mysql_end(-1);
  	}
 
    status.exit_status = read_and_execute(!status.batch); //读取命令并执行
 
    mysql_end(0); //关闭连接
  }
  ```
  * `mysql/mysql.cc:read_and_execute()`
  ```c++
  static int read_and_execute(bool interactive) {

    for (;;) {
      line = batch_readline(status.line_buff, real_binary_mode);//读取一行

      //将line复制到buffer,检查并执行
      if (add_line(glob_buffer, line, line_length, &in_string, &ml_comment,
                 status.line_buff ? status.line_buff->truncated : false))
      break;
    }
  }
  ```
  * `mysql/mysql.cc:add_line()`
  ```c++
  static bool add_line(String &buffer, char *line, size_t line_length,
                     char *in_string, bool *ml_comment, bool truncated) {

    for (;;) {
      line = batch_readline(status.line_buff, real_binary_mode);//读取一行

      //将line复制到buffer,检查并执行
      if (add_line(glob_buffer, line, line_length, &in_string, &ml_comment,
                 status.line_buff ? status.line_buff->truncated : false))
      break;
    }
  }
  ```
```
client/mysql.cc   main()
sql/mysqld.cc     mysqld_main()
/sql/mysqld.cc
/sql/sql_parse.cc   do_command() [->] dispatch_command()
/sql/sql_prepare.cc
/sql/sql_insert.cc
/sql/ha_myisam.cc
/myisam/mi_write.c
```

# Understanding MySQL Internals 笔记
## MySQL Architecture
* Core Modules
  * Initialization Module：加载配置，分配内存，初始化结构、变量，加载访问控制表，一系列初始化工作,->
  * Connection Manager：监听clients，执行网络协议任务,->
  * Thread Manager：支持线程处理连接,->
  * Connection Thread：调用Authentication Module，调用Command Dispatcher
  * Authentication Module
  * Command Dispatcher：分发command
  * Logging Module：在dispatch前记录query和command
  * Query Cache Module：检查是否需要缓存，是否已有该结果
  * Optimizer：接收Slect query
  * Table Modification Module：update, insert, table creation, schema-altering query
  * Table maintenance Module：check, repair等统计数据，碎片整理
  * Replication Module：涉及到复制的query
  * Status Reporting Module：回应状态请求
  * Replication master module：处理线程返回从库请求
  * Replication slave module：
  * 
* query vs command
  * query：要经过parser，如SELECT, DELETE, INSERT
  * command：无需parser可执行
* 每个接收Parser消息的module发送query涉及到的table到Access Control Module，如果成功则交给Table Manager。Table Manager发起一系列操作请求到Storage Engine Module，
## Classes, Structures
* THD：线程描述符，包含该线程信息
  * [THD对象](https://zhuanlan.zhihu.com/p/115054892)
  * 基类1：MDL_context_owner：MDL(元数据锁) module
  * 基类2：Query_arena：
  * 基类3：Open_tables_state：
  * LEX* lex : parse tree descriptor
  * LEX_CSTRING m_query_string : includes current query and length
  * String m_rewritten_query：m_query_string改写后
* NET
* TABLE
* FIELD
# 启动流程 in linux
## 精简版 sql/mysqld.cc
```c++
int mysqld_main(int argc, char **argv){
  //->fun()是my_init()函数中调用
  if(my_init())
    -> my_thread_global_init()
    -> my_thread_init()

  // 处理配置文件及启动参数等
  if (load_defaults(...))
  
  //继续处理参数变量
  heo_error = handle_early_options();

  //将命令存储在sql_statement_names全局数组里,命令种类参考my_sqlcommand.h
  init_sql_statement_names();

  sys_var_init();

  mysql_audit_initialize();

  //日志系统初始化
  query_logger.init();

  // 初始化很多系统内部变量
  if (init_common_variables()) 

  /* 信号系统初始化 */
  my_init_signals();  
    
  /* 核心模块启动，包括存储引擎等 */
  if (init_server_components()) unireg_abort(MYSQLD_ABORT_EXIT);

  /* 网络系统初始化 */
  if (network_init()) unireg_abort(MYSQLD_ABORT_EXIT);

  /* 状态变量初始化 */
  init_status_vars();
  
  /* Binlog相关检查初始化 */
  check_binlog_cache_size(nullptr);
  check_binlog_stmt_cache_size(nullptr);
  binlog_unsafe_map_init();

  // 开始信号处理线程
  start_signal_handler();

  // 开始 handle manager线程
  start_handle_manager();

  //******
  /* 服务监听线程创建 */
  setup_conn_event_handler_threads();
  
  // Notify the signal handler that we have stopped listening for connections.
  mysql_mutex_lock(&LOCK_socket_listener_active);
  socket_listener_active = false;
  mysql_cond_broadcast(&COND_socket_listener_active);
  mysql_mutex_unlock(&LOCK_socket_listener_active);
  
  // join shutdown thread
  if (signal_thread_id.thread != 0)
    ret = my_thread_join(&signal_thread_id, nullptr);

  //退出
  clean_up(true);
  sysd::notify("STATUS=Server shutdown complete");
  mysqld_exit(signal_hand_thr_exit_code);
}
```
* `load_defaults()`：从默认配置文件和命令行中读取配置项(option)并缓存
  ```c++
  //过程中使用argv_alloc存储各种信息:dirs,args等，最后将args复制到argv
  load_defaults(MYSQL_CONFIG_NAME, load_default_groups, &argc, &argv,&argv_alloc)
    my_load_defaults(conf_file, groups, argc, argv, alloc,&default_directories)
      // 初始化默认目录(如/etc)，dirs存储在alloc分配的内存
      dirs = init_default_directories(alloc)
      // 搜索所有设置文件，设置信息存入ctx中
      // false是指定参数is_login_file，若用户指定了--login-path则会使用login-file存储的信息登录
      my_search_option_files(conf_file, argc, argv, &args_used,
                                      handle_default_option, (void *)&ctx, dirs,
                                      false, found_no_defaults)
        //获取诸如--delaults-file之类的选项
        get_defaults_options(...)
        
        // ***_with_ext()打开配置文件并解析每一行，存储到func_ctx中
        // func是handle_default_option()函数，负责读取选项
        // func_ctx是传入的ctx(handle_option_ctx结构体)，存储参数
        search_default_file_with_ext(func, func_ctx...)
      
      最后按：配置文件参数(my_args)+分隔符(arg_sep)+命令行参数(argv)，更新argv个argc
  ```   
  * `load_defaults()`调用子过程使用的结构体了。
    ```c++
    `handle_option_ctx`结构体用来存储参数信息(option+group)并传递
    struct handle_option_ctx {
      MEM_ROOT *alloc;  // 最终缓存参数的地址，为传入的argv_alloc，m_args只是中间介质，相当于alloc分配内存的一块
      My_args *m_args;  // 参数存储在为m_args
      TYPELIB *group;   // 组信息
    };
    //My_args是类型安全的动态数组，用于表示和存储option
    typedef Prealloced_array<char *, 100> My_args;
    ```
  * `load_default()`执行后，`argc`和`argv`会更新为所有获取的配置项

* `handle_early_options()`
  * `my_option`：选项结构体
    ```c++
    struct my_option {
      const char *name;// 名字
      int id; 
      void *value;  //值
      ulong var_type; /**< GET_BOOL, GET_ULL, etc */
      longlong def_value; /**< Default value */
      ...
    }
    ```
  * `handle_early_options()`
  ```c++
  static int handle_early_options() {
    vector<my_option> all_early_options;

    //遍历所有系统变量，变量的选项为 PARSE_EARLY的放入all_early_options
    sys_var_add_options(&all_early_options, sys_var::PARSE_EARLY);
    
    //将my_long_early_options的成员加入all_early_options
    for (my_option *opt = my_long_early_options; opt->name != nullptr; opt++)
      all_early_options.push_back(*opt);
    
    //remaining_argc, remaining_argv是更新后的argc和argv
    //handle_options()将根据和EARLY匹配的argv选项进行一些设置，如 global_system_variables
    ho_error = handle_options(&remaining_argc, &remaining_argv,
                            &all_early_options[0], mysqld_get_one_option);
  }
  ```
  * 选项按使用顺序分为`PARSE_EARLY`和`PARSE_NORMAL`两种，`EARLY` 类型的选项在启动时要使用，因此提前处理。
  * early参数会被放在临时向量`all_early_options`里

* `init_sql_statement_names()`：遍历`enum_sql_command`中定义的所有SQL命令，然后从`com_status_vars[]`中提取命令名(`string`类型)和长度，保存在全局数组`sql_statement_names`中
    * `sql_statement_names[]`：全局数组，`LEX_CSTRING[]` 类型
    * `com_status_vars[]`：全局数组，`SHOW_VAR[]`类型，SQL命令是`com_status_vars`的一部分
    * `System_status_var`：结构体类型，可表示所有的状态变量的
    * `sql_statement_names`元素：`{admin_commands,len}`，`{alter_table,11}`，...

* `sys_var_init()`
  * `all_sys_vars`是一个单链表存储所有系统变量，将`all_sys_vars`的所有变量存入哈希表`system_variable_hash`
  * `handle_options()`
* 数据结构
  * `Prealloced_array`：class类型，是类型安全的动态数组
  * `System_status_var`：系统状态变量，包含一些统计信息
  ```c++
  struct System_status_var{
    ulonglong created_tmp_disk_tables;
    ulonglong created_tmp_tables;
    ulonglong ha_commit_count;
    ...
    ulong com_stat[(uint)SQLCOM_END];
  }
  ```
  * `enum_sql_command`：SQL Commands
  ```c++
  enum enum_sql_command {
    SQLCOM_SELECT,
    SQLCOM_CREATE_TABLE,
    SQLCOM_CREATE_INDEX,
    ...
    SQLCOM_END
  };
  ```
  * `SHOW_VAR`：表示一种用来SHOW STATUS的变量
  ```c++
  // SHOW STATUS Server status variable
  struct SHOW_VAR {
    const char *name;
    char *value;
    enum enum_mysql_show_type type; //SHOW_INT,SHOW_LONGLONG,...
    enum enum_mysql_show_scope scope; //SHOW_SCOPE_UNDEF,SHOW_SCOPE_GLOBAL,...
  };
  ```
## 细致版 sql/mysqld.cc 
```c++
1. 设置路径、发送启动消息
    substitute_progpath(argv);//替换成全路径的程序名
    sysd::notify_connect();// 在环境变量NOTIFY_SOCKET中查找socket的文件名并连接 
    sysd::notify()//向Notify Socket发送正在启动的消息
2. 初始化my_sys函数、资源、变量
    my_init() // init my_sys library & pthreads
3. 加载配置，缓存配置
    load_delaults()：配置文件中读取配置项
    persisted_variables_cache：持久化的参数配置缓存，采用JSON进行存储
4. 初始化pfs配置数组
    init_pfs_instrument_array
5. 处理需要先设置的选项(参数)
    handle_early_options
6. 初始化命令：将命令存储在sql_statement_names全局数组中
    init_sql_statement_names
7. 初始化系统变量
    sys_var_init
8. 初始化错误日志
    init_error_log
9. 调整相关参数
    adjust_related_options
10. 初始化performance schema
    initialize_performance_schema
11. 初始化Lock Order：Lock Order graph 描述依赖关系
    LO_init
12. 设置psi相关服务：thread_service, mutex_service等
13. 注册服务工具：init_server_psi_keys
14. 重新初始化锁：my_thread_global_reinit
15. component_infrastructure_init
16. register_pfs_notification_service 
17. register_pfs_resource_group_service 
18. Resource_group_mgr::init：初始化资源组管理器，
19. 调用psi_thread_service相关函数
20. Resource_group_mgr->init：初始化资源组管理器，
    与资源相关的服务
	  注册线程创建/断开连接的回调
	  创建用户级/系统级的资源组对象
21. 调用psi_thread_service相关函数
22. mysql_audit_initialize:初始化与audit相关的变量；
23. Srv_session::module_init：初始化srv_session模块
24. query_logger.init：查询日志初始化
25. init_common_variables： 
    init_thread_environment：初始化与线程相关的锁； 
    mysql_init_variables：初始化全局变量为缺省值 
    mysql_bin_log.set_psi_keys完成bin log的初始化，让仪表相关的对bin log可见 
    mysql_bin_log.init_pthread_objects：初始化bin log与线程相关的锁 
    get_options，剩余的可选项，binlog，压缩算法，页的大小，线程缓存大小，back_log 
      Connection_handler_manager::init,初始化连接池
        Per_thread_connection_handler::init，初始化Per_thread_connection_handler，初始化锁
    初始化mysql client的plugin 
    选字符集/collation 
    日志配置 
    创建数据目录 
    表的大小写等
26. my_init_signals：初始化信号处理 
27. 线程栈大小检查
28. Migrate_keyring::init:初始化Migrate_keyring（一种mysql数据搬运模式）相关的，如压缩方式，并且连接到数据源主机 
    Migrate_keyring::execute  
29. set_ports:确定tcp端口
30. init_server_components
    mdl_init：metadata locking subsystem元数据锁子系统，
    table_def_init
    hostname_cache_init
    my_timer_initialize
    init_slave_list
    transaction_cache_init
    
寻找、设置、调整参数，从命令行和配置文件中获取设置项
    

    my_thread_global_init()：初始化线程的环境（初始化一堆资源锁PSI_mutex_key） 
    my_thread_init()：为线程分配内存，由mysys和debug调用

， 
```
# 缩写
* PSI：performance schema interface：performance schema(资源,性能使用情况) 接口
* PFS：performance storage
* DQL,DML,DDL,DCL：数据查询，操纵，定义，控制语言