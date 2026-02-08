---
title: "aptitude safe-upgrade seems to downgrade unsafe apps ?"
date: 2018-02-09
categories: 
  - "fsse"
tags: 
  - "apt"
  - "aptitude"
  - "downgrade"
  - "update"
  - "upgrade"
---

aptitude safe-upgrade seems to downgrade unsafe apps ?

i installed openjdk-9-jdk then ran aptitude safe-upgrade and it said it would REMOVE the following packages

```
 # aptitude safe-upgrade
The following packages will be REMOVED: 
 ca-certificates-java{u} fonts-dejavu-extra{u} java-common{u} libatk-wrapper-java{u} libatk-wrapper-java-jni{u} 
 libice-dev{u} libpthread-stubs0-dev{u} libsm-dev{u} libx11-dev{u} libx11-doc{u} libxau-dev{u} libxcb1-dev{u} 
 libxdmcp-dev{u} libxt-dev{u} openjdk-9-jdk-headless{u} openjdk-9-jre{u} openjdk-9-jre-headless{u} 
 x11proto-core-dev{u} x11proto-input-dev{u} x11proto-kb-dev{u} xorg-sgml-doctools{u} xtrans-dev{u} 
0 packages upgraded, 0 newly installed, 22 to remove and 0 not upgraded.
Need to get 0 B of archives. After unpacking 333 MB will be freed.
Do you want to continue? [Y/n/?] n
```
