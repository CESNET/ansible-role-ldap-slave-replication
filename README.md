ldap_slave_replicaton
=========

Ansible Galaxy role [cesnet.ldap_slave_replication](https://galaxy.ansible.com/cesnet/ldap_slave_replication) that
configure replication on perun slave OpenLDAP server

Requirements
------------

OpenLDAP server must have loaded perun schemas ([cesnet.perun_ldap_schema_update](https://galaxy.ansible.com/cesnet/perun_ldap_schema_update) role can be used)

Role Variables
--------------

- slapd_base_dn - base dn of ldap server
- slapd_base_dn_admin - dn of admin
- master_dns - adress to master ldap server
- master_admin_password - password to admin of master ldap server

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: cesnet.ldap_slave_replication
      vars:
        slapd_base_dn: "dc=perun,dc=cesnet,dc=cz"
        master_dns: "78.128.3.24"
        master_admin_password: "test"
```