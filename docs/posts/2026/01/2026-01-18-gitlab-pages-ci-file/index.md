---
title: "gitlab pages ci file needs pages:true"
date: 2026-01-18
categories: 
  - "fsse"
---

the gitlab ci/cd file (.gitlab-ci.yml) for gitlabpages needs pages:true to generate your project-HASH.gitlab.io site

```
dpl:
  stage: deploy
  pages: true
  
```

this will appear as a magic step in your deploy pipeline

```
deploy
  dpl
  pages:deploy
  
```

[https://docs.gitlab.com/user/project/pages/#using-gitlab-pages](https://docs.gitlab.com/user/project/pages/#using-gitlab-pages)
