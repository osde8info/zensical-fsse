---
title: "ed/x/ubuntu #gnu/#linux #devops #cron gotcha with % chars"
date: 2015-11-26
categories: 
  - "fsse"
tags: 
  - "cron"
  - "crontab"
  - "devops"
---

ed/x/ubuntu #gnu/#linux #devops #cron gotchacron treats % chars as newlines so you need to escape each and every % with a \\

heres a crontab that runs two separate python scripts and put output and errors in two separate files (provided the first script takes longer than a second to run

```
# crontab
* * * * * python y.py > $(date +\%F-\%H-\%M-\%S).txt 2>&1 ; python z.py > $(date +\%F-\%H-\%M-\%S).txt 2>&1
```
