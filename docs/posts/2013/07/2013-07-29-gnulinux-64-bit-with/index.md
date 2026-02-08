---
title: "gnu/linux 64 bit with #mysql x86_64 will still break in #2038"
date: 2013-07-29
categories: 
  - "fsse"
tags: 
  - "2038"
  - "64-bit"
  - "gnu-linux"
  - "mysql"
  - "x86_64"
---

gnu/linux 64 bit with mysql x86\_64 will still break in 2038

```
SELECT UNIX_TIMESTAMP('2038-01-01'),UNIX_TIMESTAMP('2039-01-01'),UNIX_TIMESTAMP('2040-01-01');+------------------------------+------------------------------+------------------------------+| UNIX_TIMESTAMP('2038-01-01') | UNIX_TIMESTAMP('2039-01-01') | UNIX_TIMESTAMP('2040-01-01') |+------------------------------+------------------------------+------------------------------+|                   2145916800 |                            0 |                            0 |+------------------------------+------------------------------+------------------------------+1 row in set (0.01 sec)
```
