---
title: "oracle linux node 20 install"
date: 2025-08-28
categories: 
  - "fsse"
---

oracle linux 9 - how to upgrade from nodejs npm 12 to nodejs npm 20 (to run expo.dev for example)

```
dnf config-manager --set-enabled ol9_appstream
dnf module enable nodejs:20
dnf update nodejs
```

see

[https://yum.oracle.com/oracle-linux-nodejs.html](https://yum.oracle.com/oracle-linux-nodejs.html)
