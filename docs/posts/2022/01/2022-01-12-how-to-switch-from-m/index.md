---
title: "how to switch from ms edge dev #browser to ms edge prod #browser on @xubuntu #gnu/#linux"
date: 2022-01-12
categories: 
  - "fsse"
---

how to switch from ms edge dev #browser to ms edge prod #browser on @xubuntu #gnu/#linux

uninstall ms edge dev

```
# aptitude uninstall edge-dev
```

remove ms repo

```
# apt-add-repository --remove "https://packages.microsoft.com/ubuntu/18.04/prod"
```

```
Ign https://packages.microsoft.com/ubuntu/18.04/prod focal InRelease                                                                                    
Err https://packages.microsoft.com/ubuntu/18.04/prod focal Release 
```

alternatively vi /etc/apt/sources.list

run apt update you should no longer get any apt repo errors such as

then install ms edge (prod) for linux

- https://www.microsoft.com/en-us/edge

then dpkg install microsoft-edge-stable.deb

refs

- https://www.theverge.com/2021/11/2/22759123/microsoft-edge-linux-stable-channel
- https://vitux.com/
- https://vitux.com/how-to-add-ppa-repositories-in-debian/
