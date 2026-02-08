---
title: "#ssh stop timeouts"
date: 2013-06-04
categories: 
  - "fsse"
tags: 
  - "security"
  - "ssh"
  - "sysadmin"
---

you can stop ssh timeouts by creating the file .ssh/config with the following content

```
$ cat ~/.ssh/config 
Host *
ServerAliveInterval 60
```

then

```
$ chmod 644 .ssh/config
```
