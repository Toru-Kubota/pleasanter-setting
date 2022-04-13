# Install Pleasanter on Almalinux Server
## Requirements
* AlmaLinux release 8.5

## Installation

### Change OS security setting

* disable SELinux 
* open 80 port on firewalld

### Change following variable
group_vars/plesanter_server.yml

* set OS postgres user password
postgres_user_pass: "**********"

* set postgres db user password
postgres_db_pass: "**********"

* set allowd network segment for db access
pg_allowed_ipaddress: "xx.xx.xx.xx/xx"

* set server name or ip address on plesanter server
server_name: "xx.xx.xx.xx"

### Run playbook
ansible-playbook -i inventory.ini pleasanter-setting.yml