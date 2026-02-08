---
title: "vscode wsl git-credential-manager-core was renamed to git-credential-manager"
date: 2022-12-25
categories: 
  - "fsse"
---

if you are getting the error

```
warning: git-credential-manager-core was renamed to git-credential-manager
warning: see https://aka.ms/gcm/rename for more information
```

you need to change your git config

```
git config --show-origin --get-all credential.helper
```

refs

https://github.com/GitCredentialManager/git-credential-manager/blob/main/docs/rename.md
