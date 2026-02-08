---
title: "du disk usage gotcha"
date: 2014-12-09
categories: 
  - "fsse"
tags: 
  - "du"
  - "gnu-linux"
  - "sysadmin"
  - "unix"
---

du -s doesnt always show you quite what you expected for example

```
$ du -s .*
```

you may prefer to use this syntax instead

```
$ du -s .[#-z]*
```
