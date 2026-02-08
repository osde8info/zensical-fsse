---
title: "robotframework selenium-library can be used to generate documentation too"
date: 2018-02-07
categories: 
  - "fsse"
tags: 
  - "documentation"
  - "robotframework"
  - "screenshot"
  - "seleniumlibrary"
  - "webdriver"
---

robotframework selenium-library can be used to generate documentation too

```
*** Setting ***
Library    SeleniumLibrary

Suite Setup	   Suite Init   
Suite Teardown	   Suite Term 

*** Variable ***
${BROWSER}    firefox

*** Test Cases ***
test1
    go to    http://google.com
    Capture Page Screenshot    goo.png
test2
    go to    http://yahoo.co.uk
    Capture Page Screenshot    yah.png
test3
    go to    http://msn.co.uk
    Capture Page Screenshot    msn.png
        
*** Keywords ***
Suite Init
    open browser    http://google.com   ${BROWSER}
    set window size    800    600

Suite Term 
    close browser

```

 

https://www.flickr.com/photos/osde-info/25270569277/in/pool-robotframework/
