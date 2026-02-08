---
title: "php use dangers"
date: 2016-02-10
categories: 
  - "fsse"
tags: 
  - "gotcha"
  - "php"
  - "use"
---

php use dangers

example from https://github.com/cakephp/chronos

```
use Cake\Chronos\Date;
$today = new Date();
echo $today;
```

imagine line 2 was actually line 200 how am i supposed to remember that a Date is no longer a PHP Date
