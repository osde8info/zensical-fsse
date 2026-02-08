---
title: "ms windows powershell 7.5.2 install / upgrade"
date: 2025-09-04
categories: 
  - "fsse"
---

if you previously installed via msi to avoid a "technology error" you will need to uninstall

```
winget uninstall --id Microsoft.PowerShell
```

then

```
winget install --id Microsoft.PowerShell
```

see

[https://learn.microsoft.com/en-gb/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.5](https://learn.microsoft.com/en-gb/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.5)
