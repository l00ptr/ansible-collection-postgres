Role Name
=========

Role to download, install and configure pg_back
A brief description of the role goes here.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

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
Path where we should store our backups

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

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
