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
  * [Extending Mysql 8.0](https://dev.mysql.com/doc/extending-mysql/8.0/en/)
  * [MySQL Internals](https://dev.mysql.com/doc/internals/en/)
* 资源
  * [源代码阅读笔记-博客](https://blog.csdn.net/theorytree)
  * [编译运行-阅读入口](https://blog.csdn.net/happylzs2008/article/details/88252821)
  * [源码分析入门](https://blog.csdn.net/feivirus/article/details/83716680?utm_medium=distribute.pc_relevant.none-task-blog-searchFromBaidu-1.control&depth_1-utm_source=distribute.pc_relevant.none-task-blog-searchFromBaidu-1.control)
<!-- * mysql启动
```
sql/main.cc     main()
sql/mysqld.cc     mysqld_main()
```  -->
