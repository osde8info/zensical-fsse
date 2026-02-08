---
title: "git unmerge (local)"
date: 2016-06-23
categories: 
  - "fsse"
tags: 
  - "git"
  - "unmerge"
---

lets say you locally merged another branch into yourbranch but changed your mind BEFORE you pushed it

to unmerge you will need to switch to another branch, delete yourbranch then checkout yourbranch

```
git checkout anotherbranch
git branch -D yourbranch
git checkout yourbranch
git pull
```
