---
title: "how to install oracle linux 7 for arm on a raspberry pi 3"
date: 2020-02-27
categories: 
  - "fsse"
tags: 
  - "arm"
  - "linux"
  - "oracle"
  - "raspberry-pi"
---

how to install oracle linux 7 for arm (aarch64) on a raspberry pi 3 WITHOUT having to sing in and download the oracle linux 7 CD or DVD ISO

get balena etcher

- [balena etcher](https://www.balena.io/etcher/)

get an oracle 7 image

- [oracle linux 7.6 for arm](http://download.oracle.com/otn-pub/otn_software/linux/rpi3-ol7.6-image-20181116.img.xz)
- [oracle](https://download.oracle.com/otn-pub/otn_software/linux/rpi3-ol7.7-image-20190825.img.xz) [linux 7.7 for arm](http://download.oracle.com/otn-pub/otn_software/linux/rpi3-ol7.6-image-20181116.img.xz)

burn image to SD card

_note you won’t even need to uncompress the image or anything like that. Etcher is capable of reading the `xz` format_

boot from SD card

![bletch](https://fsse8info.wordpress.com/wp-content/uploads/2020/02/bletch.png)

refs

- https://dzone.com/articles/how-to-install-oracle-linux-on-a-raspberry-pi-the
- https://geraldonit.com/2019/08/11/how-to-install-oracle-linux-on-a-raspberry-pi-the-easy-way/
- https://www.linux-arm.info/index.php/1518-how-to-install-oracle-linux-on-a-raspberry-pi-the-easy-way
- https://www.oracle.com/linux/downloads/linux-arm-downloads.html

BONUS PROJECT

- https://www.balena.io/blog/turn-your-old-speakers-or-hi-fi-into-bluetooth-receivers-using-only-a-raspberry-pi/
