---
title: "wierd node webpack error"
date: 2020-01-17
categories: 
  - "fsse"
tags: 
  - "error"
  - "node"
  - "webpack"
---

wierd node webpack error

```
$ NODE_PATH=/usr/local/lib/node_modules webpack
Invalid configuration object. Webpack has been initialised using a configuration object that does not match the API schema.
- configuration.module.rules[0].exclude should be one of these:
RegExp | string | function | [(recursive)] | object { and?, exclude?, include?, not?, or?, test? } | [RegExp | string | function | [(recursive)] | object { and?, exclude?, include?, not?, or?, test? }]
-> One or multiple rule conditions
Details:
* configuration.module.rules[0].exclude[1]: The provided value "!/node_modules/idb-file-storage" is not an absolute path!
* configuration.module.rules[0].exclude[1]: The provided value "!/node_modules/idb-file-storage" is not an absolute path!
```

and

```
# npm -g install babel-loader
/usr/local/lib
├── UNMET PEER DEPENDENCY @babel/core@^7.0.0
├── babel-loader@8.0.6 
└── UNMET PEER DEPENDENCY webpack@>=2

```
