# Ansible Role: PostgreSQL

Installs PostgreSQL server on RHEL/CentOS or Debian/Ubuntu servers.

## Requirements

This role is part of a collection, it requires the PGDG repo to work correctly. We recommend the 
configure_extra_repo role from our collection to setup and configure the PGDG repo.

    - hosts: database
      roles:
        - role: postgresql
          become: yes

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    postgresql_locales:
      - 'en_US.UTF-8'

List of locales this role will generate on Debian based system

    postgresql_packages 

List of package this role is configured to install

## Dependencies

None.

## Example Playbook

    - hosts: database
      become: yes
      tasks:
        - import_role:
            name: l00ptr.postgres.postgres_install


## License

MIT / BSD

## Author Information

This role was first created in 2016 by [Jeff Geerling](https://www.jeffgeerling.com/) then forked (mostly to 
split it into more atomic roles) by Julian Vanden Broeck (in 2020)
