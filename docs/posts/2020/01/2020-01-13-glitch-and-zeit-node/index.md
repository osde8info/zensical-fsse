---
title: "glitch and zeit node dev env gotchas"
date: 2020-01-13
categories: 
  - "fsse"
tags: 
  - "glitch"
  - "node"
  - "webdev"
  - "zeit"
---

glitch and zeit node dev env gotchas that hit me today were as follows

glitch node dev

- glitch auto recompiles after you edit every line which can get irritating

zeit node dev

- glitch doesnt always attach to github so NEVER rereleases for you
- SSL\_ERROR\_INTERNAL\_ERROR\_ALERT
- SSL\_ERROR\_PROTOCOL\_VERSION\_ALERT

workaround !

- triple check the ANAME / CNAME and TXT dns records
- then simply wait 20 mins and they might disappear

the BIG bonus of zeit is that you can use YOUR own domain for FREE provided you can get rid of the SSL errors (BTW i hope glitch mktg are reading this)
