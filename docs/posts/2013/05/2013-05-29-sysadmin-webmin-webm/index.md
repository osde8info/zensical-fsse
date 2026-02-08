---
title: "#sysadmin #webmin #webminstats on #buntu"
date: 2013-05-29
categories: 
  - "fsse"
tags: 
  - "buntu"
  - "ed-k-l-x-ubuntu"
  - "statistics"
  - "sysadmin"
  - "webmin"
---

sysadmins can now install the webmin webminstats 2.7 module on ed/k/l/x/ubuntu

- [ohloh.net/p/webminstats](https://www.ohloh.net/p/webminstats)

install commands

- \# aptitude install rrdtool php5-rrd librrdtool-oo-perl libsnmp-perl libauthen-pam-perl
- \# wget http://sourceforge.net/projects/webminstats/files/latest/download?source=dlp
- \# dpkg --install webmin\_1.630\_all.deb --alldeps
