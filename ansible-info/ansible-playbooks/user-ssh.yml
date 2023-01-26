---
- name: making sure ssh keys are available for user devops
  hosts: localhost
  gather_facts: no
  tasks:
    - name: ssh key generating
      ansible.builtin.user:
        name: devops
        generate_ssh_key: yes
        ssh_key_file: .ssh/id_rsa
        state: present
- name: making sure the user devops is available
  hosts: < inventory group name >
  gather_facts: no
  tasks:
    - name: user creation and giving sudo permissions
      ansible.builtin.user:
        name: devops
        state: present
        groups: sudo
        append: yes
    - name: copying ssh public key
      ansible.posix.authorized_key:
        user: devops
        state: present
        key: "{{ lookup('file', '/home/devops/.ssh/id_rsa.pub') }}"
