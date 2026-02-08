---
title: "rpmfusion install for oracle &amp; rhel gnu/linux"
date: 2025-09-18
categories: 
  - "fsse"
---

oracle or rhel rpmfusion install

[https://rpmfusion.org/Configuration](https://rpmfusion.org/Configuration)

- `dnf install --nogpgcheck https://dl.fedoraproject.org/pub/epel/epel-release-latest-$(rpm -E %rhel).noarch.rpm`

- `dnf install --nogpgcheck https://mirrors.rpmfusion.org/free/el/rpmfusion-free-release-$(rpm -E %rhel).noarch.rpm`

- `dnf install --nogpgcheck https://mirrors.rpmfusion.org/nonfree/el/rpmfusion-nonfree-release-$(rpm -E %rhel).noarch.rpm`

ORACLE requires

```
/usr/bin/crb enable
```

RHEL requires (RHEL8 , RHEL9 and to RHEL10)

- `subscription-manager repos --enable "codeready-builder-for-rhel-$(rpm -E %{rhel})-$(uname -m)-rpms"`

THEN

```
dnf update
```
