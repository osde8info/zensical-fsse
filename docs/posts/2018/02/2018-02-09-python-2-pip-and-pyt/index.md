---
title: "python 2 pip and python 3 pip wierdness"
date: 2018-02-09
categories: 
  - "fsse"
tags: 
  - "pip"
  - "python"
  - "python3"
---

python 2 pip and python 3 pip wierdness bizarrely if you run

```
# aptitude install python3-pip
# pip3 install --upgrade pip
```

you will end up with the following files

```
# ls -l /usr/local/bin/
total 24
-rwxr-xr-x 1 root root 205 Feb 9 13:08 pip
-rwxr-xr-x 1 root root 205 Feb 9 13:08 pip3
-rwxr-xr-x 1 root root 205 Feb 9 13:08 pip3.5
```

and so bizarrely if you type pip it will now run pip3 !
