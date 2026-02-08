---
title: "ubuntu 14.04 (trusty) percona 5 install howto"
date: 2015-07-14
categories: 
  - "fsse"
tags: 
  - "db"
  - "dbadmin"
  - "howto"
  - "install"
  - "mysql"
  - "percona"
  - "ubuntu"
---

https://www.percona.com/doc/percona-server/5.5/installation/apt\_repo.html

howto switch from mysql 5 to percona 5 on ubuntu 14.04 trusty

remove mysql (if youve already installed it)

```
# aptitude remove mysql-client-5.5 mysql-client-core-5.5 mysql-workbench

```

install percona

```
# apt-key adv --keyserver keys.gnupg.net --recv-keys 1C4CBDCDCD2EFD2A
# vi /etc/apt/sources.list

  deb http://repo.percona.com/apt trusty main
  dpkg http://repo.percona.com/apt trusty main
  
# aptitude update
# aptitude install percona-server-client-5.5 percona-server-server-5.5

```
