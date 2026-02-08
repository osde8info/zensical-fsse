---
title: "wigle now has an api #netadmin #wifi #wardriving"
date: 2023-01-02
categories: 
  - "fsse"
---

the wigle wifi search engine that contains 980M wifi networks discovered (/wardriven/) worldwide

now has an api (so you can get back 10+ years of wifi wardriving data IF you been using wigle for 10+ years !)

- https://wigle.net/account

- https://api.wigle.net/swagger#/

```
$ curl -i -H 'Accept:application/json' -u X:Y --basic https://api.wigle.net/api/v2/profile/user

HTTP/1.1 200 OK
Server: nginx/1.22.0
Date: Mon, 02 Jan 2023 07:39:08 GMT
Content-Type: application/json
Content-Length: 182
Connection: keep-alive
Vary: Accept-Encoding
Strict-Transport-Security: max-age=63072000; includeSubdomains; preload

{
"userid":"osde8info",
"email":"me",
"donate":"Y",
"joindate":"2010-09",
"lastlogin":"2023-01",
"flags":0,"session":null,"success":"true"
}
```

[![](https://fsse8info.wordpress.com/wp-content/uploads/2023/01/image.png?w=1024)](https://fsse8info.wordpress.com/wp-content/uploads/2023/01/image.png)
