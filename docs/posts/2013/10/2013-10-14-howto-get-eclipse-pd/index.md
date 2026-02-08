---
title: "howto get #eclipse #pdt open declaration [F3] working again with #php files"
date: 2013-10-14
categories: 
  - "fsse"
tags: 
  - "eclipse"
  - "ide"
  - "php"
  - "webdev"
---

howto get #eclipse 4.3.1 #pdt 3.2.0 open declaration \[F3\] working again with #php files

look in your eclipse logfile do you see :

```
!ENTRY org.eclipse.dltk.core.index.sql 4 0 2013-10-14 16:45:28.670
!MESSAGE An exception has thrown while performing a search
!STACK 0
org.h2.jdbc.JdbcSQLException: 
Unsupported database file version or invalid file header in file "Old database: 
/home//workspace/.metadata/.plugins/org.eclipse.dltk.core.index.sql.h2/model.data.db 
- 
please convert the database to a SQL script and re-create it." [90048-168]
at org.h2.message.DbException.getJdbcSQLException(DbException.java:329)
```

if so

just delete your model.h2.db files as per

- http://www.eclipse.org/forums/index.php/m/1065653/#msg\_1065653
- http://www.eclipse.org/forums/index.php/m/1137607/#msg\_1137607
