---
title: "ubuntu - cmdtest yarn v node yarn"
date: 2019-05-29
categories: 
  - "fsse"
tags: 
  - "node"
  - "ubuntu"
  - "yarn"
---

ubuntu - cmdtest yarn v node yarn (https://yarnpkg.com/en/)

to run node yarn instead of cmdtest yarn you will need to use npm

```
# npm install -g yarn
```

and then specify full path to node yarn

```
$ /usr/local/bin/yarn
yarn install v1.16.0
[1/4] Resolving packages...
[2/4] Fetching packages...

error electron-builder@20.39.0: 
The engine "node" is incompatible with this module. 
Expected version ">=8.12.0". Got "8.10.0"

error Found incompatible module.

info Visit https://yarnpkg.com/en/docs/cli/install 
for documentation about this command.
```

good luck
