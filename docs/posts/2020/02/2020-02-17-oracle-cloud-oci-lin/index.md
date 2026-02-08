---
title: "oracle cloud oci linux &amp; node &amp; theai install"
date: 2020-02-17
categories: 
  - "fsse"
tags: 
  - "ide"
  - "node"
  - "npm"
  - "oci"
  - "theia"
  - "webdev"
  - "yarn"
---

install theai prereqs (as root)

```
# yum install gcc
# yum install gcc-c++
# yum install nodejs
# npm -g install yarn

```

build theia

```
    
$ mkdir mytheia
$ cd mytheia
$ vi package.json 
$ # (C&P from https://theia-ide.org/docs/composing_applications)
$ yarn # will autoinstall everything from your package.json
$ yarn theia build (takes approx 400 seconds)

```

start theia

```
$ cd mytheia
$ nohup yarn theia start &
```

create a SSH tunnel from your local PC to remote OCI

```
$ ssh -L 3000:localhost:3000 opc@my.oci.vm -N &
```

open http://localhost:3000
