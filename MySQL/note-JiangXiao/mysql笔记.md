# MySQL学习笔记

## 源码编译

依赖版本:

- Mac OS Catalina 10.15.7
- cmake 3.15.4
- boost 1.73.0
- openssl 1.1

编译版本:

mysql-server branch 8.0 commit ee4455a33b10f1b1886044322e4893f587b319ed

编译前请确保安装了[boost](https://www.boost.org/)和[openssl](https://www.openssl.org/)，并使用环境变量或者编译选项的方式指定二者所在文件夹路径。

```bash
> (mysql-server) export OPENSSL_ROOT_DIR=/usr/local/opt/openssl@1.1
> (mysql-server) mkdir bld
> (mysql-server/bld) cd bld
> (mysql-server/bld) cmake .. -DWITH_BOOST=/usr/local/boost_1_73_0
> (mysql-server/bld) make
```

其中`OPENSSL_ROOT_DIR`和`WITH_BOOST`的路径为我的本机路径，请自行调整。

## 源码编译与安装存储引擎

编写了一个定制化存储引擎后，需要将其编译并安装到MySQL中。

为了成功编译存储引擎，需要在`storage/<SE_name>`中编写源代码和CMake文件。其中，CMake文件格式如下:

```cmake
MYSQL_ADD_PLUGIN(<plugin_name> <sources> STORAGE_ENGINE)
```

其中用到的CMake宏`MYSQL_ADD_PLUGIN`具体实现细节可以在`cmake/plugin.cmake`中找到。

编译与安装流程

```bash
> (mysql-server/bld) make # 编译，同时编译了mysql和SE，SE被编译为.so文件
> (mysql-server/bld) make install # 安装mysql到本机，SE被安装到/usr/local/mysql/lib/plugin/文件夹下
> (mysql-server/bld) cd /usr/local/mysql/bin
> (mysql/bin) sudo ./mysqld_safe &
> (mysql/bin) ./mysql -uroot -p
> (./mysql) INSTALL  PLUGIN foo SONAME 'ha_foo.so'; # 安装SE
```

最后几步涉及到mysql的启动，登录以及SE的名称，这些需要根据实际情况进行调整。
