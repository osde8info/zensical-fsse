---
title: "#sysadmin @webmin #webminstats historical system stats module install"
date: 2015-07-23
categories: 
  - "fsse"
tags: 
  - "sysadmin"
  - "webmin"
---

centos / oracle uek / red hat enterprise / ubuntu linux sysadmin webmin webminstats historic system stats module install howto

- http://www.webmin.com/cgi-bin/search\_third.cgi?category=System
- http://webminstats.sourceforge.net/

on ed/x/ubuntu you will need to install rrdtool

```
# aptitude install rrdtool
# aptitude install librrdtool-oo-perl
```

on centos/oracle uek/red hat you will need to install perl-CGI

```
# yum install perl-CGI
```

install webmin stats via webmin | webmin configuration | webmin modules | from ftp

```
http://downloads.sourceforge.net/webminstats/sysstats-2.12.tgz
```

if you are running webmin on a server behind a firewall you may need to create an ssh https tunnel before you can connect

```
$ ssh user@example.com -L 10000:localhost:10000 -N
```
