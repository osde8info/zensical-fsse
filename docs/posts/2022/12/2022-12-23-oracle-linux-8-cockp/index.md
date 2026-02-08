---
title: "oracle linux 8 cockpit pcp error"
date: 2022-12-23
categories: 
  - "fsse"
---

if you see errors on oracle linux 8 cockpit metrics overview about pcp & pmlogger try installing pcp-oracle-conf

```
# dnf install pcp-oracle-conf
Last metadata expiration check: 2:16:08 ago on Fri 23 Dec 2022 07:12:13 PM GMT.
Dependencies resolved.
=================================================================================================================== Package                          Architecture       Version                       Repository                 Size
===================================================================================================================Installing:
 pcp-oracle-conf                  x86_64             1-5.0.1.el8                   ol8_addons                 22 k
Installing dependencies:
 pcp-doc                          noarch             5.3.7-7.0.2.el8               ol8_appstream             2.9 M
 pcp-pmda-dm                      x86_64             5.3.7-7.0.2.el8               ol8_appstream              75 k
 pcp-pmda-nfsclient               x86_64             5.3.7-7.0.2.el8               ol8_appstream              55 k
 pcp-pmda-openmetrics             x86_64             5.3.7-7.0.2.el8               ol8_appstream              65 k
 pcp-system-tools                 x86_64             5.3.7-7.0.2.el8               ol8_appstream             320 k
 pcp-zeroconf                     x86_64             5.3.7-7.0.2.el8               ol8_appstream              54 k
 python3-pcp                      x86_64             5.3.7-7.0.2.el8               ol8_appstream             178 k
```

see also

https://access.redhat.com/documentation/en-us/red\_hat\_enterprise\_linux/8/html/managing\_systems\_using\_the\_rhel\_8\_web\_console/getting-started-with-the-rhel-8-web-console\_system-management-using-the-rhel-8-web-console#doc-wrapper

[![](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/image-4.png?w=1024)](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/image-4.png)
