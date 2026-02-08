---
title: "ubuntu 18 &amp; vscode"
date: 2023-01-05
categories: 
  - "fsse"
---

ubuntu 18 & vscode

install gpg key and vscode repo

```
# wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg

# install packages.microsoft.gpg -D /etc/apt/keyrings/packages.microsoft.gpg

# echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" > /etc/apt/sources.list.d/vscode.list
```

install vscode dependancies & package

```
# aptitude update
# aptitude install apt-transport-https
# aptitude install code
```

run

```
$ code
```

but ignore any of these errors

```
To use Visual Studio Code with the Windows Subsystem for Linux, please install Visual Studio Code in Windows and uninstall the Linux version in WSL. You can then use the `code` command in a WSL terminal just as you would in a normal command prompt.

Do you want to continue anyway? [y/N]

To no longer see this prompt, start Visual Studio Code with the environment variable DONT_PROMPT_WSL_INSTALL defined.
```

refs

- https://code.visualstudio.com/docs/setup/linux

[![](https://fsse8info.wordpress.com/wp-content/uploads/2023/01/image-1.png?w=1024)](https://fsse8info.wordpress.com/wp-content/uploads/2023/01/image-1.png)

[![](https://fsse8info.wordpress.com/wp-content/uploads/2023/01/image-2.png?w=1024)](https://fsse8info.wordpress.com/wp-content/uploads/2023/01/image-2.png)
