# guacamole-docker

Ansible role for installing and running dockerized Apache Guacamole stack.

Deploys 3 containers:
* mariadb
* guacd
* guacamole

This role also inits the DB.

Default login:
```
guacadmin \ guacadmin
```

## Getting Started

### Prerequisites

* Ansible
* Docker

Docker can be deployed from one of many galaxy roles, such as [geerlingguy.docker](https://galaxy.ansible.com/geerlingguy/docker).


### Installing

```
$ ansible-galaxy install robrowan.guacamole_docker
```

## Use

### Role Variables

Defaults

```
mysql_database: guacamoledb
mysql_user: guacamole
mysql_password: guacamole9999
mysql_root_password: guacamole9999
```
Specify as extra or host vars to overwrite the defaults.

### Example playbook


```
- hosts: guacamole_hosts
  roles:
    - robrowan.guacamole_docker
  become: true
```

Include a docker role:
```
- hosts: guacamole_hosts
  roles:
    - geerlingguy.docker
    - robrowan.guacamole_docker
  become: true
```

## Authors

* **Rob Rowan** - [RobRowan](https://github.com/robrowan)

## Acknowledgements

Based on the official guacamole install guide. https://guacamole.apache.org/doc/gug/guacamole-docker.html 

## License

This project is licensed under the MIT License.

