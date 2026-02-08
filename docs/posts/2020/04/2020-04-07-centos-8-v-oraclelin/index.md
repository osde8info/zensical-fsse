---
title: "CentOS 8 v @OracleLinux 8 v IBMredhat 8 network install #devops #sysadmin"
date: 2020-04-07
categories: 
  - "fsse"
tags: 
  - "centos"
  - "ibmredhat"
  - "install"
  - "oraclelinux"
  - "yum"
---

### CentOS 7/8 network install

it just works ! and autodetects yum repo installation source

![VirtualBox_cent8_07_04_2020_10_57_55.png](https://fsse8info.wordpress.com/wp-content/uploads/2020/04/virtualbox_cent8_07_04_2020_10_57_55.png)

![VirtualBox_cent8_07_04_2020_10_57_27.png](https://fsse8info.wordpress.com/wp-content/uploads/2020/04/virtualbox_cent8_07_04_2020_10_57_27.png)

### OracleLinux 7/8 network install

you need to manually setup the yum repo installation source to

https://public-yum.oracle.com/repo/OracleLinux/OL8/baseos/latest/x86\_64/

![VirtualBox_orac7_04_03_2020_22_39_32.png](https://fsse8info.wordpress.com/wp-content/uploads/2020/04/virtualbox_orac7_04_03_2020_22_39_32.png)

### IBM Red Hat 7/8 network install

DOESNT WORK WITHOUT A SUB !

a) you need a ibm red hat subscription (or 'free' developer subscription)

b) even if you have a subscription you need to create your own yum repo server

c) so you have to install everything from your subscription DVD anyway
