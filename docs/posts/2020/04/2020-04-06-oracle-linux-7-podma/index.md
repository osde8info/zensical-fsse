---
title: "oracle linux 7 podman install"
date: 2020-04-06
categories: 
  - "fsse"
tags: 
  - "containers"
  - "oracle-linux"
  - "podman"
---

oracle linux 7 podman install

```
# yum install oracle-softwarecollection-release-el7 
# yum install yum-utils
# yum-config-manager --enable ol7_addons 

```

oracle linux 7 podman install podman and slirp4netns

```
# yum install podman
# yum install slirp4netns
```

then enable user namespaces

```
# echo "user.max_user_namespaces=10000" > /etc/sysctl.d/userns.conf
# sysctl -p /etc/sysctl.d/userns.conf
```

then add user

```
# useradd -m $USER
```

then login as $USER

```
$ podman images
```
