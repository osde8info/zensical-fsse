---
title: "M$ WSL 2 Oracle GNU/Linux 8 systemd &amp; snap &amp; firefox"
date: 2022-12-19
categories: 
  - "fsse"
---

With M$ WSL 2 you can run Oracle GNU/Linux 8 with systemd & snap

login into your wsl oracle

vi /etc/wsl.conf

```
[boot]
systemd=true
```

logout and reboot wsl via CMD or PowerShell

```
C:> wsl --shutdown
```

install and enable snap socket

```
# yum install https://dl.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm
# dnf install snapd
# systemctl enable --now snapd.socket
# snap install hello-world
# snap install firefox
```

refs

- https://devblogs.microsoft.com/commandline/systemd-support-is-now-available-in-wsl/

- https://devblogs.microsoft.com/commandline/automatically-configuring-wsl/

- https://learn.microsoft.com/en-us/windows/wsl/wsl-config

- https://ubuntu.com/blog/ubuntu-wsl-enable-systemd

- https://snapcraft.io/docs/installing-snap-on-red-hat

[![](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/wslfire.png?w=1024)](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/wslfire.png)
