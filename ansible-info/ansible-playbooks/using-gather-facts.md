```
---
- hosts: all
  become: true
  gather_facts: true
  roles:
    - test
```
first we specify which playbook or role to use it for.  
```
- name: printing the ip addresses using gather_facts
  ansible.builtin.shell: |
    echo "{{ ansible_eth0.ipv4.address }} or {{ ansible_devices.sda }} ."
```
this magic variables are valued by ansibles gather_facts mechanism.

---
