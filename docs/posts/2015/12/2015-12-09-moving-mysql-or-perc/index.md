---
title: "Moving MySQL or Percona db files to another disk"
date: 2015-12-09
categories: 
  - "fsse"
---

Moving MySQL or Percona database files  to another disk

Phase I

- add disk to vm
- fdisk newdisk
- mkfs newdisk
- create new mountpoint
- add newdisk to fstab
- reboot

Phase II

- service mysql stop
- mkdir /storage/mysql
- mv /var/lib/mysql/\* to /storage/mysql
- DO NOT DELETE /var/lib/mysql it is still used for sockets
- vi /etc/my.cnf
- \[mysqld\]
- datadir=/storage/mysql
- socket=/var/lib/mysql/mysql.sock

Phase III

- chown -R mysql:mysql /storage/mysql
- turn off selinux
- service mysql start

See

- http://kb.vmware.com/selfservice/microsites/search.do?language=en\_US&cmd=displayKC&externalId=1003940
