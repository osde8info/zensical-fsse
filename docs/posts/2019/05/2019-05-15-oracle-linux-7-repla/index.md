---
title: "oracle linux 7 replace node 6 with node 8 or node 10"
date: 2019-05-15
categories: 
  - "fsse"
tags: 
  - "node"
  - "oracle-linux"
---

oracle linux 7 replace node 6 with node 8 or node 10

```
# yum uninstall node
# yum install oraclelinux-release-el7

```

edit and disable and enable node8 and node10 repos

```
# vi /etc/yum.repos.d/oracle-nodejs-ol7.repo
[ol7_developer_nodejs8]
enabled=0
[ol7_developer_nodejs10]
enabled=1

```

then

```
# yum install --disablerepo=ol7_developer_EPEL nodejs

```
