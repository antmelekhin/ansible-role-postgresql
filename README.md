PostgreSQL
==========

An Ansible role to install and configure [PostgreSQL](https://www.postgresql.org/about/) server.

Requirements
------------

- Supported version of Ansible: 2.12 and higher. Systems with Python versions below than 3.7 are not compatible with ansible-core 2.17 (see [ansible/ansible#83357](https://github.com/ansible/ansible/issues/83357#issuecomment-2150254754)).
- Supported platforms:
  - Almalinux
    - 8
    - 9
  - Debian
    - 11
    - 12
  - Rockylinux
    - 8
    - 9
  - Ubuntu
    - 22.04
    - 24.04

Role Variables
--------------

All variables that can be overridden are stored in the [defaults/main.yml](https://github.com/antmelekhin/ansible-role-postgresql/blob/main/defaults/main.yml) file.
Please refer to the [meta/argument_specs.yml](https://github.com/antmelekhin/ansible-role-postgresql/blob/main/meta/argument_specs.yml) file for a description of the available variables.
Similarly, descriptions and defaults for preset variables can be found in the [vars/main.yml](https://github.com/antmelekhin/ansible-role-postgresql/blob/main/vars/main.yml) file.

Dependencies
------------

When using Ansible core, you will also need to install the following Ansible collections:

```yaml
---
collections:
  - name: community.postgresql
```

Example Playbook
----------------

Install and configure the `PostgreSQL`:

```yaml
---
- name: 'Setup the PostgreSQL server'
  hosts: all

  roles:
    - role: antmelekhin.postgresql
```

License
-------

MIT

Author Information
------------------

Melekhin Anton.
