---
title: "ssh without passwords"
date: 2013-06-03
categories: 
  - "fsse"
tags: 
  - "ed-k-l-x-ubuntu"
  - "security"
  - "ssh"
  - "sysadmin"
---

local host

- ssh-keygen -t rsa
- cd .ssh
- vi id\_rsa.pub (COPY SSH KEY)

remote host

- ssh-keygen -t rsa
- cd .ssh
- touch authorized\_keys
- chmod 600 authorized\_keys
- vi authorized\_keys (PASTE SSH KEY)

see also

- http://www.debian.org/devel/passwordlessssh
- http://www.eng.cam.ac.uk/help/jpmg/ssh/authorized\_keys\_howto.html
- https://help.ubuntu.com/community/SSH/OpenSSH/Keys
