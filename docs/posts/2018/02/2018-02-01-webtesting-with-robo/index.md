---
title: "webtesting with robotframework seleniumlibrary and geckodriver"
date: 2018-02-01
categories: 
  - "fsse"
---

webtesting with python 3 robotframework seleniumlibrary and geckodriver

install robotframework

```
# aptitude install python3-tk      # needed for robot dialogs
# aptitude install python3-pip

```

You can run pip3 as root (for best results) or as your user

```
# pip3 install robotframework 
# pip3 install robotframework-seleniumlibrary
```

NOTE: _Selenium2Library has been renamed to SeleniumLibrary since version 3.0. Nowadays Selenium2Library is just a thin wrapper to SeleniumLibrary that eases with transitioning to the new project. See SeleniumLibrary and Selenium2Library project pages for more information._

install gecko driver

```
# wget https://github.com/mozilla/geckodriver/releases/download/v0.19.1/geckodriver-v0.19.1-linux64.tar.gz
# tar zxvf geckodriver-v0.19.1-linux64.tar.gz 
# mv geckodriver /opt/
# ln -s /opt/geckodriver /usr/local/bin
```

then

install eclipse

install nokia red

create and run test.robot

```
*** Settings ***
Library SeleniumLibrary

*** Test Cases ***
test1
   open browser https://github.com/login
   input text     name     user
   input password password password
```

RobotFramework Refs

- https://github.com/robotframework
- https://github.com/robotframework/robotframework

SeleniumLibrary Refs

- https://github.com/robotframework/SeleniumLibrary
- https://pypi.python.org/pypi/robotframework-seleniumlibrary#keyword-documentation

SeleniumLibrary Refs

- http://robotframework.org/#examples
- http://robotframework.org/SeleniumLibrary/
- http://robotframework.org/SeleniumLibrary/SeleniumLibrary.html#Keywords

Gecko Driver Refs

- https://github.com/mozilla/geckodriver
- https://github.com/mozilla/geckodriver/releases

Eclipse RED Refs

- https://github.com/nokia/RED
- https://marketplace.eclipse.org/content/red-robot-editor
