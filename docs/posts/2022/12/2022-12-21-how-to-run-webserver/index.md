---
title: "how to run two webservers on two wsl instances"
date: 2022-12-21
categories: 
  - "fsse"
---

# wsl networking

all wsl instances use the SAME virtual network card ! with a random IP address on every boot so you have to bind webservers to different IP addrs and / or IP ports

## cockpit

the ip address and port binding for cockpit is defined in

```
/etc/systemd/system/sockets.target.wants/cockpit.socket
```

which is a symlink to

```
/usr/lib/systemd/system/cockpit.socket
```

## example

if your windows hypervnet is 172.24.219.113 you can add 2 extra ip addresses with

```
ip addr add 172.24.220.100/20 dev eth0
ip addr add 172.24.220.101/20 dev eth0
```

so each wsl instance now has THREE IP addrs

so on one wsl instance edit cockpit.socket

```
[Socket]
ListenStream=172.24.220.100:9090
FreeBind=true
```

and on the other wsl instance edit cockpit.socket

```
[Socket]
ListenStream=172.24.220.101:9090
FreeBind=true
```

restart cockpit in BOTH wsl instances with

```
# systemctl daemon-reload
# systemctl restart cockpit.socket
```

from edge on your windows 10 host you can now access the two webservers at

```
https://172.24.220.100:9090/system
https://172.24.220.101:9090/system
```

refs

- [cockpit-project.org/guide](https://cockpit-project.org/guide/latest/listen)
- [cockpit-project.org/guide](https://cockpit-project.org/guide/latest/cockpit.conf.5)
- [man/systemd.socket.html](https://www.freedesktop.org/software/systemd/man/systemd.socket.html)

[![](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/image-2.png?w=1024)](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/image-2.png)
