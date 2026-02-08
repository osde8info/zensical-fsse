---
title: "#mysql #unixtime quirk unixtime(123) = 01:02:03"
date: 2013-06-25
categories: 
  - "fsse"
tags: 
  - "mysql"
  - "quirk"
  - "unixtime"
---

#mysql #unixtime quirk unixtime(123) = 01:02:03

```
mysql> select from_unixtime(0);+---------------------+| from_unixtime(0)    |+---------------------+| 1970-01-01 01:00:00 |+---------------------+1 row in set (0.00 sec)mysql> select from_unixtime(123);+---------------------+| from_unixtime(123)  |+---------------------+| 1970-01-01 01:02:03 |+---------------------+1 row in set (0.01 sec)
```
