---
title: "#python uses #ascii instead of #unicode by default #gotcha"
date: 2015-11-27
categories: 
  - "fsse"
tags: 
  - "gotcha"
  - "python"
  - "unicode"
  - "utf8"
---

by default python seems to run in ascii which means if you try and process a string with a utf-8 unicode character in it you will get the error

```
UnicodeEncodeError: 'ascii' codec can't encode character 
u'\xXX' in position YYYYY: ordinal not in range(128)
```

so to force your script to use utf-8 unicode instead you need to

see http://nedbatchelder.com/text/unipain.html and

```
import sys
reload(sys)
sys.setdefaultencoding('utf8')
print sys.getdefaultencoding()
```
