---
title: "MySQL or @percona startup error caused by #SELinux"
date: 2015-12-09
categories: 
  - "fsse"
---

MySQL or @percona startup error "Starting MySQL (Percona Server).The server quit without upd" can be caused by #SELinux

Quick fix

```
# setenforce 0
# sestatus

```
