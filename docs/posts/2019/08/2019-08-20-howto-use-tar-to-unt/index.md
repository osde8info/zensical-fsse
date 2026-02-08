---
title: "howto use tar to untar (unzip) tar.bz tar.gz tar.xz files"
date: 2019-08-20
categories: 
  - "fsse"
tags: 
  - "bz"
  - "gz"
  - "tar"
  - "untar"
  - "unzip"
  - "xz"
---

howto use tar to untar (unzip) tar.bz tar.gz tar.xz files

```
$ tar xvf tar.zz
```

apparently the latest (xubuntu) version of tar now AUTOMATICALLY recognises the compression that has been used

- http://www.gnu.org/software/tar/manual/tar.html#SEC134

_The only case when you have to specify a decompression option while reading the archive is when reading from a pipe or from a tape drive that does not support random access. However, in this case GNU `tar` will indicate which option you should use._
