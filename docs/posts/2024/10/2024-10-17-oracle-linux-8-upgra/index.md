---
title: "oracle linux 8 upgrade node 16 to node 20"
date: 2024-10-17
categories: 
  - "fsse"
tags: 
  - "appstream"
  - "dns"
  - "node"
---

Nodejs is released as an AppStream Module for Oracle Linux 8; ol8\_appstream repository is enabled by default on Oracle Linux 8. If not enabled, execute:

```
dnf config-manager --set-enabled ol8_appstream
```

remove node 16

```
dnf remove nodejs
```

switch to module nodejs:20

```
dnf module list --all nodejs
dnf module enable nodejs:20
dnf install nodejs
```

[https://yum.oracle.com/oracle-linux-nodejs.html#EnablingReposOL8](https://yum.oracle.com/oracle-linux-nodejs.html#EnablingReposOL8)
