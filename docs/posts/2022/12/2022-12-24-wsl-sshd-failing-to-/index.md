---
title: "wsl sshd failing to start"
date: 2022-12-24
categories: 
  - "fsse"
---

if you have multiple or cloned wsl vms SSHD will fail to start with

`error: Bind to port 22 on 0.0.0.0 failed: Address already in use.`

```
# systemctl status ssh
Failed to dump process list for 'ssh.service', ignoring: Input/output error
× ssh.service - OpenBSD Secure Shell server
     Loaded: loaded (/lib/systemd/system/ssh.service; enabled; vendor preset: enabled)
     Active: failed (Result: exit-code) since Sat 2022-12-24 16:13:21 GMT; 35s ago
       Docs: man:sshd(8)
             man:sshd_config(5)
   Main PID: 5540 (code=exited, status=255/EXCEPTION)
      Tasks: 1 (limit: 2282)
     Memory: 3.1M
     CGroup: /system.slice/ssh.service

Dec 24 16:13:21 DESKTOP-EJTS2G0 systemd[1]: ssh.service: Failed to migrate controller cgroups from /system.slice/ssh.service>
Dec 24 16:13:21 DESKTOP-EJTS2G0 systemd[1]: ssh.service: Failed to delete controller cgroups /system.slice/ssh.service, igno>
Dec 24 16:13:21 DESKTOP-EJTS2G0 systemd[1]: Starting OpenBSD Secure Shell server...
Dec 24 16:13:21 DESKTOP-EJTS2G0 sshd[5540]: error: Bind to port 22 on 0.0.0.0 failed: Address already in use.
Dec 24 16:13:21 DESKTOP-EJTS2G0 sshd[5540]: error: Bind to port 22 on :: failed: Address already in use.
Dec 24 16:13:21 DESKTOP-EJTS2G0 sshd[5540]: fatal: Cannot bind any address.
Dec 24 16:13:21 DESKTOP-EJTS2G0 systemd[1]: ssh.service: Main process exited, code=exited, status=255/EXCEPTION
Dec 24 16:13:21 DESKTOP-EJTS2G0 systemd[1]: ssh.service: Failed with result 'exit-code'.
Dec 24 16:13:21 DESKTOP-EJTS2G0 systemd[1]: Failed to start OpenBSD Secure Shell server.
```

edit /etc/sshd\_config and change port from 22 to 2222 or 2233 etc and use systemctl to restart ssh

```
# systemctl start ssh
# systemctl status ssh
Failed to dump process list for 'ssh.service', ignoring: Input/output error
● ssh.service - OpenBSD Secure Shell server
     Loaded: loaded (/lib/systemd/system/ssh.service; enabled; vendor preset: enabled)
     Active: active (running) since Sat 2022-12-24 16:14:03 GMT; 1s ago
       Docs: man:sshd(8)
             man:sshd_config(5)
    Process: 5803 ExecStartPre=/usr/sbin/sshd -t (code=exited, status=0/SUCCESS)
   Main PID: 5804 (sshd)
      Tasks: 2 (limit: 2282)
     Memory: 4.8M
     CGroup: /system.slice/ssh.service

Dec 24 16:14:03 DESKTOP-EJTS2G0 systemd[1]: ssh.service: Failed to delete controller cgroups /system.slice/ssh.service, igno>
Dec 24 16:14:03 DESKTOP-EJTS2G0 systemd[1]: Starting OpenBSD Secure Shell server...
Dec 24 16:14:03 DESKTOP-EJTS2G0 sshd[5804]: Server listening on 0.0.0.0 port 2233.
Dec 24 16:14:03 DESKTOP-EJTS2G0 sshd[5804]: Server listening on :: port 2233.
Dec 24 16:14:03 DESKTOP-EJTS2G0 systemd[1]: Started OpenBSD Secure Shell server.
```
