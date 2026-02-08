---
title: "centos oracle uek red hat 5 6 7 nginx php 5.6 install howto"
date: 2015-07-23
categories: 
  - "fsse"
tags: 
  - "centos"
  - "nginx"
  - "oracle-uek"
  - "php"
  - "php-fpm"
---

http://wiki.nginx.org/PHPFcgiExample

install EPEL and IUSC repos

```
# yum install nginx
# yum install php56u-fpm
```

edit /etc/nginx/conf.d/default.conf and replace the default fastcgi\_param value as below

```
    # pass the PHP scripts to FastCGI server listening on 127.0.0.1:9000
    #
    location ~ \.php$ {
        root           html;
        fastcgi_pass   127.0.0.1:9000;
        fastcgi_index  index.php;
        # fastcgi_param  SCRIPT_FILENAME  /scripts$fastcgi_script_name;
        fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
        include        fastcgi_params;
    }

```

restart nginx and php-fpm services

```
# service nginx start
# service php-fpm start
```
