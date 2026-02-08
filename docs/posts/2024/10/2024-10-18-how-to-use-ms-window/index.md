---
title: "how to use ms windows remote desktop with a outlook login"
date: 2024-10-18
categories: 
  - "fsse"
---

how to use ms windows remote desktop with a outlook login

first make sure remote pc has cached outlook password by running

```
runas /u:MicrosoftAccount\your-email-address winver
```

and entering outlook password BEFORE running the Remote Desktop Connection app

run Remote Desktop goto Advanced and click "Use a web account" then connect as usual

[![](https://fsse8info.wordpress.com/wp-content/uploads/2024/10/2024-10-18.png?w=1024)](https://fsse8info.wordpress.com/wp-content/uploads/2024/10/2024-10-18.png)

see also

[https://learn.microsoft.com/en-us/windows-server/remote/remote-desktop-services/clients/remote-desktop-connection-single-sign-on?form=MG0AV3](https://learn.microsoft.com/en-us/windows-server/remote/remote-desktop-services/clients/remote-desktop-connection-single-sign-on?form=MG0AV3)
