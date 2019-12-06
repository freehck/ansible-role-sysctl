freehck.sysctl
=========

This role simply wraps sysctl module

Description
-----------

Useful to put it into dependencies

Role Variables
--------------

`sysctl_opt_name`: option name

`sysctl_opt_value`: option value

`sysctl_opt_state`: `present`(default)/`absent`

`sysctl_write`: boolean, default `true`, flag to write sysctl.conf

`sysctl_apply`: boolean, default `true`, flag to apply changes from sysctl.conf

TODO
----

`sysctl_opts`: to apply a bunch of options, not just one, and in format `OPT=VAL`

Example
-------

    - hosts: all
      become: true
      roles:
        - role: freehck.sysctl
          sysctl_opt_name: "net.ipv4.ip_forward"
          sysctl_opt_value: "1"

Install
-------

This role can be installed from [Ansible Galaxy](https://galaxy.ansible.com/):

`ansible-galaxy install freehck.sysctl`

License
-------

MIT

Author Information
------------------

Dmitrii Kashin, <freehck@freehck.ru>
