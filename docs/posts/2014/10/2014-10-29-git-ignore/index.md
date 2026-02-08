---
title: "git ignore"
date: 2014-10-29
categories: 
  - "fsse"
---

eclipse git ignore bug workaround

if you want eclipse to use git ignores setup a global git ignore file

`$ vi ~/.gitignore or vi ~/.config/git/ignore .buildpath .project .settings  $ git config --global core.excludesfile '~/.gitignore' $ git config --global --list $ git config --get-all core.excludesfile  $ git config --global core.excludesfile '~/.config/git/ignore' $ git config --global --list $ git config --get-all core.excludesfile`

thanks to

http://stackoverflow.com/questions/7335420/global-git-ignore
