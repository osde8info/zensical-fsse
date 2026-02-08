---
title: "opensuse does not install SSL ca certs"
date: 2020-03-21
categories: 
  - "fsse"
tags: 
  - "certificates"
  - "ssl"
---

opensuse does not install SSL ca certs and you will get SSL certificate errors from WGET and GIT CLONE until you

`# zypper install ca-certificates{,-cacert,-mozilla}`

refs

- https://stackoverflow.com/questions/33353569/cannot-use-ssl-certificate-when-using-git-on-opensuse
