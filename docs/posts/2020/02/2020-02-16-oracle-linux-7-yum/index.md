---
title: "Oracle Linux 7 yum ++"
date: 2020-02-16
categories: 
  - "fsse"
tags: 
  - "oracle-linux"
  - "post-install"
  - "repo"
  - "yum"
---

Theres more than meets the eye to Oracle Linux 7 yum as well as the default yum repo there are also BONUS yum repos for EPEL, NODE etc

You can also connecting to yum mirrors in different Oracle Cloud Infrastructure (OCI) regions

- https://yum.oracle.com/getting-started.html
- https://yum.oracle.com/getting-started.html#installing-software-from-oracle-linux-yum-server
- https://yum.oracle.com/repo/OracleLinux/OL7/latest/aarch64/

By default you get

```
# ls -l /etc/yum.repos.d/
total 12
-rw-r--r--. 1 root root 3594 Mar 30 01:28 oracle-linux-ol7.repo
-rw-r--r--. 1 root root 2587 Mar 30 01:27 uek-ol7.repo
-rw-r--r--. 1 root root  226 Mar 30 01:27 virt-ol7.repo

# yum repolist
Loaded plugins: langpacks, ulninfo
repo id                                 repo name                                                                                               status
ol7_UEKR5/x86_64                        Latest Unbreakable Enterprise Kernel Release 5 for Oracle Linux 7Server (x86_64)                           263
ol7_latest/x86_64                       Oracle Linux 7Server Latest (x86_64)                                                                    16,661
```

but you can update to the latest by running

```
# yum install oracle-softwarecollection-release-el7
```

and you will then have more repos available

```
# cat /etc/yum.repos.d/oracle-softwarecollection-ol7.repo
[ol7_software_collections]
name=Software Collection Library release 3.0 packages for Oracle Linux 7 ($basearch)
baseurl=https://yum$ociregion.oracle.com/repo/OracleLinux/OL7/SoftwareCollections/$basearch/
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-oracle
gpgcheck=1
enabled=1

```

then to get access to oracle linux 7 EPEL repo run

\# yum install yum-utils
# yum-config-mgr --enable `oracle-epel-release-el7` 
# yum repolist
yum --enablerepo=\* repolist

and you should see

```
repo id                                 repo name                                                                                                    status
ol7_MODRHCK/x86_64                      Latest RHCK with fixes from Oracle for Oracle Linux 7Server (x86_64)                                            619
ol7_UEKR3/x86_64                        Latest Unbreakable Enterprise Kernel Release 3 for Oracle Linux 7Server (x86_64)                                984
ol7_UEKR3_OFED20/x86_64                 OFED supporting tool packages for Unbreakable Enterprise Kernel on Oracle Linux 7 (x86_64)                       64
ol7_UEKR4/x86_64                        Latest Unbreakable Enterprise Kernel Release 4 for Oracle Linux 7Server (x86_64)                                166
ol7_UEKR4_OFED/x86_64                   OFED supporting tool packages for Unbreakable Enterprise Kernel Release 4 on Oracle Linux 7 (x86_64)            205
ol7_UEKR4_archive/x86_64                Unbreakable Enterprise Kernel Release 4 for Oracle Linux 7Server (x86_64) - Archive                           1,084
ol7_UEKR5/x86_64                        Latest Unbreakable Enterprise Kernel Release 5 for Oracle Linux 7Server (x86_64)                                263
ol7_UEKR5_RDMA/x86_64                   Oracle Linux 7 UEK5 RDMA (x86_64)                                                                               189
ol7_UEKR5_archive/x86_64                Unbreakable Enterprise Kernel Release 5 for Oracle Linux 7Server (x86_64) - Archive                             245
ol7_UEKR6/x86_64                        Latest Unbreakable Enterprise Kernel Release 6 for Oracle Linux 7Server (x86_64)                                 71
ol7_UEKR6_RDMA/x86_64                   Oracle Linux 7 UEK6 RDMA (x86_64)                                                                                34
ol7_addons/x86_64                       Oracle Linux 7Server Add ons (x86_64)                                                                           411
ol7_kvm_utils/x86_64                    Oracle Linux 7Server KVM Utilities (x86_64)                                                                     441
ol7_latest/x86_64                       Oracle Linux 7Server Latest (x86_64)                                                                         16,661
ol7_latest_archive/x86_64               Oracle Linux 7Server Latest (x86_64) - Archive                                                               24,368
ol7_optional_archive/x86_64             Oracle Linux 7Server Optional (x86_64) - Archive                                                             19,061
ol7_optional_latest/x86_64              Oracle Linux 7Server Optional Latest (x86_64)                                                                12,153
ol7_security_validation/x86_64          Oracle Linux 7Server (x86_64) Security Validations                                                               86
ol7_software_collections/x86_64         Software Collection Library release 3.0 packages for Oracle Linux 7 (x86_64)                                 14,433
ol7_u0_base/x86_64                      Oracle Linux 7Server GA installation media copy (x86_64)                                                      6,171

```
