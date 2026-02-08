---
title: "node &amp; javascript ecmascript include import and export"
date: 2019-05-10
categories: 
  - "fsse"
tags: 
  - "import"
  - "include"
  - "javascript"
  - "node"
---

javascript ecmascript include import and export

https://stackoverflow.com/questions/39436322/node-js-syntaxerror-unexpected-token-import#

_While `import` is indeed part of ES6, it is unfortunately not yet supported in NodeJS by default, and has only very recently landed support in browsers._

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import

rename your .JS files to .MJS then run

```
$ node --experimental-modules my-app.mjs
```
