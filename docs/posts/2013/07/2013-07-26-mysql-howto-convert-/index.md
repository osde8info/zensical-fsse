---
title: "#mysql howto convert a database and it tables to #utf8"
date: 2013-07-26
categories: 
  - "fsse"
tags: 
  - "charset"
  - "db"
  - "dba"
  - "mysql"
  - "utf8"
---

DUMP mysqldump -h 127.0.0.1 -uMYUSER --skip-quote-names --skip-comments --skip-extended-insert MYDATABASE > db.sql

MODIFY mysql > alter database MYDATABASE character set = utf8 collate = utf8\_general\_ci;

PATCH sed "s/ENGINE=MyISAM/ENGINE=InnoDB/g" < db.sql > db2.sql sed "s/DEFAULT CHARSET=latin1;/;/g" < db2.sql > db3.sql sed "s/CHARACTER SET utf8 COLLATE utf8\_bin//g" < db3.sql > db4.sql

.MY.CNF \[client\] default-character-set=utf8

RESTORE mysql -h 127.0.0.1 -uMYUSER < db4.sql

CHECK NEW SETTINGS mysql > show variables

```
| character_set_client                    | utf8                       
| character_set_connection                | utf8                       
| character_set_database                  | utf8                       
| character_set_filesystem                | binary                     
| character_set_results                   | utf8                       
| character_set_server                    | latin1                     
| character_set_system                    | utf8                    
   
| collation_connection                    | utf8_general_ci            
| collation_database                      | utf8_general_ci            
| collation_server                        | latin1_swedish_ci
```

Refs

- http://dev.mysql.com/doc/refman/5.1/en/charset-syntax.html
- http://dev.mysql.com/doc/refman/5.1/en/charset-server.html
- http://dev.mysql.com/doc/refman/5.1/en/charset-database.html
- http://dev.mysql.com/doc/refman/5.1/en/charset-literal.html
