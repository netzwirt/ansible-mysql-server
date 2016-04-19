

# Ansible mysql server

- Install mysql-server on Ubuntu/Debian. 
- No password has to be configured. 
- This role generates a random password for the root user.
- If you need the password find it in /root/.my.cnf.


## Role variables:

Give the exact package name you want to install. 
This is important for preseeding the generated password.

    mysql_server_package: mysql-server-5.5

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
