---
title: "vercel nuxt quickstart"
date: 2025-09-20
categories: 
  - "fsse"
---

create vercel nuxt quickstart project in vercel web ui then

locally

ROOT

```
npm install -g pnpmnpm install -g nuxt
```

WINDOW 1

```
git clone git@gitlab.com:osde8info/vercel-nuxtjs-boilerplate.git
cd vercel-nuxtjs-boilerplate
```

```
npm installvercel buildnuxt dev
```

WINDOW 2

```
git config --global user.email "yourname@example.com"
git config --global user.name "Your Name"

git branch dev
git switch dev

vi app.vue

git push --set-upstream origin dev
git add .
git commit -m "patch"
git push

vercel --prod
```
