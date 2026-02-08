---
title: "git and git projects subdirs"
date: 2013-10-29
categories: 
  - "fsse"
tags: 
  - "git"
  - "webdev"
---

if you want to work with git with two projects in two subdirectorys you need to set BOTH git-dir and work-tree

```
$ git --git-dir=subdir1/.git --work-tree=subdir1 status -s
```

```
$ git --git-dir=subdir2/.git --work-tree=subdir2 status -s
```
