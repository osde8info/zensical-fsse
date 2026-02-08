---
title: "#mysql #mysqldump command"
date: 2013-06-14
categories: 
  - "fsse"
tags: 
  - "db"
  - "dba"
  - "mysql"
  - "mysqldump"
---

my favorite mysql mysqldump command

```
$ mysqldump -p --compatible=ansi --skip-quote-names \
--skip-extended-insert --no-create-info --skip-set-charset \
MYDATABASE MYTABLE
```

http://dev.mysql.com/doc/refman/5.5/en/mysqldump.html
