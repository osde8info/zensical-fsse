---
title: "php ini_get may return unexpected results !"
date: 2013-08-14
categories: 
  - "fsse"
tags: 
  - "inifile"
  - "php"
  - "webdev"
---

_Many ini memory size values, such as upload\_max\_filesize, are stored in the php.ini file in **shorthand** notation. ini\_get() will return the exact string stored in the php.ini file and NOT its integer equivalent. Attempting normal arithmetic functions on these values will not have otherwise expected results._

- http://www.php.net/manual/en/function.ini-get.php
