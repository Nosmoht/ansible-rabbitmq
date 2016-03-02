rabbitmq
=========
- [Introduction](#introduction)
- [Requirements](#requirements)
- [Variables](#variables)
- [Usage](#usage)
- [License](#license)

# Introduction
Ansible role to install and configure RabbitMQ on RHEL based systems.

# Requirements
- Ansible >= 2.0

# Variables
| Name | Description | Default |
|:-----|:------------|:--------|
| rabbitmq_package_names | Package names to install | rabbitmq-server |
| rabbitmq_package_state | Package state | installed |
| rabbitmq_service_name | Service name | rabbitmq-server |
| rabbitmq_service_state | Service state | running |
| rabbitmq_service_enabled | Service enabled | true |
| rabbitmq_users | Users to ensure | [] |

To define users use:
```yaml
rabbitmq_users:
- name: admin
  password: secret
  vhost: '/'
  configure_priv: '.*'
  read_priv: '.*'
  write_priv: '.*'
```

# Usage
```yaml
- hosts: servers
  roles:
  - role: rabbitmq
```

# License

BSD

# Author
[Thomas Krahn](mailto:ntbc@gmx.net)
