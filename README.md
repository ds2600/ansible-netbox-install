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
2. Copy `inventory.example.yml` to `inventory.yml` and modify the IP address and `ansible_user` to reflect your environment
3. Copy `config.example.yml` to `config.yml` and add the superuser name, email and password
4. Run `ansible-playbook main.yml`
