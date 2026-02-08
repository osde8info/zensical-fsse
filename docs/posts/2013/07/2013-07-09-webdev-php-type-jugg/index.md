---
title: "#webdev #php type juggling"
date: 2013-07-09
categories: 
  - "fsse"
tags: 
  - "conversion"
  - "php"
  - "types"
  - "webdev"
---

#webdev #php type juggling and casting and converting to int

- http://www.php.net/manual/en/language.types.type-juggling.php
- http://php.net/manual/en/language.types.integer.php
- http://www.php.net/manual/en/function.intval.php

`<!--?php  `

PHP `echo 'is_int'.PHP_EOL; echo is_int(1).PHP_EOL; echo is_int('1').PHP_EOL; echo is_int('a').PHP_EOL; echo is_int('1234').PHP_EOL; echo 'is_numeric'.PHP_EOL; echo is_numeric(1).PHP_EOL; echo is_numeric('1').PHP_EOL; echo is_numeric('a').PHP_EOL; echo is_numeric('1234').PHP_EOL; echo intval(420000000000000000000).PHP_EOL; // 0 echo intval('420000000000000000000').PHP_EOL; // 2147483647`

RETURNS `is_int 1 - is_numeric 1 1 - 1 0 9223372036854775807`
