---
title: "browser extensions DIY"
date: 2020-01-17
categories: 
  - "fsse"
tags: 
  - "api"
  - "browser"
  - "extension"
  - "w3c"
---

browser extensions DIY

docs and github

- https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions
- https://github.com/mdn/webextensions-examples

dev.to articles

- https://dev.to/search?q=browser%20extension

so far so  good but just got an error

```
webpack --display-error-details --progress --colors

Invalid configuration object. Webpack has been initialised using a configuration object that does not match the API schema.
 - configuration.module.rules[0].exclude should be one of these:
   RegExp | string | function | [(recursive)] | object { and?, exclude?, include?, not?, or?, test? } | [RegExp | string | function | [(recursive)] | object { and?, exclude?, include?, not?, or?, test? }]
   -> One or multiple rule conditions
   Details:
    * configuration.module.rules[0].exclude[1]: The provided value "!/node_modules/idb-file-storage" is not an absolute path!
    * configuration.module.rules[0].exclude[1]: The provided value "!/node_modules/idb-file-storage" is not an absolute path!
```
