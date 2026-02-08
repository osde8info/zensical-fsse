---
title: "gnu/linux uname and lsb_release"
date: 2013-06-03
categories: 
  - "fsse"
tags: 
  - "gnu-linux"
  - "info"
  - "lsb"
  - "lsb_release"
  - "sysadmin"
  - "uname"
---

uname -a tells you which linux kernel you are using

```
$ uname -a

Linux myserver 2.6.30.10-105.2.23.fc11.i686.PAE #1 SMP Thu Feb 11 07:05:37 UTC 2010 i686 i686 i386 GNU/Linux

Linux myserver 3.8.0-22-generic #33~precise1-Ubuntu SMP Fri May 17 01:00:37 UTC 2013 i686 i686 i386 GNU/Linux
```

lsb\_release tells you which gnu/linux distro you are using

```
$ lsb_release -a

LSB Version:    :core-4.0-ia32:core-4.0-noarch:graphics-4.0-ia32:graphics-4.0-noarch:printing-4.0-ia32:printing-4.0-noarch
Distributor ID:    Fedora
Description:    Fedora release 11 (Leonidas)
Release:    11
Codename:    Leonidas

No LSB modules are available.
Distributor ID:    Ubuntu
Description:    Ubuntu 12.04.2 LTS
Release:    12.04
Codename:    precise
```
