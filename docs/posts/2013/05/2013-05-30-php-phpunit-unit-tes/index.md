---
title: "#php #phpunit unit testing"
date: 2013-05-30
categories: 
  - "fsse"
tags: 
  - "pear"
  - "php"
  - "phpunit"
  - "tdd"
  - "testing"
  - "unit-testing"
  - "webdev"
---

there are a number of php pear phpunit unit test librarys floating around 1.3.2, 2.3.6, 3.7.21 & 3.8.x but currently i would NOT install OLD versions of phpunit from ubuntu repo or default pear repo BUT install phpunit 3.7.21 from phpunit.de instead

- [pear.phpunit.de/](http://pear.phpunit.de/)
- [phpunit.de/manual/current/en/index.html](http://phpunit.de/manual/current/en/index.html)
- [github.com/sebastianbergmann/phpunit/](https://github.com/sebastianbergmann/phpunit/)
- [phpunit.de/manual/3.7/en/writing-tests-for-phpunit.html](http://phpunit.de/manual/3.7/en/writing-tests-for-phpunit.html#writing-tests-for-phpunit.assertions.assertEquals)

using

```
# pear channel-discover pear.phpunit.de
# pear channel-discover pear.symfony.com
# pear remote-list -c phpunit
# pear install --alldeps phpunit/PHPUnit
VERIFY INSTALL WITH
# pear list -c phpunit
```
