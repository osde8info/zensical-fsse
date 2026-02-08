---
title: "oracle linux 7 network install yum repo gotcha"
date: 2020-03-04
categories: 
  - "fsse"
tags: 
  - "amd"
  - "arm"
  - "gnu-linux"
  - "intel"
  - "network-install"
  - "oracle-linux"
  - "raspberry-pi"
  - "yum"
---

oracle linux 7 network install yum repo gotcha(s)

if you have a 800x600 screen scroll down to

goto **network & hostname** (

- enable network card
- enable DHCP

then goto **installation source** and enter

- https://yum.oracle.com/repo/OracleLinux/OL7/latest/aarch64/ for ARM & AArch64
- https://yum.oracle.com/repo/OracleLinux/OL7/latest/x86\_64/ for X86 64 bit

then set **software selection** to

- server with gui (and choose KDE if you are running in a low spec environment)

see also

- https://yum.oracle.com/
- https://yum.oracle.com/oracle-linux-7.html
