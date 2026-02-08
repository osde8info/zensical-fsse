---
title: "Pelican is a Python static site generator that requires no database or server-side logic"
date: 2022-12-26
categories: 
  - "fsse"
---

Pelican is a Python static site generator that requires no database or server-side logic

https://getpelican.com/

https://github.com/getpelican/pelican

https://github.com/osde8info/pelican-website

https://pelican-website.vercel.app/

run pelican quickstart

```
C:\Users\USER\AppData\Local\Packages\PythonSoftwareFoundation.Python.3.10_qbz5n2kfra8p0\LocalCache\local-packages\Python310\Scripts\pelican-quickstart.exe

```

answer pelican questions

```
Welcome to pelican-quickstart v4.8.0.

This script will help you create a new Pelican-based website.

Please answer the following questions so this script can generate the files
needed by Pelican.

> Where do you want to create your new web site? [.]
> What will be the title of this web site? vercel python pelican
> Who will be the author of this web site? osde.info
> What will be the default language of this web site? [English]
> Do you want to specify a URL prefix? e.g., https://example.com   (Y/n) n
> Do you want to enable article pagination? (Y/n)
> How many articles per page do you want? [10] 3
> What is your time zone? [Europe/Rome] europe/london
> Do you want to generate a tasks.py/Makefile to automate generation and publishing? (Y/n)
> Do you want to upload your website using FTP? (y/N) n
> Do you want to upload your website using SSH? (y/N) n
> Do you want to upload your website using Dropbox? (y/N) n
> Do you want to upload your website using S3? (y/N) n
> Do you want to upload your website using Rackspace Cloud Files? (y/N) n
> Do you want to upload your website using GitHub Pages? (y/N) n

Done. 

Your new project is available at C:\Users\USER\Documents\Git\pelican-website

```

create requirements.txt

```
invoke==1.7.3
Markdown==3.4.1
pelican==4.8.0
```

config vercel project settings

```
build command: make build
output directory : output
```

[![](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/image-26.png?w=399)](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/image-26.png)

create page(s)

`vi ./content/page1.md`

```
Title: My Page
Date: 2010-12-03 10:20
Category: Review

Following is my page
```

create an icon

`touch .content/favicon.ico`

test

`C:\Users\USER\AppData\Local\Packages\PythonSoftwareFoundation.Python.3.10_qbz5n2kfra8p0\LocalCache\local-packages\Python310\Scripts\pelican -r -l`

goto

localhost:8000

[![](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/image-25.png?w=1024)](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/image-25.png)
