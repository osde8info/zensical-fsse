---
title: "reconfigure your @vercel @next @node project settings before 09aug22 when node.js 12 will be deprecated in favor of node.js 16"
date: 2022-06-24
categories: 
  - "fsse"
---

reconfigure your @vercel @next @node project settings before 09aug22 when node.js 12 will be deprecated in favor of node.js 16

first rename `now.json` to `vercel.json` and any "use" : `@now/node to @vercel/node`

```
Error: Node.js version 12.x is deprecated. 
Deployments created on or after 2022-08-09 will fail to build. 
Please set Node.js Version to 16.x in your Project Settings to use Node.js 16. 
This change is the result of a decision made by an upstream infrastructure provider (AWS).
```

see also

- https://vercel.com/changelog/node-js-12-is-being-deprecated
- https://vercel.com/docs/errors

node 12 EOL

- https://nodejs.org/en/blog/release/v12.22.12/
