---
title: "rsync without updating owner and group"
date: 2013-06-03
categories: 
  - "fsse"
tags: 
  - "copy"
  - "copying"
  - "rsync"
  - "sysadmin"
---

rsync without updating owner and group

```
$ rsync -cav --no-owner --no-group SOURCE/DIR TARGET/DIR
```

see also

- http://linux.die.net/man/1/rsync
