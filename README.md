Role Name
=========

This role is used by this repo [https://github.com/nicholasrodriguez/lab] to deploy dhcp for an Ansible lab or test environment.

A dhcp scope from x.x.x.100 to x.x.x.200 will be created

The router ip is the first in the lab subnet

Requirements
------------

* Lab variables are defined in  [https://github.com/nicholasrodriguez/lab/blob/main/controller_setup.sh]
* Lab subnet is a /24
* Role tested on CentOS 7 and CentOS 8

Role Variables
--------------

|Variable|Default|Comments|
| :---| :---| :---|
| `authoritative`| `authoritative`| |
| `log_facility`| `local7`| |
| `ddns_updates`| `off`| |
| `default_lease_time`|`1800`| |
| `min_lease_time`|`180`| |
| `max_lease_time`|`1800`| |
| `domain`| From lab variables| |
| `dns1`| From lab variables| |
| `dns2`| From lab variables| |

Dependencies
------------

None required

Example Playbook
----------------

```
    - hosts: servers
      roles:
         - role: nicholasrodriguez.dhcp
```

License
-------

MIT

Author Information
------------------

- https://github.com/nicholasrodriguez/ (maintainer)
