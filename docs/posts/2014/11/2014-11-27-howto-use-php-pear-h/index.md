---
title: "howto use php pear horde utilities whilst avoiding the ubuntu14 apache2 php5 pear includefile bug"
date: 2014-11-27
categories: 
  - "fsse"
tags: 
  - "diff"
  - "horde"
  - "pear"
  - "php"
---

on an ubuntu 14 apache 2 php 5 install if you look at your php include\_path it may look like this

```
include_path .:/usr/share/php:/usr/share/pear 

```

which is WRONG because there is no /usr/share/pear directory in fact on ubuntu 14 php 5 pear is installed in /usr/share/php/PEAR and horde is installed in /usr/share/php/Horde

so to enable autoloading to allow you to automatically use a horde class just

install pear horde

```
# pear channel-discover pear.horde.org
# pear install horde/Horde_Autoloader
# pear install horde/Horde_Text_Diff

```

then

```
require_once 'Horde/Autoloader/Default.php';

```

then whenever you use any horde class library (that you have previously downloaded and installed) it will be autoloaded

```
$check_diff = new Horde_Text_Diff( 'auto', array($a_lines, $b_lines) );
$renderer = new Horde_Text_Diff_Renderer_Inline();

```
