---
title: "oracle linux dnf update \"certificate cannot be authenticated\" error"
date: 2023-01-04
categories: 
  - "fsse"
---

if you are getting errors from oracle linux dnf update such as

```
# dnf update

Oracle Linux 8 BaseOS Latest (x86_64)                                                               

0.0  B/s |   0  B     00:00

Errors during downloading metadata for repository 'ol8_baseos_latest':
  - Curl error (60): 
Peer certificate cannot be authenticated with given CA certificates for https://yum.oracle.com/repo/OracleLinux/OL8/baseos/latest/x86_64/repodata/repomd.xml 
[SSL certificate problem: unable to get local issuer certificate]

Error: Failed to download metadata for repo 'ol8_baseos_latest': 
Cannot download repomd.xml: 
Cannot download repodata/repomd.xml: All mirrors were tried
```

maybe its because you are using ZSCALER and so you can try DISABLING SSL checks by adding `sslverify=0` to your `dnf.conf`

```
$ cat /etc/dnf/dnf.conf
[main]
gpgcheck=1
installonly_limit=3
clean_requirements_on_remove=True
best=True
skip_if_unavailable=False
sslverify=0
```

refs

- [https://support.oracle.com/epmos/faces/DocumentDisplay?\_afrLoop=278360930482824&parent=EXTERNAL\_SEARCH&sourceId=PROBLEM&id=2809683.1&\_afrWindowMode=0&\_adf.ctrl-state=13cad8b22d\_53](https://support.oracle.com/epmos/faces/DocumentDisplay?_afrLoop=278360930482824&parent=EXTERNAL_SEARCH&sourceId=PROBLEM&id=2809683.1&_afrWindowMode=0&_adf.ctrl-state=13cad8b22d_53)
