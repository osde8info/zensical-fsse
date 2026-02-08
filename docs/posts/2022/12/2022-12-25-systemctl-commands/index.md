---
title: "systemctl commands"
date: 2022-12-25
categories: 
  - "fsse"
---

systemctl commands

status / list

```
status
show

list-units
list-sockets
```

target (graphical.target multi-user.target)

```
get-default
set-default
isolate
```

start/stop enable/disable daemon-reload

```
start
stop

restart
reload

enable
disable
mask
unmask

daemon-reload
```

default

```
get-default
set-default
isolate
```

refs

https://www.man7.org/linux/man-pages/man1/systemctl.1.html
