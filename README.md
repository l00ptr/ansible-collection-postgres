# Ansible Collection - l00ptr.postgres

## Description
This collection provides a few roles to install, configure and manage your postgres 
instances.

We try to keep variable name consistent between the roles composing this collection.

This collection is under develoment and currently only available for Debian 9 and 10.

## Tested with Ansible

2.10

## Included content
### Roles

- [configure_pgdg_repo](docs/role_configure_pgdg_repo.md) (Allow to install the PGDG repo)
- [postgresql_install](docs/role_postgresql_install.md) (Allow to install the postgres packages)
- [configure_instances](docs/role_configure_instances.md) (Allow to init and configure our postgres instances)

## Using this collection

Please refer to the examples in the [examples.md](docs/examples.md) you can also read the playbooks available on the docs directory.

See [Ansible Using collections](https://docs.ansible.com/ansible/latest/user_guide/collections_using.html) for more details.

## Contributing to this collection

See the [contributor guideline](CONTRIBUTING.md).

## Roadmap
- Imrpove tests
- Add support for more operating systems
- Add role to configure and manage PITR backup
- Add role to configure and manage replication
- Add role to configure and manage pg_back 

## More information

General information:

- [Ansible Collection overview](https://github.com/ansible-collections/overview)
- [Ansible User guide](https://docs.ansible.com/ansible/latest/user_guide/index.html)
- [Ansible Developer guide](https://docs.ansible.com/ansible/latest/dev_guide/index.html)
- [Ansible Collections Checklist](https://github.com/ansible-collections/overview/blob/master/collection_requirements.rst)
- [Ansible Community code of conduct](https://docs.ansible.com/ansible/latest/community/code_of_conduct.html)
- [The Bullhorn (the Ansible Contributor newsletter)](https://us19.campaign-archive.com/home/?u=56d874e027110e35dea0e03c1&id=d6635f5420)
- [Changes impacting Contributors](https://github.com/ansible-collections/overview/issues/45)

## Licensing
Released under MIT License

Copyright (c) 2020 Julian Vanden Broeck.


Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"),
to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense,
and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, 
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

