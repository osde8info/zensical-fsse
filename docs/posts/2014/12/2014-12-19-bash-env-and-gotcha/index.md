---
title: "bash env ; and &amp;&amp; gotcha"
date: 2014-12-19
categories: 
  - "fsse"
tags: 
  - "bash"
  - "cron"
  - "env"
  - "term"
---

if you want to change a bash environment variable you need to set it in each and every bash multistatement

```
$ env TERM=lpr env|grep TERM ; env TERM=lpr env|grep TERM
TERM=lpr
COLORTERM=xfce4-terminal
TERM=lpr
COLORTERM=xfce4-terminal

$ env TERM=lpr env|grep TERM && env TERM=lpr env|grep TERM
TERM=lpr
COLORTERM=xfce4-terminal
TERM=lpr
COLORTERM=xfce4-terminal

```
