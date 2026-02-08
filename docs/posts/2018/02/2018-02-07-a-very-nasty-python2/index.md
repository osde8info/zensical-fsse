---
title: "a very nasty python2 python3 hack"
date: 2018-02-07
categories: 
  - "fsse"
tags: 
  - "eclipse"
  - "hack"
  - "python"
  - "python2"
  - "python3"
  - "red"
---

i did have a very nasty python 2 to python 3 hack to get the eclipse ide nokia/RED robot framework editor to work with python 3 but theres a better version below

```
$ cd ~
$ mkdir eclipse-red
$ ln -s /usr/bin/python3 eclipse-red/python
```

after you have created your symlink run eclipse

- and goto `Window → Preferences → Robot Framework → Installed frameworks → Add` 
- and if you are lucky nokia/RED should find Robot Framework 3.0.2 (Python 3.5.2 on linux) instead of the python 2 version

how to use eclipse ide and nokia red with python 3

- https://github.com/filug
- https://github.com/nokia/RED/issues/125
