# robrowan.guacamole-docker

Ansible role for installing and running dockerized guacamole. Based on the official guacamole install guide. https://guacamole.apache.org/doc/gug/guacamole-docker.html 

## Getting Started

### Prerequisites

* Ansible
* Docker

### Installing

A step by step series of examples that tell you how to get a development env running

Say what the step will be

```
$ ansible-galaxy install robrowan.guacamole-docker
```

## Use

Explain how to run the automated tests for this system

### Role Variables

Defaults

```
mysql_database: guacamoledb
mysql_user: guacamole
mysql_password: guacamole9999
mysql_root_password: guacamole9999
```
Specify each as extra vars or host vars to set credentials to non-defaults (recommended).


### Example playbook

Explain what these tests test and why

```
- hosts: guacamole_hosts
  roles:
    - robrowan.guacamole-docker
  become: true
```

Include a docker role:
```
- hosts: guacamole_hosts
  roles:
    - geerlingguy.docker
    - robrowan.guacamole-docker
  become: true
```

## Authors

* **Rob Rowan** - [RobRowan](https://github.com/robrowan)

## License

This project is licensed under the MIT License.

