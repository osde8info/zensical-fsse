---
title: "IBM Red Hat RHEL Developer 7 is even more locked down than Windows 10 #mktg #fail"
date: 2020-04-03
categories: 
  - "fsse"
tags: 
  - "ibm"
  - "red-hat"
  - "subscription"
  - "updates"
  - "yum"
---

IBM Red Hat RHEL Developer 7 is even more locked down than Windows 10 since you cannot even run YUM in a clean install of RHEL 7 without registering your PC with IBM Red Hat.

```
$ yum update
Loaded plugins: langpacks, product-id, search-disabled-repos, 
subscription-manager

This system is not registered with an entitlement server. 
You can use subscription-manager to register.

There are no enabled repos.
 Run "yum repolist all" to see the repos you have.
 To enable Red Hat Subscription Management repositories:
     subscription-manager repos --enable 
 To enable custom repositories:
     yum-config-manager --enable
```

Red Hat Update Subscription procedures

- https://access.redhat.com/documentation/en-us/red\_hat\_subscription\_management/1/html/introduction\_to\_red\_hat\_subscription\_management\_workflows/index
- https://access.redhat.com/documentation/en-us/red\_hat\_subscription\_management/1/html/quick\_registration\_for\_rhel/registering-cmd

![Screenshot from 2020-04-03 12-17-24.png](https://fsse8info.wordpress.com/wp-content/uploads/2020/04/screenshot-from-2020-04-03-12-17-24.png)
