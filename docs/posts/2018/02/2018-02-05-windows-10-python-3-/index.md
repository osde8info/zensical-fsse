---
title: "windows 10 python 3 robotframework 3 webdrivers"
date: 2018-02-05
categories: 
  - "fsse"
tags: 
  - "python"
  - "qa"
  - "testing"
  - "webdriver"
  - "webtesting"
---

windows 10 python 3 robotframework 3 seleniumlibrary webdrivers for web testing

install python

- install python (see https://goo.gl/y36JcN)
- pip install robotframework
- pip install robotframework-seleniumlibrary

install browsers

- download and install browsers (chrome, edge, firefox)

download drivers

- https://sites.google.com/a/chromium.org/chromedriver/
- https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/
- https://github.com/mozilla/geckodriver/releases

install webdrivers

- unzip webdrivers
- move exes to a folder in your windows PATH

such as

```
C:\Users\MYUSERNAME\AppData\Local\Microsoft\WindowsApps\
```

then you can run python robot

```
C:\Users\MYUSERNAME> python -m robot mytests.robot
```
