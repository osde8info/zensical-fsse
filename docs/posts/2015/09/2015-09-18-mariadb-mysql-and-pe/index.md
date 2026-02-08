---
title: "mariadb, mysql and percona 5.5 general query and slow query logging"
date: 2015-09-18
categories: 
  - "fsse"
tags: 
  - "db"
  - "dba"
  - "logging"
  - "logs"
  - "mariadb"
  - "mysql"
  - "percona"
---

mariadb, mysql and percona 5.5 general query and slow query logging

- https://dev.mysql.com/doc/refman/5.5/en/log-destinations.html
- https://dev.mysql.com/doc/refman/5.5/en/server-system-variables.html#sysvar\_general\_log\_file
- https://dev.mysql.com/doc/refman/5.5/en/server-system-variables.html#sysvar\_slow\_query\_log\_file

```
mysql> select @@general_log;
+---------------+
| @@general_log |
+---------------+
|             1 |
+---------------+

mysql> select @@general_log_file;
+-------------------------------+
| @@general_log_file            |
+-------------------------------+
| /var/lib/mysql/data/query.log |
+-------------------------------+

mysql> select  @@slow_query_log;
+------------------+
| @@slow_query_log |
+------------------+
|                1 |
+------------------+

mysql> select @@slow_query_log_file;
+------------------------------------+
| @@slow_query_log_file              |
+------------------------------------+
| /var/lib/mysql/data/mysql-slow.log |
+------------------------------------+
```
