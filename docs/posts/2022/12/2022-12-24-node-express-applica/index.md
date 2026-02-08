---
title: "node express application generator"
date: 2022-12-24
categories: 
  - "fsse"
---

node express application generator

```
$ npx express-generator --view=pug
$ npm install
$ DEBUG=myproject:* npm start
```

npx output

```
   create : public/
   create : public/javascripts/
   create : public/images/
   create : public/stylesheets/
   create : public/stylesheets/style.css
   create : routes/
   create : routes/index.js
   create : routes/users.js
   create : views/
   create : views/error.pug
   create : views/index.pug
   create : views/layout.pug
   create : app.js
   create : package.json
   create : bin/
   create : bin/www
```

npm start output

```
> myproject@0.0.0 start
> node ./bin/www

  myproject:server Listening on port 3000 +0ms
GET / 304 577.229 ms - -
GET /stylesheets/style.css 200 20.472 ms - 111
GET / 304 25.413 ms - -
GET /stylesheets/style.css 304 1.708 ms - -
```

http://expressjs.com/en/starter/generator.html

[![](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/image-12.png?w=1024)](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/image-12.png)
