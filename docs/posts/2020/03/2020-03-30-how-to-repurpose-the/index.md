---
title: "how to repurpose the @VMware #photonos @foldingathome #VM to run the newer @infrabuilder @foldingathome @docker image @lamw #beatthevirus #solvethevirus #iamoneinamillion"
date: 2020-03-30
categories: 
  - "fsse"
tags: 
  - "docker"
  - "folding"
  - "foldingathome"
  - "photon-os"
  - "vmware"
---

how to repurpose the @VMware #photonos @foldingathome F@H 7.4.4 (2014) #VM to run the newer @infrabuilder foldingathome F@H 7.5.1 (2018) @docker image

Run Oracle VirtualBox and start the VMware Photon OS FAH VM

- https://flings.vmware.com/vmware-appliance-for-folding-home

Hack root password and login as root

Enable and start docker

```
# systemctl enable docker
# systemctl start docker
```

Create a user and add to docker group

```
# useradd -m myuser
# usermod -aG docker myuser
```

Logout

Login as user

Test docker

```
$ docker run hello-world
```

Pull infrabuilder/foldingathome image

```
$ docker pull infrabuilder/foldingathome
```

Run infrabuilder/foldingathome

```
$ docker docker run -d \
-e USER="" -e TEAM=236450 -e PASSKEY="" -e CPUS=2 \
--name ff infrabuilder/foldingathome
```

See also a another way to achieve this hack by @lamw

- https://www.virtuallyghetto.com/2020/03/how-to-manually-install-folding-home-on-vmware-photon-os.html
