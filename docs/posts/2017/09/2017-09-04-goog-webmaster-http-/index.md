---
title: "goog webmaster http https website property gotcha"
date: 2017-09-04
categories: 
  - "fsse"
tags: 
  - "analytics"
  - "goog"
  - "seo"
  - "stats"
  - "webmaster"
---

if you are using webmaster to monitor your http and https websites make sure you set up **separate** website properties for each of them !

- https://www.google.com/webmasters/tools/home
- https://support.google.com/webmasters/answer/34592

_If your site supports multiple protocols (http:// and https://), you must add each as a separate site. Similarly, if you support multiple domains (for example example.com, m.example.com, and www.example.com) you must add each one as a separate site._

its useful to use the goog webmaster tool | CRAWL | FETCH AS GOOGLE to check what the goog crawlers actually see (check they are not seeing a 301 for example)
