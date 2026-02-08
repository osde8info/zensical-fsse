---
title: "drupal 7 install fails with call to undefined function"
date: 2014-11-21
categories: 
  - "fsse"
tags: 
  - "drupal"
  - "install"
---

if you get

**Fatal error**: Call to undefined function field\_attach\_load() in **/var/www/drupal/includes/entity.inc** on line **316**

just drop all the tables in your drupal db and rerun /install
