## Features
Install Pleasanter for AlmaLinux 8

## Require
Ansible on AlmaLinux 8

## Install

Change OS security setting
* disable SELinux
* open 80 port on firewalld

Set the following variables in **plesanter_server.yml**
| variable| explanation |
| ------ | ------ |
| postgres_user_pass | OS user password|
| postgres_db_pass | postgres user password|
| pg_allowed_ipaddress | allowd network segment for db access  |
| server_name | pleasanter server name or ip address |

run ansible playbook
```sh
ansible-playbook -i inventory.ini pleasanter-setting.yml
```