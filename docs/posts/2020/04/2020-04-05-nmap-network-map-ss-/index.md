---
title: "nmap (network map) &amp; ss (socket statistics) #devops #netadmin #sysadmin"
date: 2020-04-05
categories: 
  - "fsse"
tags: 
  - "devops"
  - "netadmin"
  - "nmap"
  - "ss"
  - "sysadmin"
---

nmap (network map) & ss (socket statistics) #devops #netadmin #sysadmin

nmap localhost

```
[root@localhost ~]# nmap localhost
Starting Nmap 7.70 ( https://nmap.org ) at 2020-04-05 10:05 BST
Nmap scan report for localhost (127.0.0.1)
Host is up (0.000016s latency).
Other addresses for localhost (not scanned): ::1
Not shown: 996 closed ports
PORT STATE SERVICE
22/tcp open ssh
111/tcp open rpcbind
631/tcp open ipp
9090/tcp open zeus-admin
```

Nmap done: 1 IP address (1 host up) scanned in 1.65 seconds

ss -ntl

```
[root@localhost ~]# ss -ntl
State Recv-Q Send-Q Local Address:Port Peer Address:Port 
LISTEN 0 5 127.0.0.1:4330 0.0.0.0:* 
LISTEN 0 64 127.0.0.1:46447 0.0.0.0:* 
LISTEN 0 128 0.0.0.0:111 0.0.0.0:* 
LISTEN 0 32 192.168.122.1:53 0.0.0.0:* 
LISTEN 0 128 0.0.0.0:22 0.0.0.0:* 
LISTEN 0 5 127.0.0.1:631 0.0.0.0:* 
LISTEN 0 128 127.0.0.1:6010 0.0.0.0:* 
LISTEN 0 128 127.0.0.1:8125 0.0.0.0:* 
LISTEN 0 64 127.0.0.1:40703 0.0.0.0:* 
LISTEN 0 128 0.0.0.0:19999 0.0.0.0:* 
LISTEN 0 5 127.0.0.1:44321 0.0.0.0:* 
LISTEN 0 5 [::1]:4330 [::]:* 
LISTEN 0 128 [::]:111 [::]:* 
LISTEN 0 128 [::]:22 [::]:* 
LISTEN 0 5 [::1]:631 [::]:* 
LISTEN 0 128 [::1]:6010 [::]:* 
LISTEN 0 128 [::1]:8125 [::]:* 
LISTEN 0 128 [::]:19999 [::]:* 
LISTEN 0 5 [::1]:44321 [::]:* 
LISTEN 0 128 *:9090 *:*
```
