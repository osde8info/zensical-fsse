---
title: "red hat nginx php fpm nginx config"
date: 2016-03-22
categories: 
  - "fsse"
---

red hat nginx php fpm nginx config

```
    location / {
        # First attempt to serve request as file, then
        # as directory, then fall back to displaying a 404.
        # try_files $uri $uri/ =404;
        try_files $uri $uri/ index.js /index.php$is_args$args;
    }

    # pass the PHP scripts to FastCGI server listening on 127.0.0.1:9000
    #
    location ~ \.php$ {
        index  index.html index.htm index.php;
        fastcgi_index index.php;
        fastcgi_param SCRIPT_FILENAME $request_filename;
        fastcgi_pass 127.0.0.1:9000;
        fastcgi_split_path_info ^(.+\.php)(/.*)$;
        include fastcgi_params;
    }
```
