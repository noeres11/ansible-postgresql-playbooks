# Ansible PostgreSQL Playbooks

This repository contains Ansible playbooks for automating common PostgreSQL administration tasks.

## Included Playbooks

- `create_users.yml`: Creates PostgreSQL users with basic privileges.

## Requirements

- Ansible installed on your local machine.
- PostgreSQL running on the target host.
- The target host configured in the `inventory.ini` file.

## How to use it

```bash
ansible-playbook -i inventory.ini create_users.yml
