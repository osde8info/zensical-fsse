---
title: "in #centos 6.x #percona 5.x #phpmyadmin 4.x reads config file from a new directory #dba #devops #sysadmin"
date: 2015-10-09
categories: 
  - "fsse"
tags: 
  - "centos"
  - "config"
  - "dba"
  - "devops"
  - "percona"
  - "phpmyadmin"
  - "sysadmin"
---

in #centos 6.x #percona 5.x #phpmyadmin 4.x reads its config file from a completely different directory - it is no longer in the phpmyadmin code directory

ACTUAL centos 6 percona 5 phpmyadmin 4 config files are as follows

- phpMyAdmin httpd - /etc/httpd/conf.d/phpMyAdmin.conf
- phpMyAdmin conf - /etc/phpMyAdmin/config.inc.php
- phpMyAdmin code - /usr/share/phpMyAdmin/

See also

- https://www.howtoforge.com/perfect-server-centos-6.5-apache2-mysql-php-pureftpd-postfix-dovecot-and-ispconfig3
- https://www.digitalocean.com/community/tutorials/how-to-install-and-secure-phpmyadmin-on-a-centos-6-4-vps
- https://www.percona.com/doc/percona-server/5.5/installation/yum\_repo.html
