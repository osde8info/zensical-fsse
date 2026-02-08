---
title: "howto downgrade ed/x/ubuntu 16 php 7.0 to php 5.6"
date: 2016-09-02
categories: 
  - "fsse"
tags: 
  - "5-6"
  - "7"
  - "downgrade"
  - "php"
  - "ubuntu"
---

howto downgrade ed/x/ubuntu 16 php 7.0 to php 5.6

install a clean ed/x/ubuntu from ISO but do not add php then

```
add-apt-repository ppa:ondrej/php
aptitude update
aptitude install php5.6

# verify php
php -v

# verify apache
a2query -m
```

thanks to

- http://askubuntu.com/questions/761713/how-can-i-downgrade-from-php-7-to-php-5-6-on-ubuntu-16-04
- http://geekdecoder.com/ubuntu-16-04-xenial-downgrade-php-7-php-5-6/
- http://lornajane.net/posts/2016/php-7-0-and-5-6-on-ubuntu
