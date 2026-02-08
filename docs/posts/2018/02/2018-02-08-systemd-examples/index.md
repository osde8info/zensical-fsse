---
title: "systemd examples"
date: 2018-02-08
categories: 
  - "fsse"
tags: 
  - "init"
  - "initd"
  - "services"
  - "startup"
  - "systemd"
---

see which systemd startup targets are available and what the current default target is

```
# systemctl list-units --type target --all
# systemctl get-default

```

switch from graphical gui startup target to multi user text startup target on next boot

```
# systemctl set-default multi-user.target
```

and to switch to gui startup target on next boot

```
# systemctl set-default graphical.target
```

 

disable apache and php fpm from starting on next boot

```
# systemctl list-units --type service | grep -e "apache|fpm"
# systemctl disable apache2.service
# systemctl disable php7.0-fpm.service
```
