---
title: "oracle linux 8 nginx.x, node.x, python.x, ruby.x"
date: 2022-12-24
categories: 
  - "fsse"
---

oracle linux 8 yum repos contain multiple versions of nginx, node 10 & 12 & 14 & 16 & 18 , python and ruby and more

type

`# dnf module list`

to get a list of modules with multiple versions

type

`# dnf module list nodejs`

to get a list of all the node versions available

```
# dnf module list nodejs
Last metadata expiration check: 3:55:06 ago on Sat 24 Dec 2022 01:04:27 PM GMT.
Oracle Linux 8 Application Stream (x86_64)
Name                Stream               Profiles                                           Summary
nodejs              10 [d]               common [d], development, minimal, s2i              Javascript runtime
nodejs              12                   common [d], development, minimal, s2i              Javascript runtime
nodejs              14                   common [d], development, minimal, s2i              Javascript runtime
nodejs              16 [e]               common [d], development, minimal, s2i              Javascript runtime
nodejs              18                   common [d], development, minimal, s2i              Javascript runtime

Oracle Linux 8 EPEL Modular Packages for Development (x86_64)
Name                Stream               Profiles                                           Summary
nodejs              13                   default, development, minimal                      Javascript runtime
nodejs              16-epel              default, development, minimal                      Javascript runtime

Hint: [d]efault, [e]nabled, [x]disabled, [i]nstalled
```

for example if you want to install node 16 type  

```
# dnf module enable nodejs:16
# dnf install nodejs
```

refs

https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-centos-8

[![](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/image-11.png?w=1024)](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/image-11.png)
