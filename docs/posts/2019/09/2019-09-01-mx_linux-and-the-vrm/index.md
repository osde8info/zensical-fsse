---
title: "MX_Linux and the vrms free libre open source detection command"
date: 2019-09-01
categories: 
  - "fsse"
tags: 
  - "free-libre"
  - "mx_linux"
  - "open-source"
  - "rms"
---

MX Linux https://mxlinux.org/ is NON-FREE here is their reasoning:

_Non-free software MX Linux is fundamentally user-oriented, so includes a certain amount of non-free software to assure that the system works out of the box as much as possible._

_Our rationale: it is much easier for advanced users to remove these drivers than it is for regular users to install them. And it's particularly difficult to install a driver for a network card without Internet access!_

BUT the user can see a list by opening a console or terminal and typing:

```
$ vrms
```

Examples:

• The “wl” driver (broadcom-sta) and non-free firmware with proprietary components.

• A dedicated tool for installing Nvidia graphic drivers.

• Adobe Flash Player (distributed by permission).

```
$ vrms
Non-free packages installed on vboxmx

adobe-flash-properties-gtk GTK+ control panel for Adobe Flash Player plugin
adobe-flashplugin Adobe Flash Player plugin
amd64-microcode Processor microcode firmware for AMD CPUs
atmel-firmware Firmware for Atmel at76c50x wireless networking chips.
bluez-firmware Firmware for Bluetooth devices
broadcom-sta-dkms dkms source for the Broadcom STA Wireless driver
firmware-amd-graphics Binary firmware for AMD/ATI graphics chips
firmware-atheros Binary firmware for Qualcomm Atheros wireless cards
Reason: Modifications problematic

Contrib packages installed on vboxmx

b43-fwcutter utility for extracting Broadcom 43xx firmware
firmware-b43-installer firmware installer for the b43 driver
firmware-b43legacy-installer firmware installer for the b43legacy driver
iucode-tool Intel processor microcode tool
ttf-mscorefonts-installer Installer for Microsoft TrueType core fonts

Contrib packages with status other than installed on vboxmx

virtualbox-guest-utils ( dei) x86 virtualization solution - non-X11 guest ut
virtualbox-guest-x11 ( dei) x86 virtualization solution - X11 guest utilit

26 non-free packages, 1.3% of 1936 installed packages.
7 contrib packages, 0.4% of 1936 installed packages.

```

vrms "virtual richard m stallman" has a great manpage including

```
the opinions of Richard M Stallman and the Debian project have 
diverged since this program was originally written.  In such cases,
this  program  follows  the  definition of freedom embodied in 
the Debian Free Software Guidelines.

```
