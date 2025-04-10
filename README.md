# Ansible PostgreSQL Playbooks

This repository contains Ansible playbooks for automating common PostgreSQL administration tasks.

## Included Playbooks

- `create_database.yml`: Creates a PostgreSQL database (`testdb`) owned by the default user.
- `create_roles_and_users.yml`: Defines application roles (`read_only`, `read_write`), creates users, assigns roles, grants schema usage, table privileges, and sets default privileges for future objects.
- `create_tables.yml`: Creates a simple data model with students, courses, and enrollments.
- `insert_data.yml`: Inserts sample records into the database for testing purposes.
- `main.yml`: Orchestrates all of the above steps in the correct order for a clean setup.


## Requirements

- Ansible installed on your local machine, including `community.postgresql` collection.
- PostgreSQL running locally.
- Python 3
- `psycopg2`


## How to use it

## Run the main playbook:

```bash
ansible-playbook -i inventory.ini main.yml

## Run a single playbook directly (optional):

ansible-playbook -i inventory.ini create_roles_and_users.yml


## Notes

All playbooks assume connection as the local user with no become: true unless specified.
Default privileges are configured so that newly created tables automatically inherit the correct permissions.
The project is intentionally minimal and self-contained, to serve as a reference or starting point for more advanced setups.
