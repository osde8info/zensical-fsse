---
title: "apt install \"package is missing, has been obsoleted, or is only available from another source\" msg"
date: 2022-12-23
categories: 
  - "fsse"
---

apt install "package is missing, has been obsoleted, or is only available from another source" msg may NOT mean that

just try running "apt update" then run "apt install" AGAIN

```
# apt install aptitude
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
Package aptitude is not available, but is referred to by another package.
This may mean that the 

package is missing, has been obsoleted, or is only available from another source

E: Package 'aptitude' has no installation candidate

# apt update

# apt install aptitude
SUCCESS
```
