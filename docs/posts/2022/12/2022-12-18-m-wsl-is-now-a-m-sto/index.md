---
title: "M$ WSL is now a M$ Store App and supports X11 GUIs with WSLg"
date: 2022-12-18
categories: 
  - "fsse"
---

M$ WSL (that now includes WSLg) is now available as a M$ Store App and supports X11 GUI apps.

But first turn the following Windows features on

- Virtual Machine Platform

- Windows Subsystem for LInux

then get WSL from the M$ Store

[![](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/winfeat.png?w=621)](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/winfeat.png)

Then get a a distro of your choice (Oracle, SUSE, Ubuntu etc)

```
C:> wsl --install OracleLinux_8_5
```

but watch out for a couple of errors !

```
Error code: Wsl/WSL_E_DEFAULT_DISTRO_NOT_FOUND

Installing, this may take a few minutes...
WslRegisterDistribution failed with error: 0x80370114
Error: 0x80370114 The operation could not be started because a required feature is not installed.

Press any key to continue...
```

[![](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/wsl.png?w=1024)](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/wsl.png)

WSLg _is available both as part of the Windows 11 WSL builtin support as well as through the [Windows Subsystem for Linux from the Microsoft Store](https://aka.ms/wslstorepage). It is highly recommended to use the Microsoft Store version of WSL, which supports both Windows 10 and Windows 11, and contains the most up to date version of WSL and WSLg_

WSLg is short for _Windows Subsystem for Linux GUI_ and the purpose of the project is to enable support for running Linux GUI applications (X11 and Wayland) on Windows in a fully integrated desktop experience.

- https://learn.microsoft.com/en-gb/windows/wsl/compare-versions#whats-new-in-wsl-2

- https://devblogs.microsoft.com/commandline/the-windows-subsystem-for-linux-in-the-microsoft-store-is-now-generally-available-on-windows-10-and-11/

- https://learn.microsoft.com/en-us/windows/wsl/about

- https://github.com/microsoft/WSL

- https://github.com/microsoft/WSLg
