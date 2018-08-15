ansible_role_users
=========

Ansible role to provision users and add ssh keys.

Role Variables
--------------

Create a list of users following this format:
```
host_local_users:
- name: user1
  createhome: yes
  groups: wheel
- name: user2

```

Example Playbook
----------------

    - hosts: servers
      vars:
        host_local_users:
        - name: user1
          createhome: yes
          groups: wheel
        - name: user2
      roles:
        - { role: engonzal.users, tags: [ 'users'] }

License
-------

BSD

Author Information
------------------

Noe Gonzalez - http://engonzal.com
