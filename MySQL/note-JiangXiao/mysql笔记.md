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
