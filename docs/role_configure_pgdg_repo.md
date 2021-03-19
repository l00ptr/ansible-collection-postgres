configure_pgdg_repo
===================
This role allows to configure the PGDG repository on CentOS and Debian.

Role Variables
--------------
We use internal variables to define how to install the PGDG repo, you can (even 
if it's not recommended) extend / override those variable if you need to 
install some repo.

Example Playbook
----------------
    - hosts: all 
      roles:
         - { role: configure_extra_repo }

License
-------
MIT/BSD

Author Information
------------------
This role was first created in 2016 by Jeff Geerling then forked (mostly to 
split it into more atomic roles) by Julian Vanden Broeck (in 2020)
