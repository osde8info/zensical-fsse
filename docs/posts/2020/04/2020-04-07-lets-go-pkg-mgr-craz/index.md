---
title: "lets go pkg mgr crazy - dpkg, apt, aptitude, rpm, yum, dnf, tdnf #sysadmin #devops"
date: 2020-04-07
categories: 
  - "fsse"
tags: 
  - "deb"
  - "dnf"
  - "package-manager"
  - "rpm"
  - "tdnf"
  - "yum"
---

lets go pkg mgr crazy - dpkg, apt, aptitude, rpm, yum, dnf, microdnf, tdnf

dnf

- https://dnf.readthedocs.io/en/latest/

ibm red hat UBI images use

- microdnf

and vmware photonos introduces the 'latest' package manager on the block - tdnf

- https://vmware.github.io/photon/assets/files/html/1.0-2.0/tdnf.html
- https://vmware.github.io/photon/assets/files/html/3.0/photon\_admin/tdnf.html
- https://github.com/vmware/tdnf

and they have removed yum localinstall so you have to create your own repo to install an rpm

- https://vmware.github.io/photon/assets/files/html/3.0/photon\_admin/adding-a-new-repository.html
- https://github.com/vmware/tdnf/wiki#adding-a-new-repository
