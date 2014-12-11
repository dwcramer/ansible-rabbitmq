# Rabbitmq role for Ansible

Installs RabbitMQ from the official apt repository and applies the specified configuration options.

## Requirements

Tested on Ubuntu 12.04 Server.

## Role Variables

    rabbitmq_user: 'admin'         # The administrator username
    rabbitmq_password: 'changeme'  # The administrator's password (should be changed)

## Example Playbook

    - hosts: 'servers'
      roles:
        - role: { 'ssilab.rabbitmq' }
          rabbitmq_user: 'admin'
          rabbitmq_password: 'changeme'

# License

This playbook is provided 'as-is' under the conditions of the BSD license. No fitness for purpose is guaranteed or implied.