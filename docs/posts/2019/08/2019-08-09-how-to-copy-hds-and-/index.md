---
title: "how to copy HDs and SDs with dd or pv"
date: 2019-08-09
categories: 
  - "fsse"
tags: 
  - "dd"
  - "pv"
---

how to copy HDs, SDs (and raspberry pi boot SDs) with dd and/or pv

assuming source device is SDC and destination device is SDD

```
# umount /dev/sdc1
# umount /dev/sdd1

# shred /dev/sdd
```

then

```
# dd if=/dev/sdc of=/dev/sdd
```

or

```
# dd if=/dev/sdc status=progress bs=4K of=/dev/sdd
```

or

```
# dd if=/dev/sdc | pv | of=/dev/sdd
```

more fun uses of pv

```
$ pv -d
```

see also

- https://www.howtoforge.com/tutorial/linux-dd-command-clone-disk-practical-example/
- https://www.linuxnix.com/what-you-should-know-about-linux-dd-command/
- https://opensource.com/article/18/7/how-use-dd-linux
