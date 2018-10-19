# Ansible proxy_client role

This is an [Ansible](http://www.ansible.com) role which configures proxy client environment variables.

## Requirements

[Ansible 2.7+](http://docs.ansible.com/ansible/latest/intro_installation.html)

## Variables

A list of all the default variables for this role is available in `defaults/main.yml`.

## Dependencies

[amtega.environment](https://galaxy.ansible.com/amtega/environment)

## Usage

This is an example playbook:

```yaml
---

- hosts: all
  roles:
    - role: amtega.proxy_client
      proxy_client_http_proxy: http://acme.local
      proxy_client_https_proxy: https://acme.local
      proxy_client_no_proxy:
        - https://acme2.local
```

## Testing

Tests are based on docker containers. You can setup docker engine quickly using the playbook `files/setup.yml` available in the role [amtega.docker_engine](https://galaxy.ansible.com/amtega/docker_engine).

Once you have docker, you can run the tests with the following commands:

```shell
$ cd amtega.proxy_client/tests
$ ansible-playbook main.yml
```

## License

Copyright (C) 2018 AMTEGA - Xunta de Galicia

This role is free software: you can redistribute it and/or modify it under the terms of:

GNU General Public License version 3, or (at your option) any later version; or the European Union Public License, either Version 1.2 or – as soon they will be approved by the European Commission ­subsequent versions of the EUPL.

This role is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details or European Union Public License for more details.

## Author Information

- Juan Antonio Valiño García.
