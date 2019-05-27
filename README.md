EC2-ASG
=========

Create AWS EC2 Auto Scaling Groups

Requirements
------------

The boto package is required for this role

Role Variables
--------------

You are required to pass in the following variables:

  - component
  - service
  - env
  - region
  - ami_id
  - sec_groups

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
        component: mgt
        env: nonprod
        service: auth
        region: eu-west-2
        sec_groups:
          - Auth-SG
          - default
        ami_id: ami-01234567
      roles:
         - { role: ec2-asg }

License
-------

GPL

Author Information
------------------

Iain M Conochie <iain@shihad.org>
