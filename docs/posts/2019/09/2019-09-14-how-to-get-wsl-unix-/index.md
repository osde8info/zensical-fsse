---
title: "how to get WSL UNIX commands without sysadmin rights"
date: 2019-09-14
categories: 
  - "fsse"
tags: 
  - "command-line"
  - "gnu-linux"
  - "linux"
  - "unix"
  - "utils"
---

On Windows 10 you cant install WSL without sysadmin rights so you have to use CYGWIN instead

- https://cygwin.com/faq.html#faq.setup.noroot

_Can I install Cygwin without administrator rights?_

_Yes. The default installation requests administrator rights because this allows to set up the Cygwin environment so that all users can start a Cygwin shell out of the box._

_However, if you don't have administrator rights for your machine, and the admins don't want to install it for you, you can install Cygwin just for yourself by downloading setup-x86.exe (for a 32 bit install) or setup-x86\_64.exe (for a 64 bit install) and then start it from the command line or via the "Run..." dialog from the start menu using the --no-admin option, for instance:_

```
#  setup-x86.exe --no-admin
```
