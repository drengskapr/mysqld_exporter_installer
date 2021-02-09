mysqld_exporter installer
=========

Installs and sets up mysqld_exporter for Prometheus.

Requirements
------------

Debian 10

Role Variables
--------------

`exporter_version` version of mysql_exporter to be installed.
`mysqld_exporter_user` mysql user for mysql_exporter. Must exist in MySQL.
`mysqld_exporter_user_password` mysql user's password. Must match with user's password in MySQL.

Example Playbook
----------------

```
- name: Setting up mysqld_exporter
  hosts: all
  remote_user: root
  roles:
    - mysqld_exporter_installer
  vars:
    exporter_version: 0.12.1
    mysqld_exporter_user: user
    mysqld_exporter_user_password: password

```

License
-------

BSD

