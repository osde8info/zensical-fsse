---
title: "ed/x/ubuntu list usb devices"
date: 2018-02-08
categories: 
  - "fsse"
tags: 
  - "sysadmin"
  - "usb"
  - "usd-ids"
---

ed/x/ubuntu 16 uses a 3 year old file (usb.ids) to list usb devices

```
$ lsusb
Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
Bus 002 Device 003: ID 0e0f:0002 VMware, Inc. Virtual USB Hub
Bus 002 Device 002: ID 0e0f:0003 VMware, Inc. Virtual Mouse
Bus 002 Device 001: ID 1d6b:0001 Linux Foundation 1.1 root hub
```

you can update this manually if you like

```
# locate usb.ids
/usr/share/hwdata/usb.ids
/usr/share/kcmusb/usb.ids
/usr/share/misc/usb.ids
/var/lib/usbutils/usb.ids
```

the first three are symlinks to the last one in /var/lib so that is the only one you need to update

```
# wget http://www.linux-usb.org/usb.ids
# diff usb.ids /var/lib/usbutils/usb.ids | head -20
```

(optionally) add your favorite missing device(s)

then

```
# cp usb.ids /var/lib/usbutils/usb.ids
```

try lsusb again and your missing devices might now be listed
