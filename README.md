Role Name
=========

This role will:
- Ensure the presence of DHCPD service.
- Ensure the presence of standard configuration file.
- Ensure the service is started and enabled.

The role was wrote to attent a very specif demand where many DHCP servers share the same configuration.
In this case, for instance, there are a company with many branch offices with the same guest network.

Admins:
- Manage the custom settings in vars/main.yml.
- Maybe you want to change the NTP server in templates/dhcpd.conf.j2

Requirements
------------

Just a working repository.

Role Variables
--------------

In the defaults/main.yml and vars/main.yml there are some interesting variables that should be checked.

Dependencies
------------

None

Example Playbook
----------------

1) Install and use the default settings.

```

- hosts: dhcp-servers
  roles:
    - role: ansible-role-dhcp
```

License
-------

MIT

Author Information
------------------

Marcus Burghardt - marcus.apb@gmail.com
@MBSEC - marcus@mbsec.com.br
https://mbsec.com.br

