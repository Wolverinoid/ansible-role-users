# Ansible Role: Users

An Ansible Role to manage users in OS Ubuntu / Debian.

## Role Variables

```yaml
- username: username
    name: FirstName LastName
    home_create: yes
    home_mode: "0750"
    home: /home/username
    shell: /bin/bash
    groups: ["sudo"]
    authorized_keys:
      - ssh-rsa 
    sudoers:
      - ALL=(ALL) NOPASSWD:ALL
```

## Example Playbook

```yaml
---
- hosts: server
  become: yes
  gather_facts: yes
  roles:
    - users
```

## Author Information

This role was created in 2016 by Aleksandr Ivanov (avic.ivanov@gmail.com).
