---
title: "#php serialize() encodes null's as 'N'"
date: 2015-09-15
categories: 
  - "fsse"
tags: 
  - "encode"
  - "null"
  - "php"
  - "serialise"
  - "serialize"
---

php serialize() encodes null's as the character 'N'

- http://php.net/manual/en/language.oop5.serialization.php
- http://php.net/manual/en/function.serialize.php#66147

```
IN 
<?php
$a = array('a'=>123,'b'=>NULL);
echo serialize($a);
?>

OUT
a:2:{s:1:"a";i:123;s:1:"b";N;}
```
