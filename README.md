Role Name
=========

A brief description of the role goes here.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

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
