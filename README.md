# Ansible: Netbox Installation

An Ansible playbook to run through the installation process of [Netbox](https://github.com/netbox-community/netbox).

## Netbox
   * v3.7.0
## Compatibility
   * Ubuntu 22.04LTS

## Ansible Control Dependencies
   * community.general

## Current Installation Process
1. Ensure your Ansible control node can communicate with your desired Netbox server
2. Copy `inventory.example.yml` to `inventory.yml` and modify to reflect your environment
3. Copy `config.example.yml` to `config.yml` and add the Netbox superuser name, database name and database user.
4. Run `ansible-vault create secrets.yml`, enter a password for the vault and add the following variables to the file:
   ```yaml
   db_password: <your-database-password>
   nb_password: <netbox-superuser-password>
   nb_email: <netbox-superuser-password>

   ```
5. Run `ansible-playbook main.yml`
