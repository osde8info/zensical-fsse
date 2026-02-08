---
title: "wsl is a sort of rsh"
date: 2023-01-06
categories: 
  - "fsse"
---

lets say you have 3 vm instances

```
wsl -l -v

  NAME               STATE           VERSION
* OracleLinux_8_5    Running         2
  Ubuntu-22.04       Running         2
  Ubuntu-20.04       Stopped         2

```

you can run remote commands in each from powershell by using -d to specify the instance (if you dont want wsl to use your default instance)

```
wsl hostname
wsl hostname -I

wsl -d Ubuntu-20.04 hostname
wsl -d Ubuntu-20.04 df -h

wsl -d Ubuntu-22.04 hostname

wsl -d Ubuntu-22.04 df -h

```
