---
title: "ms windows 7 and ms windows 10 system repair discs, system image backups and media ids #gotcha"
date: 2017-02-19
categories: 
  - "fsse"
tags: 
  - "backup"
  - "gotcha"
  - "media-id"
  - "restore"
  - "windoz"
---

It would seem that ms windows 7 and ms windows 10 backup writes a media id to the System Repair Disc CD/DVD it creates and puts the same media id in the system image subdirectory in WindowsImageBackup\\MACHINENAME\\ to **LOCK** the windows System Repair Disc CD/DVD with the USB disk System Image backup/restore disk you are creating.

ie if you lose the original System Repair Disc CD/DVD you CANNOT restore from your USB System Image with a different/new System Repair Disc CD/DVD

Possible workarounds:

- Always keep MATCHING CD/DVD disc and USB disk drive backups together

or

- Install a clean Windows 7 or 10 on target machine
- Create a NEW System Repair Disc CD/DVD
- Create a NEW USB System Image
- Copy MediaId file from NEW USB System Image to OLD USB System Image
- Boot from new System Repair Disc CD/DVD with OLD USB System Image
