---
title: "node npm global modules"
date: 2019-05-12
categories: 
  - "fsse"
tags: 
  - "list"
  - "modules"
  - "node"
  - "npm"
---

node npm global modules can be found in /usr/lib/node\_modules and /usr/lib/node\_modules/npm

install with

```
# npm -g install dotenv
```

list with

```
$ ls /usr/lib/node_modules/
or
$ ls /usr/local/lib/node_modules/
or
$ ls /usr/share/npm/node_modules/
```

or recursively with

```
$ npm -g list
```

to run node with global modules set the NODE\_PATH environment variable

```
$ NODE_PATH=/usr/lib/node_modules/ node myapp.js
```
