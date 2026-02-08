---
title: "microsoft wsl 2 oracle linux 8 cockpit podman firewalld iptables &amp; nftables error"
date: 2022-12-22
categories: 
  - "fsse"
---

if you are running microsoft wsl 2 oracle linux 8 with cockpit & podman you might get the following firewalld iptables & nftables errors when you try to start a podman container

# firewalld errors

firewalld

```
ERROR: COMMAND_FAILED: 'python-nftables' failed: internal:0:0-0: Error: Could not process rule: No such file or directory
internal:0:0-0: Error: Could not process rule: No such file or directory
internal:0:0-0: Error: Could not process rule: No such file or directory
internal:0:0-0: Error: Could not process rule: No such file or directory

ERROR: 'python-nftables' failed: internal:0:0-0: Error: Could not process rule: No such file or directory
internal:0:0-0: Error: Could not process rule: No such file or directory
internal:0:0-0: Error: Could not process rule: No such file or directory
```

# firewalld warnings

```
WARNING: AllowZoneDrifting is enabled. This is considered an insecure configuration option. It will be removed in a future release. Please consider disabling it now.
```

# workaround

switch from nftables to iptables and disable drifting

vi /etc/firewalld/firewalld.conf

```
...
# FirewallBackend
# Selects the firewall backend implementation.
# Choices are:
#       - nftables (default)
#       - iptables (iptables, ip6tables, ebtables and ipset)
FirewallBackend=iptables
...
# AllowZoneDrifting
# Older versions of firewalld had undocumented behavior known as "zone
# drifting". This allowed packets to ingress multiple zones - this is a
# violation of zone based firewalls. However, some users rely on this behavior
# to have a "catch-all" zone, e.g. the default zone. You can enable this if you
# desire such behavior. It's disabled by default for security reasons.
# Note: If "yes" packets will only drift from source based zones to interface
# based zones (including the default zone). Packets never drift from interface
# based zones to other interfaces based zones (including the default zone).
# Possible values; "yes", "no". Defaults to "yes".
AllowZoneDrifting=no
```

# firewalld restart

```
systemctl restart firewalld.service
```

# podman network check

```
# podman network inspect podman
[
     {
          "name": "podman",
          "id": "2f259bab93aaaaa2542ba43ef33eb990d0999ee1b9924b557b7be53c0b7a1bb9",
          "driver": "bridge",
          "network_interface": "cni-podman0",
          "created": "2022-12-22T10:01:25.529850819Z",
          "subnets": [
               {
                    "subnet": "10.88.0.0/16",
                    "gateway": "10.88.0.1"
               }
          ],
          "ipv6_enabled": false,
          "internal": false,
          "dns_enabled": false,
          "ipam_options": {
               "driver": "host-local"
          }
     }
]
```

# refs

- https://github.com/firewalld/firewalld/issues/742
    
- https://github.com/firewalld/firewalld/issues/891
    
- https://bugzilla.redhat.com/show\_bug.cgi?id=1817205
    
- https://bugzilla.redhat.com/show\_bug.cgi?id=1836571
