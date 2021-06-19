Role Name
=========

Role to download, install and configure pg_back. This role allows to create a 
config file  and add a cron for each instance.

Requirements
------------

To use this role, you should install and configure postgres from the PGDG. For 
that you can check the other role from this collection.


Role Variables
--------------

    postgresql_user: postgres
User running PostgreSQL server

    postgresql_group: postgres
Group of the PostgreSQL server

    postgresql_default_unix_socket_directories: /var/run/postgresql/
Path of the unix socket directories associated to your PostgreSQL configuration

    postgresql_pg_back_version : v2.0.1
Version of pg_back we want to install 

    postgresql_pg_back_bin_src_url: https://github.com/orgrim/pg_back/releases/download/{{ postgresql_pg_back_version }}/pg_back-{{ postgresql_pg_back_version }}-linux-amd64
URL of the pg_back binary

    postgresql_pg_back_bin_dest_path: /usr/local/bin/pg_back
Where we should copy the pg_back binary

    postgresql_pg_back_default_backup_directory: /var/backups/postgresql/
Path where we should store our backups. If this directory doesn't exist this
role will create it.

    postgresql_pg_back_default_parallel_backup_jobs: 1
Number of parallel jobs to dumps (-j option of pg_dump)

    postgresql_pg_back_default_purge_older_than: 30
Purge dumps older than this number of days.

Dependencies
------------
You should use other role from this collection to install and configure 
postgres from the PGDG repo. 

For that you can use the following roles:
- configure_extra_repo
- postgres_install


For more information please read the readme of this collection

Example Playbook
----------------

You can use this role with some other comapnions (configure_pgdg_repo, 
postgresql_install, configure__instance, etc) to deploy your PostgreSQL 
instance.

      - hosts: servers
        vars:
          postgresql_instances:
          - name: "test2"
            port: 5438
            state: present
            postgresql_version: 10
            pgdata_path: /var/lib/postgresql/10/test2
            pg_back_conf:
              schedule_hour: 2
              schedule_minute: 30
        roles:
          - postgres.postgres.configure_pgdg_repo
          - postgres.postgres.postgresql_install
          - postgres.postgres.configure_instances
          - postgres.postgres.configure_pg_back

License
-------
BSD

Author Information
------------------

This role was first created in 2016 by Jeff Geerling then forked (mostly to 
split it into more atomic roles) by Julian Vanden Broeck (in 2020)

