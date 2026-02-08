---
title: "oracle linux selinux &amp; ubuntu apparmor"
date: 2022-12-24
categories: 
  - "fsse"
---

you can secure oracle linux with selinux & ubuntu with apparmor

disable / enable and get status of selinux

```
# sestatus
SELinux status:                 enabled
SELinuxfs mount:                /sys/fs/selinux
SELinux root directory:         /etc/selinux
Loaded policy name:             targeted
Current mode:                   enforcing
Mode from config file:          enforcing
Policy MLS status:              enabled
Policy deny_unknown status:     allowed
Memory protection checking:     actual (secure)
Max kernel policy version:      31

# getenforce
# setenforce
```

disable / enable and get status of apparmor

```
# aa-status
apparmor module is loaded.

42 profiles are loaded.

37 profiles are in enforce mode.
   /snap/snapd/17883/usr/lib/snapd/snap-confine

5 profiles are in complain mode.
   snap.oracle-cloud-agent.hook.install
   snap.oracle-cloud-agent.hook.post-refresh
   snap.oracle-cloud-agent.hook.remove
   snap.oracle-cloud-agent.oracle-cloud-agent
   snap.oracle-cloud-agent.oracle-cloud-agent-updater

3 processes are in complain mode.
   /snap/oracle-cloud-agent/48/agent (886) snap.oracle-cloud-agent.oracle-cloud-agent
   /snap/oracle-cloud-agent/48/plugins/gomon/gomon (2254) snap.oracle-cloud-agent.oracle-cloud-agent
   /snap/oracle-cloud-agent/48/updater/updater (885) snap.oracle-cloud-agent.oracle-cloud-agent-updater

# aa-enabled
# aa-enforce
# aa-teardown
```

_Make sure that you know what you are doing! Ubuntu offers AppArmor as an alternative to SELinux. While SELinux is available on Ubuntu, it is rather in an experimental stage and most likely will beak your system if set to `enforcing` mode. In case you must use SELinux, make sure to [disable AppArmor](https://linuxconfig.org/how-to-disable-apparmor-on-ubuntu-22-04-jammy-jellyfish-linux) first. Also set SELinux first to `permissive` mode and check your logs for potential issues before you enable `enforcing` mode._

refs

- https://www.golinuxcloud.com/disable-selinux/

- https://www.ibm.com/support/pages/how-disable-selinux

- https://linuxconfig.org/how-to-disable-enable-selinux-on-ubuntu-22-04-jammy-jellyfish-linux

- https://apparmor.net/

[![](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/image-6.png?w=1024)](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/image-6.png)
