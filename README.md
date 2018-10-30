### Ansible Roles: Users
Ansible role to provision users and add ssh keys.

[![Build Status](https://travis-ci.org/engonzal/ansible_role_users.svg?branch=master)](https://travis-ci.org/engonzal/ansible_role_users)

#### Role Variables
Create a list of users following this format:
```yaml
host_local_users:
- name: engonzal
  createhome: yes
  shell: "/bin/bash"
  groups: wheel
    pubkeys:
  - 'ssh-rsa myr4nd0mk3y engonzal@home'
- name: engontowel
```

#### Example Playbook
```yaml
    - hosts: servers
      vars:
        host_local_users:
        - name: engonshowel
        - name: engonzal
          createhome: yes
          shell: "/bin/bash"
          groups: wheel
          pubkeys:
            - 'ssh-rsa myr4nd0mk3y engonzal@home'
      roles:
        - { role: engonzal.users, tags: [ 'users'] }
```

#### License

BSD

#### Author

Noe Gonzalez - http://engonzal.com
