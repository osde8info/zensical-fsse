---
title: "php unicode utf-16 bom processing with iconv and mb_convert"
date: 2015-07-22
categories: 
  - "fsse"
tags: 
  - "bom"
  - "convert"
  - "gotcha"
  - "php"
  - "unicode"
  - "utf-16"
  - "utf-8"
  - "webdev"
---

basically php iconv doesnt handle FEFF BOMs while mb\_convert does !

```
        $fh = fopen($s, "r");
        
        // watch out for notepad unicode FEFF BOM
        
        $utf16 = fgets($fh, 1024);

        $utf8 = mb_convert_encoding($utf16,'UTF-8','UTF-16');
        var_export($utf8);
        echo PHP_EOL;

        $utf8 = mb_convert_encoding($utf16,'UTF-8','UTF-16LE');
        var_export($utf8);
        echo PHP_EOL;

        $utf8 = iconv('UTF-16LE','UTF-8',mb_substr($utf16,1,null,'UTF-16LE'));
        var_export($utf8);
        echo PHP_EOL;
```
