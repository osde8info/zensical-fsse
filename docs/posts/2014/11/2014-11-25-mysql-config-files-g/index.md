---
title: "mysql config files, global, commandline options and session variables"
date: 2014-11-25
categories: 
  - "config"
  - "ini"
  - "mysql"
  - "options"
  - "variables"
---

you seem to be able to set global and command line options variables in mysql config files but not session variables so you'll need to create a .my.cnf file with your favorite global and command line options and a separate mysql.sql file with your favorite session variables and source it once logged in

ie

.my.cnf

```
[mysql]
user=user
password=password

```

mysql.sql

```
#
set sql_quote_show_create=OFF

```

mysql

```
mysql> source ~/mysql.sql

```

see also

https://dev.mysql.com/doc/refman/5.5/en/option-files.html
