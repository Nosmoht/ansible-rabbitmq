ansible-role-rabbitmq
=========

Ansible role to install and configure RabbitMQ on RHEL based systems.

Requirements
------------

No requirements yet.

Role Variables
--------------

    rabbitmq_package_name: rabbitmq-server
    rabbitmq_package_state: installed
    rabbitmq_service_name: rabbitmq-server
    rabbitmq_service_state: running
    rabbitmq_service_enabled: true

Dependencies
------------

No dependencies.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: Nosmoht.ansible-role-rabbitmq }

License
-------

BSD

Author Information
------------------

Name: Thomas Krahn
mail: ntbc@gmx.net

