# AWS Relational Database Service (RDS)


## Aurora

### 查詢 Aurora 版本

***MySQL***

```
select AURORA_VERSION();
select @@aurora_version;
```

***PostgreSQL***

```
SELECT AURORA_VERSION();
```

### 參考資料
* [Amazon Aurora 概述 - Amazon Relational Database Service](https://docs.aws.amazon.com/zh_cn/AmazonRDS/latest/UserGuide/Aurora.Overview.html)
* [利用Mycat中间件实现RDS MySQL的分库分表及读写分离功能 | 亚马逊AWS官方博客](https://aws.amazon.com/cn/blogs/china/mycat-rds-mysql/)
* [Amazon Aurora MySQL Database Engine Updates - Amazon Relational Database Service](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/AuroraMySQL.Updates.html)
* [Amazon Aurora MySQL 2.0 Database Engine Updates - Amazon Relational Database Service](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/AuroraMySQL.Updates.20Updates.html)
