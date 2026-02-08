---
title: "eclipse red robotframework problems"
date: 2018-02-09
categories: 
  - "fsse"
tags: 
  - "eclipse"
  - "python3"
  - "red"
  - "robotframework"
---

if you having a problem getting eclipse red to run python 3 robotframework libraries/modules/packages

try running pip3 as root so that the libraries/modules/packages end up installed globally instead of a hidden .local directory

```
# pip3 install --upgrade pip
# pip3 install robotframework 
# pip3 install robotframework-seleniumlibrary

# ls -l /usr/local/bin/
total 24
lrwxrwxrwx 1 root root 17 Feb 9 13:50 chromedriver -> /opt/chromedriver
lrwxrwxrwx 1 root root 16 Feb 9 13:32 geckodriver -> /opt/geckodriver
-rwxr-xr-x 1 root root 205 Feb 9 13:08 pip
-rwxr-xr-x 1 root root 205 Feb 9 13:08 pip3
-rwxr-xr-x 1 root root 205 Feb 9 13:08 pip3.5
-rwxr-xr-x 1 root root 80 Feb 9 13:11 pybot
-rwxr-xr-x 1 root root 202 Feb 9 13:11 rebot
-rwxr-xr-x 1 root root 198 Feb 9 13:11 robot
```
