---
title: "howto get eclipse to use spaces instead of tabs for php files"
date: 2015-02-09
categories: 
  - "annoyance"
  - "eclipse"
  - "php"
  - "spaces"
  - "tabs"
  - "webdev"
---

you need change eclipse settings in 3 three places in order to get eclipse to use spaces for tabs in php files

- general | editors | text editors |
    - displayed tab width = 2
    - insert spaces for tabs

and

- php | editor | typing
    - tab key indents the current line

- php | code style | formatter
    - tab policy = spaces
    - indentation size = 2
    - tab size = 2
    - default indentation for wrapped lines = 2
    - default indentation for array initializers = 2
