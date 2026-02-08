---
title: "dnf install mssql-tools does not create symlinks"
date: 2023-06-29
categories: 
  - "fsse"
---

dnf install mssql-server & dnf install mssql-tools do not create symlinks to /opt/mssql and /opt/mssql-tools18/bin/

to run mssql commands you need to create your own symlink to /\*/bin, add /opt/mssql-tools18/bin/ to your PATH or type in the full paths

mssql-conf

```
# /opt/mssql/bin/mssql-conf
```

sqlcmd

```
$ /opt/mssql-tools18/bin/sqlcmd
```

please upvote bug here

- https://feedback.azure.com/d365community/idea/2c8a766c-6e16-ee11-a81c-000d3adb7ffd
