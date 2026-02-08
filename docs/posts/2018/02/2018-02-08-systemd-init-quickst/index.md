---
title: "systemd init quickstart"
date: 2018-02-08
categories: 
  - "fsse"
tags: 
  - "init"
  - "initd"
  - "services"
  - "sysadmin"
  - "systemd"
---

systemd initd quickstart

list services

```
# systemctl list-units --type service
# systemctl list-unit-files --type service
```

enable a service

```
# systemctl enable name.service
```

stopping a service

```
# systemctl stop name.service
```

disable a service

```
# systemctl disable name.service
```
