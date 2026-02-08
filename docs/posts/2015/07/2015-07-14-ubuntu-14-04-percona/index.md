---
title: "ubuntu 14.04 percona 5.5 enable remote tcp access"
date: 2015-07-14
categories: 
  - "fsse"
tags: 
  - "mysql"
  - "percona"
  - "tcp"
---

https://www.percona.com/doc/percona-xtrabackup/2.1/howtos/enabling\_tcp.html

ubuntu 14.04 percona 5.5 enable remote access

vi /etc/mysql/my.cnf

comment out bind-address

```
# bind-address        = 127.0.0.1
```

then

```
# service mysql restart
# netstat -lnp | grep mysql
```
