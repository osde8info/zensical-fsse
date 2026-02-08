---
title: "#php ini file #date &amp; #timezone settings"
date: 2013-06-04
categories: 
  - "fsse"
tags: 
  - "datetime"
  - "lamp"
  - "php"
  - "settings"
  - "sysadmin"
  - "timezone"
---

dont forget to edit your php.ini file and add a prefered date timezone to prevent apache httpd php warnings such as:

```
PHP Warning:  date(): It is not safe to rely on the system's timezone 
settings. You are *required* to use the date.timezone setting or 
the date_default_timezone_set() function. 

In case you used any of those methods and you are still getting 
this warning, you most likely misspelled the timezone identifier. 

We selected 'Europe/London' for 'BST/1.0/DST' instead
```

see also

- http://www.uk-cheapest.co.uk/blog/2010/11/php-strict-standards-strtotime-function-strtotime-it-is-not-safe-to-rely-on-the-systems-timezone-settings-please-use-the-date-timezone-setting/
- http://forums.powweb.com/showthread.php?t=82493
- http://www.unixmen.com/timezone-for-php-is-not-set-please-set-qdatetimezoneq-option-in-phpini/
