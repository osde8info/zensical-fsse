---
title: "netdata deb rpm &amp; docker images"
date: 2020-04-09
categories: 
  - "fsse"
tags: 
  - "deb"
  - "devops"
  - "netdata"
  - "rpm"
  - "sysadmin"
---

netdata deb rpm & docker images

- https://docs.netdata.cloud/packaging/installer/methods/packages/
- https://docs.netdata.cloud/packaging/docker/

docker run cmd

```
$ docker run -d \
  -p 19999:19999 \
  -v /etc/passwd:/host/etc/passwd:ro \
  -v /etc/group:/host/etc/group:ro \
  -v /proc:/host/proc:ro \
  -v /sys:/host/sys:ro \
  -v /etc/os-release:/host/etc/os-release:ro \
  --cap-add SYS_PTRACE \
  --security-opt apparmor=unconfined \
  --name=netdata netdata/netdata
```
