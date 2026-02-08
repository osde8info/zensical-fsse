---
title: "wireguard - yet another open source vpn"
date: 2019-08-23
categories: 
  - "fsse"
tags: 
  - "security"
  - "vpn"
---

wireguard - yet another open source vpn

- https://www.wireguard.com/
- https://git.zx2c4.com/WireGuard/

_WireGuard securely encapsulates IP packets over UDP. You add a WireGuard interface, configure it with your private key and your peers' public keys, and then you send packets across it. All issues of key distribution and pushed configurations are out of scope of WireGuard; these are issues much better left for other layers, lest we end up with the bloat of IKE or OpenVPN. In contrast, it more mimics the model of SSH and Mosh; both parties have each other's public keys, and then they're simply able to begin exchanging packets through the interface._
