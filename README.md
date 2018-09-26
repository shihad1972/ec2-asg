EC2-ASG
=========

Create AWS EC2 Auto Scaling Groups

Requirements
------------

The boto package is required for this role

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

If you require load balancers associated with the ASG, you should already have them created.

Example Playbook
----------------

    - hosts: localhost
      vars:
        volumes:
          - name: My_Volume
            size: 30
            zone: eu-west-1b
            device: /dev/xvdf
      roles:
         - { role: username.rolename, x: 42 }

License
-------

GPL

Author Information
------------------

Iain M Conochie <iain@shihad.org>
