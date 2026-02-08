---
title: "ms powershell update from 7.5.3 to 7.5.4"
date: 2026-02-07
categories: 
  - "fsse"
---

if winget gives you an error

```
winget update PowerShell

A newer version was found, but the install technology is different from the current version installed. 
Please uninstall the package and install the newer version.
```

uninstall PS msi

open Control Panel\\Programs\\Programs and Features

select powershell right-click uninstall

open a CMD prompt

```
winget install --id Microsoft.PowerShell

```

check your install

```
$PSVersionTable

Name                           Value
---- -----
PSVersion                      7.5.4
PSEdition                      Core
GitCommitId                    7.5.4
OS                             Microsoft Windows 10.0.26200
Platform                       Win32NT
PSCompatibleVersions           {1.0, 2.0, 3.0, 4.0…}
PSRemotingProtocolVersion      2.3
SerializationVersion           1.1.0.1
WSManStackVersion              3.0
```
