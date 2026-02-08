---
title: "ubuntu aptitude doesnt install #php php5-mcrypt correctly but its a known bug"
date: 2016-02-08
categories: 
  - "fsse"
tags: 
  - "bug"
  - "mcrypt"
  - "nginx"
  - "php"
---

ubuntu aptitude doesnt install php5-mcrypt correctly and breaks php cli and nginx php fpm but its a known bug

bug

- https://bugs.launchpad.net/ubuntu/+source/php-mcrypt/+bug/1243568

workaround

- https://davekz.com/mcrypt-php-fpm-ubuntu/

or

```
# cd cli/conf.d/
# ln -s ../../mods-available/mcrypt.ini 20-mcrypt.ini
```

```
# cd fpm/conf.d/
# ln -s ../../mods-available/mcrypt.ini 20-mcrypt.ini
```
