---
title: "OracleLinux 8 dnf &amp; yum repos"
date: 2022-12-20
categories: 
  - "fsse"
---

OracleLinux 8 dnf & yum repos

- https://yum.oracle.com/getting-started.html#installing-software-from-oracle-linux-yum-server

```
# dnf list *release-el8
# dnf install oraclelinux-developer-release-el8
# dnf install oracle-epel-release-el8
# dnf repolist

# dnf repolist
repo id                                          repo name
ol8_UEKR6                                        Latest Unbreakable Enterprise Kernel Release 6 for Oracle Linux 8 (x86_64)
ol8_appstream                                    Oracle Linux 8 Application Stream (x86_64)
ol8_baseos_latest                                Oracle Linux 8 BaseOS Latest (x86_64)
ol8_developer                                    Oracle Linux 8 Development Packages (x86_64)
ol8_developer_EPEL                               Oracle Linux 8 EPEL Packages for Development (x86_64)
ol8_developer_EPEL_modular                       Oracle Linux 8 EPEL Modular Packages for Development (x86_64)
```
