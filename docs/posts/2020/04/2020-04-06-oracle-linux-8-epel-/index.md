---
title: "oracle linux 7 &amp; oracle linux 8 bonus repos"
date: 2020-04-06
categories: 
  - "fsse"
tags: 
  - "addons"
  - "epel"
  - "oracle-linux"
  - "repo"
  - "yum"
---

oracle linux 7 & oracle linux 8 bonus repos

oracle linux 7 repos

- addons
- developer
- developer\_EPEL
- latest
- software\_collections

oracle linux 7 yum install

```
# yum install oraclelinux-developer-release-el7
# yum install oracle-epel-release-el7
```

oracle linux 7 yum repolist

```
# yum repolist
Loaded plugins: langpacks, ulninfo
repo id repo name status
ol7_addons/x86_64         Oracle Linux 7Server Add ons (x86_64) 411
ol7_developer/x86_64      Oracle Linux 7Server Development Packages (x86_64)                                    1,254
ol7_developer_EPEL/x86_64 Oracle Linux 7Server Development Packages (x86_64) 31,355
ol7_latest/x86_64         Oracle Linux 7Server Latest (x86_64) 16,661
ol7_software_collections/x86_64  Software Collection Library release 3.0 packages for Oracle Linux 7 (x86_64) 14,433
```

oracle linux 7 docs

- https://yum.oracle.com/oracle-linux-7.html
- https://yum.oracle.com/repo/OracleLinux/OL7/addons/x86\_64/index.html
- https://yum.oracle.com/repo/OracleLinux/OL7/developer/x86\_64/index.html
- https://yum.oracle.com/repo/OracleLinux/OL7/developer/EPEL/x86\_64/index.html

oracle linux 8 repos

- appstream
- baseos
- developer
- developer\_EPEL

oracle linux 8 repo docs

- https://yum.oracle.com/oracle-linux-8.html
- https://yum.oracle.com/repo/OracleLinux/OL8/addons/x86\_64/index.html
- https://yum.oracle.com/repo/OracleLinux/OL8/developer/x86\_64/index.html
- https://yum.oracle.com/repo/OracleLinux/OL8/developer/EPEL/x86\_64/index.html

oracle linux 8 yum install

```
# yum install oraclelinux-developer-release-el8
# yum install oracle-epel-release-el8
```

oracle linux 8 yum repolist

```
# yum repolist
Last metadata expiration check: 0:07:13 ago on Mon 06 Apr 2020 14:26:26 EDT.
repo id repo name status
ol8_appstream      Oracle Linux 8 Application Stream (x86_64) 11,621
ol8_baseos_latest  Oracle Linux 8 BaseOS Latest (x86_64) 4,652
ol8_developer      Oracle Linux 8 Development Packages (x86_64)                                        29
ol8_developer_EPEL Oracle Linux 8 EPEL Packages for Development (x86_64) 594
```
