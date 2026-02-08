---
title: "how to get @redhat @centos @oracle #gnu/linux to 8 run @microsoft #edge #dev #browser 88"
date: 2020-11-27
categories: 
  - "fsse"
---

add microsoft edge repo

```
# rpm --import https://packages.microsoft.com/keys/microsoft.asc
# dnf config-manager --add-repo https://packages.microsoft.com/yumrepos/edge
```

install microsoft edge dev

```
# dnf install microsoft-edge-dev
```

refs

- [https://www.tecmint.com/install-microsoft-edge-browser-in-linux/](https://www.tecmint.com/install-microsoft-edge-browser-in-linux/)
- [https://www.debugpoint.com/2020/10/how-to-install-edge-ubuntu-linux/](https://www.debugpoint.com/2020/10/how-to-install-edge-ubuntu-linux/)
- [https://www.redhat.com/sysadmin/add-yum-repository](https://www.redhat.com/sysadmin/add-yum-repository)
- [https://linoxide.com/how-tos/add-repositories-yum/](https://linoxide.com/how-tos/add-repositories-yum/)
- [https://access.redhat.com/documentation/en-us/red\_hat\_enterprise\_linux/6/html/deployment\_guide/sec-managing\_yum\_repositories](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/6/html/deployment_guide/sec-managing_yum_repositories)
- [https://packages.microsoft.com/yumrepos/](https://packages.microsoft.com/yumrepos/)
- [https://packages.microsoft.com/yumrepos/edge](https://packages.microsoft.com/yumrepos/edge)

screenshots

[![](https://fsse8info.wordpress.com/wp-content/uploads/2020/11/virtualbox_orac8_27_11_2020_19_34_10.png?w=1024)](https://fsse8info.wordpress.com/wp-content/uploads/2020/11/virtualbox_orac8_27_11_2020_19_34_10.png)

[![](https://fsse8info.wordpress.com/wp-content/uploads/2020/11/virtualbox_orac8_27_11_2020_20_05_14.png?w=1024)](https://fsse8info.wordpress.com/wp-content/uploads/2020/11/virtualbox_orac8_27_11_2020_20_05_14.png)
