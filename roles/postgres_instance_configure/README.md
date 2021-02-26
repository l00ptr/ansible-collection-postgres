Role Name
=========

A role to init and configure your postgres instances.

Requirements
------------

To use this role, you shouldinstall and configure postgres from the PGDG. For 
that you can check the other role from this collection.

Role Variables
--------------

    dalibo_postgresql_instances:
      - name: "test2"
        port: 5438
        state: present
        postgresql_version: 10
        pgdata_path: /var/lib/postgresql/10/test2
      - name: "test3"
        port: 5439
        state: present
        postgresql_version: 12
        pgdata_path: /var/lib/postgresql/12/test3
        custom_config_options:
          - listen: "*"

Dependencies
------------

You should use other role from this collection to install and configure postgres 
from the PGDG repo. For that you can use the following roles:
- configure_extra_repo
- postgres_install

Example Playbook
----------------
    - hosts: servers
      vars:
          dalibo_postgresql_instances:
          - name: "test2"
            port: 5438
            state: present
            postgresql_version: 10
            pgdata_path: /var/lib/postgresql/10/test2
      roles:
         - { role: dalibo.configure_extra_repo }
         - { role: dalibo.postgres_install }
         - { role: dalibo.postgres_instance_configure }

License
-------

MIT/BSD

Author Information
------------------

This role was first created in 2016 by Jeff Geerling then forked (mostly to split it into 
more atomic roles) by Julian Vanden Broeck (in 2020)
