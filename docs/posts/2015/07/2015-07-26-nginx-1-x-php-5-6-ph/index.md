---
title: "nginx 1.x php 5.6 phpmyadmin 4.x"
date: 2015-07-26
categories: 
  - "fsse"
---

after installing nginx, php56u and php-fpm you may need to

yum install php56u-mbstring php56u-mcrypt php56u-mysqlnd php56u-pdo

then

service php-fpm restart
