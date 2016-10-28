# ansible-zabbix-docker
Install Dockerized Zabbix server on CentOS 7

Software: zabbix-server, zabbix-agent, mysql, nginx, php-fpm

Based on **[zabbix-docker](https://github.com/zabbix/zabbix-docker)**


## Variables
`container_state: "started"` State of zabbix containers: _started, stopped, present, absent_

`zabbix_data_path: "/srv/zabbix"` Path to zabbix data volumes

`zabbix_timezone: "Etc/GMT"`

`zabbix_name: "Zabbix Server"`

`zabbix_database: zabbix` Zabbix database name

`zabbix_db_user: zabbix` Zabbix database user name

`zabbix_db_password: zabbix` zabbix database password

`zabbix_mysql_root_password: root_pw` Database root password



## Dependencies
* [`ansible-pip`](https://github.com/aliusmiles/ansible-pip)
* [`ansible-docker`](https://github.com/aliusmiles/ansible-docker)


## Example
    - hosts: zabbix-server
      roles:
        - role: ansible-pip
        - role: ansible-docker
        - role: ansible-zabbix-docker


## Author
Taras Bondarchuk
