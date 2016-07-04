

# Ansible mysql server

- Install mysql-server | mysql-server on Ubuntu/Debian. 
- No password has to be configured. 
- This role generates a random password for the root user.
- If you need the password find it in /root/.my.cnf.


## Role variables:

Give the exact package name you want to install. 
This is important for preseeding the generated password.

    mysql_server_package: mysql-server-5.5
    
Or

	mysql_server_package: mariadb-server-10.1

Charset

	mysql_server_character_set: 'utf8'
	mysql_server_collation: 'utf8_general_ci'

SQL-Mode
	
	mysql_server_sql_mode: 'STRICT_TRANS_TABLES,NO_AUTO_CREATE_USER,NO_ENGINE_SUBSTITUTION'
	
Listen address

	mysql_server_bind_address: 127.0.0.1


## Dependencies

None.


## Example Playbook

    ---  
    - hosts: mysql
      become: true
      roles:
        - netzwirt.mysql-server


## License

BSD


## Author Information

[netzwirt](https://github.com/netzwirt)
