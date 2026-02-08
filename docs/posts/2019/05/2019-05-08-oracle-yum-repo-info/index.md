---
title: "oracle linux 7 yum repo info has changed"
date: 2019-05-08
categories: 
  - "fsse"
tags: 
  - "epel"
  - "oracle"
  - "packages"
  - "repo"
  - "rpm"
  - "yum"
---

oracle linux 7 & 8 yum repos have changed

network install repo is at

https://public-yum.oracle.com/repo/OracleLinux/OL8/baseos/latest/x86\_64/

- https://oracle-base.com/articles/linux/download-the-latest-oracle-linux-repo-file
- https://yum.oracle.com/repo/OracleLinux/OL7/latest
- _http://yum.oracle.com/public-yum-ol7.repo_ IS DEPRECATED

you now need to run

```
# yum install oracle-softwarecollection-release-el7
```

to get the extra oracle linux 7 EPEL packages (such as yumex)

if you want to stop YUM auto updating in the background

```
# yum remove PackageKit
```

list of extra repos

```
$ yum list *release-el*
Loaded plugins: langpacks, ulninfo
Installed Packages
oraclelinux-release-el7.x86_64                           1.0-6.el7              @anaconda/7.6
Available Packages
mysql-release-el7.x86_64                                 1.0-2.el7              ol7_latest   
oracle-ceph-release-el7.x86_64                           1.0-2.el7              ol7_latest   
oracle-epel-release-el7.x86_64                           1.0-2.el7              ol7_latest   
oracle-gluster-release-el7.x86_64                        1.0-3.el7              ol7_latest   
oracle-nodejs-release-el7.x86_64                         1.0-3.el7              ol7_latest   
oracle-olcne-release-el7.x86_64                          1.0-1.el7              ol7_latest   
oracle-openstack-release-el7.x86_64                      1.0-2.el7              ol7_latest   
oracle-release-el7.x86_64                                1.0-2.el7              ol7_latest   
oracle-softwarecollection-release-el7.x86_64             1.0-2.el7              ol7_latest   
oraclelinux-developer-release-el7.x86_64                 1.0-2.el7              ol7_latest
```

to add the extra repos you need yum config mgr

```
# yum install yum-utils
```

then you can add an extra repo with

```
# yum-config-manager --enable ol7_developer_EPEL
```

see also

- https://oracle-base.com/articles/linux/articles-linux
- https://oracle-base.com/articles/linux/download-the-latest-oracle-linux-repo-file
