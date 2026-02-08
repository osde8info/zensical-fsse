---
title: "oracle linux 8 grub default grubby kernel"
date: 2022-12-22
categories: 
  - "fsse"
---

oracle linux 8 grub default grubby kernel

you can change the default oracle linux 8 kernel to NON - UEK if you wish to use virtualbox guest additions

```
# grubby --info=ALL
# grubby --default-kernel
# grubby --set-default /boot/vmlinuz-4.18.0-425.3.1.el8.x86_64
# grubby --default-kernel

# reboot
```

see

https://docs.oracle.com/en/learn/oracle-linux-kernels/#change-the-default-kernel

[![](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/virtualbox_orac8_22_12_2022_08_01_59.png?w=1024)](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/virtualbox_orac8_22_12_2022_08_01_59.png)
