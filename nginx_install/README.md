Role Name
=========

`nginx_install` is an Ansible role for installing and configuring the NGINX web server on Ubuntu-based systems.

Requirements
------------

- The target machine should be running Ubuntu (or a compatible Debian-based distribution).
- Ansible must be installed on the control node.
- SSH access to the target machine with a valid private key.

  
Role Variables
--------------

The following variables can be configured to customize the role:

| Variable                | Default Value | Description                          |
|-------------------------|---------------|--------------------------------------|
| `nginx_state`           | `present`     | Whether to install or remove NGINX.  |
| `nginx_service_state`   | `started`     | Desired state of the NGINX service.  |
| `nginx_service_enabled` | `yes`         | Whether to enable NGINX at boot.     |

To override these variables, define them in your playbook or an external vars file.


Dependencies
------------

This role does not have any external dependencies.

Example Playbook
----------------

Here’s an example playbook using this role:
.yaml file

---
- name: Install and Configure NGINX
  hosts: nginx_servers
  vars:
    nginx_state: present
    nginx_service_state: started
    nginx_service_enabled: yes
  roles:
    - nginx_install


License
-------

MIT

Author Information
------------------

This role was created by Jitendra, as part of an Ansible automation project to install and manage NGINX on EC2 instances.
