---
title: "m$ wsl &amp; m$ vscode remote dev extension pack"
date: 2022-12-21
categories: 
  - "fsse"
---

WSL & VSCODE remote development extension pack !

_The VSCODE remote development_ _extension splits VS Code into a “client-server” architecture, with the client (the user interface) running on your Windows machine and the server (your code, Git, plugins, etc) running "remotely" in your WSL distribution._

so you will end up installing your vscode extensions twice ie locally and in your wsl vm

```
$ ls -l .vscode-server/extensions/
total 44
drwxr-xr-x  5 cdarra cdarra 4096 Dec 21 16:42 esbenp.prettier-vscode-9.10.3
drwxr-xr-x  7 cdarra cdarra 4096 Dec 21 16:37 ms-python.isort-2022.8.0
drwxr-xr-x 10 cdarra cdarra 4096 Dec 21 16:37 ms-python.python-2022.20.1
drwxr-xr-x  4 cdarra cdarra 4096 Dec 21 16:37 ms-python.vscode-pylance-2022.12.20
drwxr-xr-x 10 cdarra cdarra 4096 Dec 21 16:37 ms-toolsai.jupyter-2022.11.1003412109
drwxr-xr-x  2 cdarra cdarra 4096 Dec 21 16:36 ms-toolsai.jupyter-keymap-1.0.0
drwxr-xr-x  4 cdarra cdarra 4096 Dec 21 16:36 ms-toolsai.jupyter-renderers-1.0.12
drwxr-xr-x  6 cdarra cdarra 4096 Dec 21 16:36 ms-toolsai.vscode-jupyter-cell-tags-0.1.6
drwxr-xr-x  5 cdarra cdarra 4096 Dec 21 16:36 ms-toolsai.vscode-jupyter-slideshow-0.1.5
drwxr-xr-x  6 cdarra cdarra 4096 Dec 21 16:42 redhat.vscode-yaml-1.10.1
drwxr-xr-x  7 cdarra cdarra 4096 Dec 21 16:42 yzhang.markdown-all-in-one-3.5.0
```

- https://learn.microsoft.com/en-us/windows/wsl/tutorials/wsl-vscode#extensions-inside-of-vs-code-wsl

[![](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/image.png?w=1024)](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/image.png)
