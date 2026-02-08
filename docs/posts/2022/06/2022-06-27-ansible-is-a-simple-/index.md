---
title: "Ansible is a simple automation language that can perfectly describe an IT application infrastructure."
date: 2022-06-27
categories: 
  - "fsse"
---

Ansible is a simple automation language that can perfectly describe an IT application infrastructure.

- https://www.ansible.com/overview/it-automation?hsLang=en-us
- https://docs.ansible.com/
- https://docs.ansible.com/ansible-core/devel/getting\_started/get\_started\_inventory.html
- https://docs.ansible.com/ansible-core/devel/getting\_started/get\_started\_playbook.html

It uses ssh and yaml inventorys and playbooks

inv.yaml

```
myvms:
  hosts:
    vm01:
      ansible_host: 127.0.0.1
```

ansible

```
$ ansible myvms -m ping -i inv.yaml

vm01 | SUCCESS => {
    "ansible_facts": {
        "discovered_interpreter_python": "/usr/bin/python3"
    },
    "changed": false,
    "ping": "pong"
}
```

play.yaml

```
- name: my play
  hosts: myvms
  tasks:
   - name: ping hosts
     ansible.builtin.ping:
   - name: debug hi
     ansible.builtin.debug:
       msg: hi
```

ansible-playbook

```
$ ansible-playbook -i inv.yaml play.yaml

PLAY [my play] **************************************************************************************
TASK [Gathering Facts] **************************************************************************************ok: [vm01]

TASK [ping hosts] **************************************************************************************ok: [vm01]

TASK [debug hi] **************************************************************************************ok: [vm01] => {
    "msg": "hi"
}

PLAY RECAP **************************************************************************************vm01                       : ok=3    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   
```
