---
title: "git syncing a fork master branch"
date: 2020-01-09
categories: 
  - "fsse"
tags: 
  - "git"
  - "merge"
  - "remote"
  - "upstream"
---

git syncing a fork master branch

- https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/configuring-a-remote-for-a-fork
- https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/syncing-a-fork

commands

```
$ git checkout master
$ git remote -v
$ git remote add upstream https://github.com/...
$ git remote -v
$ git fetch upstream
$ git merge upstream/master
$ git push
```
