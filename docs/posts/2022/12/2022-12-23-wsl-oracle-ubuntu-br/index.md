---
title: "wsl oracle &amp; ubuntu broken CA certificates and X509 unknown authority errors"
date: 2022-12-23
categories: 
  - "fsse"
---

wsl oracle & ubuntu broken CA certificates and X509 unknown authority errors

```
Oracle Linux 8 BaseOS Latest (x86_64)                                                      0.0  B/s |   0  B     00:00
Errors during downloading metadata for repository 'ol8_baseos_latest':
  - Curl error (60): 
Peer certificate cannot be authenticated with given CA certificates for 
https://yum.oracle.com/repo/OracleLinux/OL8/baseos/latest/x86_64/repodata/repomd.xml 
  [SSL certificate problem: unable to get local issuer certificate]
Error: Failed to download metadata for repo 'ol8_baseos_latest': 
Cannot download repomd.xml: 
Cannot download repodata/repomd.xml: All mirrors were tried

error: cannot perform the following tasks:
- Download snap "firefox" (2211) from channel "stable" 
(Get "https://canonical-bos01.cdn.snapcraftcontent.com/download-origin/canonical-lgw01/3wdHCAVyZEmYsCMFDE9qt92UV8rC8Wdk_2211.snap?interactive=1&token=1671822000_722ad9892a6405812a747988934f480445a9572a": 
x509: certificate signed by unknown authority)
- Download snap "gnome-3-38-2004" (119) from channel "stable" 
(Get "https://canonical-lgw01.cdn.snapcraftcontent.com/download-origin/canonical-lgw01/rw36mkAjdIKl13dzfwyxP87cejpyIcct_119.snap?interactive=1&token=1671822000_1a5cdcdfce0b22c557049c9ec86ea225c8fa5906": 
x509: certificate signed by unknown authority)
```
