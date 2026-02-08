---
title: "create #graphql &amp; #rest #apis with @vercel @nextjs @node in 10 mins #webdev"
date: 2021-01-15
categories: 
  - "fsse"
---

create #graphql & #rest #apis with @vercel @nextjs @node in 10 mins

node

- https://www.codementor.io/@olatundegaruba/nodejs-restful-apis-in-10-minutes-q0sgsfhbd
- https://www.kindsonthegenius.com/nodejs/rest-api/
- https://medium.com/the-node-js-collection/10-best-practices-for-writing-node-js-rest-apis-7643a7765cd
- http://mfikri.com/en/blog/nodejs-restful-api-mysql
- https://www.toptal.com/nodejs/secure-rest-api-in-nodejs
- https://www.tutorialspoint.com/nodejs/nodejs\_restful\_api.htm

vercel nextjs

- https://frontend-devops.com/blog/build-deploy-a-vercel-api
- https://nextjs.org/docs/api-routes/introduction
- https://github.com/apollographql/apollo-server/tree/main/packages/apollo-server-micro
- https://github.com/vercel/next.js/tree/canary/examples/api-routes-graphql
- https://github.com/vercel/next.js/tree/canary/examples/api-routes-rest

curl result

```
$ curl 'http://localhost:3000/graphql' -H 'Accept-Encoding: gzip, deflate, br' -H 'Content-Type: application/json' -H 'Accept: application/json' -H 'Connection: keep-alive' -H 'DNT: 1' -H 'Origin: http://localhost:3000' --data-binary '{"query":"{sayHello}"}' --compressed

{"data":{"sayHello":"Hello World!"}}
```

browser result

[![](https://fsse8info.wordpress.com/wp-content/uploads/2021/01/screenshot_2021-01-15-playground-http-localhost-3000-graphql.png?w=1024)](https://fsse8info.wordpress.com/wp-content/uploads/2021/01/screenshot_2021-01-15-playground-http-localhost-3000-graphql.png)
