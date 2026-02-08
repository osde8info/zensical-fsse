---
title: "oracle linux 8 &amp; cockpit logs"
date: 2022-12-24
categories: 
  - "fsse"
---

oracle linux 8 cockpit log access requires the user you login to cockpit as to be a member of systemd-journal group

```
# usermod -aG systemd-journal MYUSER
# groupmems -g systemd-journal -l
opc MYUSER
```

[![](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/image-5.png?w=1024)](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/image-5.png)
