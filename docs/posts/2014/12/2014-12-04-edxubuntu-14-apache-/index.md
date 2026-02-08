---
title: "ed/x/ubuntu 14 apache apache2 apache2ctl -S"
date: 2014-12-04
categories: 
  - "fsse"
tags: 
  - "apache"
  - "sysadmin"
  - "ubuntu"
---

if you are running apache on ubuntu 14 dont use apache2 but use apache2ctl instead if you dont want to get AH00111 config variable $ is not defined errors !

```
# apache2 -S

[core:warn] [pid 4998] AH00111: Config variable ${APACHE_LOCK_DIR} is not defined
[core:warn] [pid 4998] AH00111: Config variable ${APACHE_PID_FILE} is not defined
[core:warn] [pid 4998] AH00111: Config variable ${APACHE_RUN_USER} is not defined
[core:warn] [pid 4998] AH00111: Config variable ${APACHE_RUN_GROUP} is not defined
[core:warn] [pid 4998] AH00111: Config variable ${APACHE_LOG_DIR} is not defined
AH00526: Syntax error on line 74 of /etc/apache2/apache2.conf:
Invalid Mutex directory in argument file:${APACHE_LOCK_DIR}

# apache2ctl -S
ServerRoot: "/etc/apache2"
Main DocumentRoot: "/var/www"
Main ErrorLog: "/var/log/apache2/error.log"
Mutex default: dir="/var/lock/apache2" mechanism=fcntl 
Mutex mpm-accept: using_defaults
Mutex watchdog-callback: using_defaults
Mutex rewrite-map: using_defaults
PidFile: "/var/run/apache2/apache2.pid"
Define: DUMP_VHOSTS
Define: DUMP_RUN_CFG
User: name="www-data" id=33
Group: name="www-data" id=33

```

thanks to

- http://www.howdididothat.info/category/server-administration/web-server-administration/apache/
