---
title: "#webdev #python curl #http post requests"
date: 2015-11-25
categories: 
  - "fsse"
tags: 
  - "curl"
  - "http"
  - "post"
  - "python"
  - "webdev"
---

webdev python curl http requests

- http://docs.python-requests.org/en/latest/user/quickstart/
- http://docs.python-requests.org/en/latest/
- https://gist.github.com/kennethreitz/973705

simple python curl http post request example

```
import requests
url = 'https://www.example.com/'
data = {'requestXml': '<MYREQUESTXML>'}

r = requests.post(url, data)

print 'U '
print url
print 'S '
print r.status_code
print 'H '
print r.headers
print 'T '
print r.text
```
