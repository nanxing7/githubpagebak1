---
title: 常用MySQL数据库语法
date: 2019-10-03 12:02:30
tags: 
categories:
- 数据库
- MySQL
---

连接数据库
```sql
mysql -u root -p
```

编辑114sdhshd

显示所有数据库
```sql
SHOW DATABASES;
```

显示数据库中所有表
```sql
SHOW TABLES;
```

选择数据库
```sql
USE 数据库名；
```

获取表结构
```sql
desc <表名>
或者
SHOW COLUMNS FROM <表名>;
```

```slq
CREATE DATABASE <数据库名>
DROP DATABASE <数据库名>
```

```sql

```

约束条件
```sql
ALTER TABLE <表名> DROP FOREIGN KEY <外键约束名>
ALTER TABLE <表名> DROP PRIMARY KEY
ALTER TABLE <表名> DROP {约束名|候选键字段名}
```

外键的添加
```sql
FOREIGN KEY(添加的列) REFERENCES 关联的表(关联的列) ON DELETE RESTRICET ON UPDATE RESTRICT
FOREIGN KEY(pro_id) REFERENCES pro(id) ON DELETE RESTRICET ON UPDATE RESTRICT
```

触发器
删除触发器
```sql
DROP TRIGGER [IF EXIST] 
```
创建触发器
```sql
CREATE TRIGGER add_test AFTER INSTER ON test FOR EACH row set @x='OK'
```