---
title: "howto upgrade apache 2.2 to apache 2.4 and php 5.6 on centos, oracle uek and redhat gnu/linux"
date: 2016-04-01
categories: 
  - "fsse"
tags: 
  - "devops"
  - "lamp"
  - "sysadmin"
  - "webdev"
---

howto upgrade apache 2.2 to apache 2.4 and php 5.6 on centos, oracle uek and redhat gnu/linux

add extra repos, remove apache 2.2, install apache 2.4 & php 5.6, workaround mod\_dnssd error

```
  wget https://dl.iuscommunity.org/pub/ius/stable/Redhat/6/x86_64/epel-release-6-5.noarch.rpm
  rpm -ivh epel-release-6-5.noarch.rpm

  wget https://dl.iuscommunity.org/pub/ius/stable/Redhat/6/x86_64/ius-release-1.0-14.ius.el6.noarch.rpm
  rpm -ivh ius-release-1.0-14.ius.el6.noarch.rpm 

  yum remove httpd
  yum remove httpd-tools

  yum install php56u-fpm-httpd.noarch

  system-config-firewall

  yum remove mod_dnssd

  service httpd start
```

```
  service php-fpm start

```

```
  chkconfig httpd on
```

```
  chkconfig php-fpm on
```

this worksaround the error

```
Starting httpd: 
httpd: Syntax error on line 353 of /etc/httpd/conf/httpd.conf: 
Syntax error on line 1 of /etc/httpd/conf.d/mod_dnssd.conf: 
Cannot load modules/mod_dnssd.so into server: 
/etc/httpd/modules/mod_dnssd.so: undefined symbol: unixd_setup_child

```
