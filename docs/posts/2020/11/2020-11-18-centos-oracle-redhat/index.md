---
title: "centos/oracle/redhat enterprise linux 8 gui install #sysadmin #devops"
date: 2020-11-18
categories: 
  - "fsse"
---

if you centos/oracle/redhat enterprise linux 8 gui iso network install goes wrong and doesnt install xwindows simply follow these instructions

https://oracle-base.com/articles/linux/oracle-linux-8-installation

```
# dnf update -y
# dnf groupinstall -y "GNOME"
# dnf install -y gdm
# systemctl enable gdm 
# systemctl set-default graphical.target
# reboot
```

and if you change your mind follow these instructions to disable xwindows

https://docs.oracle.com/cd/E19957-01/817-5310/6mkpbn3up/index.html
