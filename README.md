Role Name
=========

Installs and configures PostgreSQL on Ubuntu.

Requirements
------------

- Target machine is Ubuntu.
- Hosts in inventories are their ip addresses, no names.

Role Variables
--------------

- postgresql_installing_packages: apt packages of postgresql to be installed
- postgresql_systemd_service_name: name of systemctl postgresql service
- postgresql_postgres_user: name of "postgres" user
- postgresql_data_directory_mode: permissions for postgresql data directory

- postgresql_replication_params_for_postgresql_conf_dict: dictionary of key-value params to be written 
to postgresql configuration files when configuring streaming replication

- postgresql_data_directory: custom data directory
- postgresql_databases: list of databases to be created
- postgresql_users: list of users to be created
- postgresql_db_user_owners_dict: dict of databases and users-their new owners
- postgresql_db_master_group_name and postgresql_db_replicas_group_name: when defined together give an ability to 
configure streaming replication, group_name - name of ansible inventory groups

Dependencies
------------

No dependencies.

Example Playbook
----------------

    - hosts: servers
      roles:
         - postgresql

License
-------

MIT

Author Information
------------------

Grigorii Simonov
