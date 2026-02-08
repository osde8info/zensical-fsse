---
title: "php and notepad unicode files"
date: 2015-07-22
categories: 
  - "fsse"
tags: 
  - "bom"
  - "little-endian"
  - "php"
  - "ucs-2"
  - "unicode"
  - "utf-16"
---

notepad unicode csvfiles have a 2 byte BOM (FEFF) and are UTF-16/UCS-2 little endian encoded

- https://anupamsaha.wordpress.com/2011/08/02/detecting-utf-byte-order-mark-using-php/
- http://www.w3schools.com/php/func\_misc\_pack.asp

```
$ od -t x1z hot.csv | head
0000000 ff fe 48 00 6f 00 74 00 65 00 6c 00 49 00 44 00  >..H.o.t

$ od -t x2z hot.csv | head
0000000 feff 0048 006f 0074 0065 006c 0049 0044  >..H.o.t
```
