---
title: "apache2 listen ports are now in a separate file"
date: 2018-02-19
categories: 
  - "fsse"
tags: 
  - "apache"
  - "config"
  - "http"
  - "port"
---

in apache2 the server listen ports are now in a separate file so to add a site on port :8000 you need to add 8000 to /etc/apache2/ports.conf AND add a <VirtualHost \*:8000> to  yoursite.conf

```
# If you just change the port or add more ports here, you will likely also
# have to change the VirtualHost statement in
# /etc/apache2/sites-enabled/000-default.conf
Listen 80
Listen 8000
```
