---
title: "all about node async await asynchronous and synchronous functions"
date: 2019-05-11
categories: 
  - "fsse"
tags: 
  - "asynchronous"
  - "functions"
  - "js"
  - "node"
  - "synchronous"
---

all about node async await asynchronous and synchronous functions

- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async\_function
- https://blog.risingstack.com/node-hero-async-programming-in-node-js/
- https://blog.risingstack.com/mastering-async-await-in-nodejs/#

you can find more node tutorials at

- https://blog.risingstack.com/node-hero-tutorial-getting-started-with-node-js/
- https://blog.risingstack.com/nodejs-at-scale-npm-best-practices/

node js sleep() example

```
function sleep(ms) {
  return new Promise(resolve => setTimeout(resolve, ms));
}

async function addprop(obj) {
        await sleep(2000);
        obj.deps = {};
}

var tree={};

addprop(tree);
console.log(tree);
addprop(tree.deps);
console.log(tree);
addprop(tree.deps.deps);
console.log(tree);

```
