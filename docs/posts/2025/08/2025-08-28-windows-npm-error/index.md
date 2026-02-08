---
title: "windows npm error"
date: 2025-08-28
categories: 
  - "fsse"
---

if windows npm errors or fails to run

```
npm : File C:\Program Files\nodejs\npm.ps1 cannot be loaded. The file C:\Program Files\nodejs\npm.ps1 is not digitally signed. You cannot run
this script on the current system. For more information about running scripts and setting execution policy, see about_Execution_Policies at
https:/go.microsoft.com/fwlink/?LinkID=135170.
```

open PowerShell as an Administrator

run \`Set-ExecutionPolicy RemoteSigned\`

then rerun your npm command
