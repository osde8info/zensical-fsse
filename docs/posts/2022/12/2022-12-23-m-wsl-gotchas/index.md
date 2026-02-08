---
title: "m$ wsl gotchas"
date: 2022-12-23
categories: 
  - "fsse"
---

# windows versions

only some windows version support microsoft store wsl

Windows version 10.0 21H2 19044.2251 does not support the packaged version of Windows Subsystem for Linux.

so if you have

- Windows 10 Home/Ent/Pro 21H2 19044

upgrade to

- Windows 10 Home/Ent/Pro 22H2 19045

For information please visit https://aka.ms/wslinstall

# wsl versions

wsl --version FAILS if you have WSL 1

# wsl version command

wsl --version still SAYS 1 even if you have 2

```
wsl --version
WSL version: 1.0.3.0
Kernel version: 5.15.79.1
WSLg version: 1.0.47
MSRDC version: 1.2.3575
Direct3D version: 1.606.4
DXCore version: 10.0.25131.1002-220531-1700.rs-onecore-base2-hyp
Windows version: 10.0.19045.2364
```

# wsl 1 & 2 -l -o list different distros

## WSL 1

```
wsl -l -o

The following is a list of valid distributions that can be installed.
Install using 'wsl.exe --install <Distro>'.

NAME            FRIENDLY NAME
Ubuntu          Ubuntu
Debian          Debian GNU/Linux
kali-linux      Kali Linux Rolling
openSUSE-42     openSUSE Leap 42
SLES-12         SUSE Linux Enterprise Server v12
Ubuntu-16.04    Ubuntu 16.04 LTS
Ubuntu-18.04    Ubuntu 18.04 LTS
Ubuntu-20.04    Ubuntu 20.04 LTS
```

## WSL 2

```
wsl -l -o
NAME               FRIENDLY NAME
Ubuntu             Ubuntu
Debian             Debian GNU/Linux
kali-linux         Kali Linux Rolling
SLES-12            SUSE Linux Enterprise Server v12
SLES-15            SUSE Linux Enterprise Server v15
Ubuntu-18.04       Ubuntu 18.04 LTS
Ubuntu-20.04       Ubuntu 20.04 LTS
OracleLinux_8_5    Oracle Linux 8.5
OracleLinux_7_9    Oracle Linux 7.9
```

note OPENSUSE is missing from V2 list AND the list is different again to distros available on the microsoft store !

# wsl and VPNs !

wsl autogenerates /etc/resolv.conf incorrectly if you are using a VPN on your host (override with generateResolvConf=false)

- https://learn.microsoft.com/en-us/windows/wsl/wsl-config
- https://gist.github.com/machuu/7663aa653828d81efbc2aaad6e3b1431
