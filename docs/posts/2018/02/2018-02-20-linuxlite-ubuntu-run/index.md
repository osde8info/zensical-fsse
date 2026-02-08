---
title: "linuxlite ubuntu run synaptic on remote host"
date: 2018-02-20
categories: 
  - "fsse"
tags: 
  - "ssh"
  - "synaptic"
  - "x"
---

linuxlite ubuntu run synaptic on remote host

this fails

```
$ ssh remotehost
$ synaptic
```

with errors

```
Failed to connect to Mir: Failed to connect to server socket: 
No such file or directory
Unable to init server: Could not connect: Connection refused
```

 

this fails

```
$ ssh -X remotehost
$ su -
# synaptic
```

with errors

```
X11 connection rejected because of wrong authentication.
Failed to connect to Mir: Failed to connect to server socket: 
No such file or directory
Unable to init server: Could not connect: Connection refused

(synaptic:1659): Gtk-WARNING **: cannot open display: localhost:11.0
```

 

this works

```
$ ssh -X remotehost
$ sudo synaptic
```

BUT with warnings

```
** (synaptic:1403): WARNING **: 
Couldn't connect to accessibility bus: 
Failed to connect to socket /tmp/dbus-WJ1IDwyNzq: 
Connection refused
```
