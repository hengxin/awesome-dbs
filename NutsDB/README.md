# NutsDB

NutsDB is a transactional key/value store database written in Go. All transactions executed in NutsDB are fully serializable. Transactions are categorized into types based on their level of access. In other words, there are read-only and read-write transactions. Multiple read-only transactions are allowed at the same time, and they could, of course, read values from a bucket using a key or…

## 基本信息

- **数据库类型**: KV
- **所属机构**: Jiajun Xu
- **许可证**: Apache v2
- **首次发布**: 2018
- **国家/地区**: CN

## 官网与文档

- [官网](https://xujiajun.cn/nutsdb)
- [官方文档](https://xujiajun.cn/nutsdb)
- [GitHub](https://github.com/nutsdb/nutsdb)

## 数据源

- [Database of Databases](https://dbdb.io/db/nutsdb)
