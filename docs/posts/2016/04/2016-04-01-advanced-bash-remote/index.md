---
title: "advanced bash remote diffs using ssh"
date: 2016-04-01
categories: 
  - "fsse"
tags: 
  - "ssh"
  - "sysadmin"
---

advanced bash remote diffs using ssh

```
diff <(ssh server1.dom1 cat /composer.json) <(ssh server2.dom2 cat /composer.json)

```

http://tldp.org/LDP/abs/html/process-sub.html
