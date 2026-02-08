---
title: "HTTPD #PHP #PDO error caused by #SELinux"
date: 2015-12-09
categories: 
  - "fsse"
tags: 
  - "apache"
  - "httpd"
  - "pdo"
  - "php"
  - "selinux"
---

The HTTPD PHP PDO connect error "SQLSTATE\[HY000\] \[2002\] Permission denied" can be caused by SELinux on Centos & Red Hat 5 & 6

Quick Fix

```
# setenforce 0
# sestatus

```

See

- https://www.centos.org/docs/5/html/5.2/Deployment\_Guide/sec-sel-enable-disable-enforcement.html
- https://www.centos.org/docs/5/html/5.2/Deployment\_Guide/sec-sel-enable-disable.html
