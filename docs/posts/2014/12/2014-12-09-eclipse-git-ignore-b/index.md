---
title: "eclipse git ignore broken hack"
date: 2014-12-09
categories: 
  - "fsse"
tags: 
  - "bug"
  - "eclipse"
  - "git"
  - "ignore"
---

here's a nasty eclipse hack to get eclipse to read your git ignore/exclude files from .config/git/ignore

```
$ cat ~/.gitconfig 
[user]
 name = me
 email = me@example.com

[core]
 excludesfile=/home/me/.config/git/ignore

```
