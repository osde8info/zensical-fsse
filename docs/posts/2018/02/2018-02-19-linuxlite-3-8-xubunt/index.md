---
title: "linuxlite 3.8 / xubuntu 16 cpu microcode"
date: 2018-02-19
categories: 
  - "fsse"
tags: 
  - "intel"
  - "linuxlite"
  - "microcode"
---

how do i check if i have the latest linuxlite 3.8 xubuntu 16 cpu microcode

```
# aptitude install intel-microcode
The following NEW packages will be installed:
 intel-microcode iucode-tool{a} 
0 packages upgraded, 2 newly installed, 0 to remove and 79 not upgraded.
Need to get 1,019 kB of archives. After unpacking 1,275 kB will be used.
Do you want to continue? [Y/n/?] 
Get: 1 http://gb.archive.ubuntu.com/ubuntu xenial-updates/main amd64 iucode-tool amd64 1.5.1-1ubuntu0.1 [33.8 kB]
Get: 2 http://gb.archive.ubuntu.com/ubuntu xenial-updates/main amd64 intel-microcode amd64 3.20180108.0+really20170707ubuntu16.04.1 [985 kB]
Fetched 1,019 kB in 0s (5,185 kB/s) 
Selecting previously unselected package iucode-tool.
(Reading database ... 240840 files and directories currently installed.)
Preparing to unpack .../iucode-tool_1.5.1-1ubuntu0.1_amd64.deb ...
Unpacking iucode-tool (1.5.1-1ubuntu0.1) ...
Selecting previously unselected package intel-microcode.
Preparing to unpack .../intel-microcode_3.20180108.0+really20170707ubuntu16.04.1_amd64.deb ...
Unpacking intel-microcode (3.20180108.0+really20170707ubuntu16.04.1) ...
```

 

then reboot

```
# aptitude show intel-microcode
Package: intel-microcode 
State: installed
Automatically installed: no
Version: 3.20180108.0+really20170707ubuntu16.04.1
```
