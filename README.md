# Rabbitmq role for Ansible

Installs RabbitMQ from the official apt repository and applies the
specified configuration options.

## Requirements

Tested on Ubuntu 14.04 Server.

## Installation

In a `requirements.yml` file, add the lines:

```
- src: dwcramer.rabbitmq
  version: "1.0"
```

Where 1.0 is the desired version number of the role. Alternatively,
omit the version to use whatever is latest.

## Role Variables

    rabbitmq_user: 'admin'         # The administrator username
    rabbitmq_password: 'changeme'  # The administrator's password (should be changed)
    rabbitmq_nodename:             # Usually omitted. By default this is rabbit@$HOSTNAME.
                                   # It is sometimes necessary to set this if the host name
                                   # might change. Note that if you change the NODENAME
                                   # on an existing installation, existing rabbitmq database
                                   # is lost/unavailable.

## Example Playbook

    - hosts: 'servers'
      roles:
        - role: { 'ssilab.rabbitmq' }
          rabbitmq_user: 'admin'
          rabbitmq_password: 'changeme'

# License

This playbook is provided 'as-is' under the conditions of the BSD
license. No fitness for purpose is guaranteed or implied.
