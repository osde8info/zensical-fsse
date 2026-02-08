---
title: "oracle gnu/linux 7 mate-desktop install doesnt install mate-screenshot so screenshots dont work #screenshot #alsamixer"
date: 2020-12-04
categories: 
  - "fsse"
---

after installing oracle gnu/linux mate-desktop you need to additionally run

```
# yum install mate-screenshot 
# yum install mate-system-monitor
# yum install mate-sensors-applet
```

additionally oracle gnu/linux mate-desktop doesnt have a volume control so run

```
$ alsamixer
```

from the command line instead
