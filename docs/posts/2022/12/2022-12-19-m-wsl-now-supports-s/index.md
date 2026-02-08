---
title: "M$ WSL now supports systemd (and snap/snapcraft !)"
date: 2022-12-19
categories: 
  - "fsse"
---

M$ WSL now supports systemd (and snap/snapcraft !)

_In September 2022, Microsoft [announced support for systemd in WSL](https://ubuntu.com/blog/ubuntu-wsl-enable-systemd). This long-awaited upgrade to WSL unlocks a huge number of quality of life features for managing processes and services. This includes snapd support, which enables users to take advantage of all of the tools and apps available on [snapcraft.io](https://snapcraft.io/store)._

login to wsl ubuntu and sudo and create /etc/wsl.conf

```
[boot]
systemd=true
```

logout from wsl ubuntu and reboot wsl ubuntu from a CMD or PowerShell window

```
C:> wsl --shutdown
```

you can now relogin to your ubuntu and install snap

```
# aptitude install snap
# snap install hello-world
```

- https://ubuntu.com/blog/ubuntu-wsl-enable-systemd

- https://ubuntu.com/tutorials/install-ubuntu-on-wsl2-on-windows-11-with-gui-support#4-configure-ubuntu

- https://snapcraft.io/store

[![](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/wslubufire.png?w=1024)](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/wslubufire.png)
