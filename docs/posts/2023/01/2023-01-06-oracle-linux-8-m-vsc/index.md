---
title: "oracle linux 8 &amp; m$ vscode"
date: 2023-01-06
categories: 
  - "fsse"
---

oracle linux 8 & m$ vscode

set up m$ code yum repo

```

rpm --import https://packages.microsoft.com/keys/microsoft.asc

echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo
```

update repos and install code

```
dnf check-update

dnf install code

dnf install git
```

ignore any errors

```
To use Visual Studio Code with the Windows Subsystem for Linux, please install Visual Studio Code in Windows and uninstall the Linux version in WSL. You can then use the `code` command in a WSL terminal just as you would in a normal command prompt.

Do you want to continue anyway? [y/N]

To no longer see this prompt, start Visual Studio Code with the environment variable DONT_PROMPT_WSL_INSTALL defined.
```

refs

- https://code.visualstudio.com/docs/setup/linux

use

[![](https://fsse8info.wordpress.com/wp-content/uploads/2023/01/image-3.png?w=1024)](https://fsse8info.wordpress.com/wp-content/uploads/2023/01/image-3.png)
