---
title: "#centos 6 #oracle-linux 6 #red-hat 6 #xfce open source desktop install using #fedora #epel"
date: 2013-06-05
categories: 
  - "fsse"
tags: 
  - "centos"
  - "desktop"
  - "epel"
  - "fedora"
  - "oracle-linux"
  - "red-at"
  - "xfce"
---

centos 6 oracle-linux 6 red hat enterprise linux 6 can all use the #xfce desktop if you install #fedora #epel

- install redhat fedora epel yum repo
- yum install xorg-x11-xdm
- yum install xfdesktop xfce-utils

then

- yum groupinstall "X Window System" XFCE

finally

- logout
- login
- choose xfce from session combo at bottom of screen

welcome to your new xfce desktop

see also

- fedoraproject.org/wiki/Xfce
- http://www.linuxtopia.org/online\_books/rhel6/rhel\_6\_installation/rhel\_6\_installation\_sn-switching-to-gui-login.html
- xfce.org/download
- http://distrowatch.com/search.php?pkg=xfdesktop&pkgver=4.10
- http://alinuxblog.com/fedora/install-xfce-fedora-17.htm
