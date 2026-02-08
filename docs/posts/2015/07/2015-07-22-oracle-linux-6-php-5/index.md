---
title: "oracle linux 6 php 5.6 install"
date: 2015-07-22
categories: 
  - "fsse"
tags: 
  - "5-6"
  - "install"
  - "oracle-linux"
  - "php"
---

for an oracle linux 6 php 5.6 install you will need to add some extra yum repos

- http://www.if-not-true-then-false.com/2010/install-apache-php-on-fedora-centos-red-hat-rhel/comment-page-3/

then

- EPEL – [https://dl.fedoraproject.org/pub/epel/6Server/](https://dl.fedoraproject.org/pub/epel/6Server/)
- IUSC – [https://iuscommunity.org/pages/About.html](https://iuscommunity.org/pages/About.html)
- REMI – [http://rpms.famillecollet.com/enterprise/remi-release-6.rpm](http://rpms.famillecollet.com/enterprise/remi-release-6.rpm)

then

```
# yum install php56-cli
```
