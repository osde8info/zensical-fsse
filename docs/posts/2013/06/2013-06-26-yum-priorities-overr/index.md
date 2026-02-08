---
title: "yum priorities override"
date: 2013-06-26
categories: 
  - "fsse"
tags: 
  - "repo"
  - "yum"
---

you can override yum priorities by using enablerepo to force a yum rpm repo with a lower (higher value) priority to be included for example if epel priority=10 and remi priority=20 you can include packages from the remi yum repo with

```
# yum check-update --enablerepo=remi
```
