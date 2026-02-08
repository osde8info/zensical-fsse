---
title: "how to get @redhat @fedora @centos @oracle #gnu/linux 7 &amp; 8 to run @microsoft #sqlserver 2019 #client #tools #dba #devops #sysadmin"
date: 2020-11-27
categories: 
  - "fsse"
---

how to get @redhat @fedora @centos @oracle #gnu/linux 7 & 8 to run @microsoft #sqlserver 2019 #client #tools #dba #devops #sysadmin

@redhat @fedora @centos @oracle enterprise unbreakable #gnu/linux 7

```
# rpm --import https://packages.microsoft.com/keys/microsoft.asc

# yum-config-manager --add-repo https://packages.microsoft.com/yumrepos/microsoft-rhel7.4-prod/

# yum update
# yum install mssql-cli
# yum install mssql-tools

# yum-config-manager --add-repo https://packages.microsoft.com/yumrepos/mssql-server-2019-rhel7/
```

@redhat @fedora @centos @oracle enterprise unbreakable #gnu/linux 8

```
# rpm --import https://packages.microsoft.com/keys/microsoft.asc

# dnf config-manager --add-repo https://packages.microsoft.com/yumrepos/microsoft-rhel8.0-prod/

# dnf update
# dnf install mssql-tools

# dnf config-manager --add-repo https://packages.microsoft.com/yumrepos/mssql-server-2019-rhel8/
```

refs

- https://packages.microsoft.com/yumrepos/
- https://packages.microsoft.com/yumrepos/microsoft-rhel7.4-prod/
- https://packages.microsoft.com/yumrepos/mssql-server-2019-rhel7/
- https://packages.microsoft.com/yumrepos/microsoft-rhel8.0-prod/
- https://packages.microsoft.com/yumrepos/mssql-server-2019-rhel8/
