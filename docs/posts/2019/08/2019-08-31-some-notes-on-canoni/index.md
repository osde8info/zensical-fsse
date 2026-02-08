---
title: "some notes on @canonical #snapd #snap #filesystems and #files"
date: 2019-08-31
categories: 
  - "fsse"
tags: 
  - "canonical"
  - "packages"
  - "snap"
  - "squashfs"
---

canonical snapd snap packages are stored in /var/lib/snapd/

```
# ls -l /var/lib/snapd/snaps
total 600456
-rw------- 2 root root 57069568 Aug 29 14:29 core18_1074.snap
-rw------- 2 root root 92733440 May 29 18:49 core_6964.snap
-rw------- 1 root root 92983296 Aug 29 14:28 core_7396.snap
-rw------- 2 root root 113704960 May 29 18:50 electronplayer_6.snap
-rw------- 2 root root 56287232 Aug 29 14:30 electronplayer_9.snap
-rw------- 2 root root 157192192 Aug 29 14:31 gnome-3-28-1804_71.snap
-rw------- 2 root root 44879872 Aug 29 14:30 gtk-common-themes_1313.snap
```

they are squashfs filesystems which are then mounted at /snap

```
# df -h
Filesystem Size Used Avail Use% Mounted on
/dev/loop0 55M 55M 0 100% /snap/core18/1074
/dev/loop1 89M 89M 0 100% /snap/core/7396
/dev/loop2 54M 54M 0 100% /snap/electronplayer/9
/dev/loop3 150M 150M 0 100% /snap/gnome-3-28-1804/71
/dev/loop4 109M 109M 0 100% /snap/electronplayer/6
/dev/loop5 89M 89M 0 100% /snap/core/6964
/dev/loop6 43M 43M 0 100% /snap/gtk-common-themes/1313
```

but actually create more space than appears

```
# du -sh /snap/*
4.0K /snap/bin
507M /snap/core
166M /snap/core18
593M /snap/electronplayer
570M /snap/gnome-3-28-1804
256M /snap/gtk-common-themes
```

snapd snap adds /snap/bin your path

```
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:
/sbin:/bin:/usr/games:/usr/local/games:
/snap/bin:/root/.dotnet/tools
```

so that you can see the snap symbolic links that run each snap app via snap

```
$ ls -l /snap/bin/
total 0
lrwxrwxrwx 1 root root 13 Aug 29 14:30 electronplayer -> /usr/bin/snap
lrwxrwxrwx 1 root root 13 Aug 31 15:18 freemind -> /usr/bin/snap
```

docs

- https://forum.snapcraft.io/t/the-snap-format/698
- https://forum.snapcraft.io/t/the-system-snap-directory/2817
