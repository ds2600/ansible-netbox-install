# Ansible: Netbox Installation

An Ansible playbook to run through the installation process of Netbox.

## Compatibility
   * Ubuntu 22.04LTS VM 
   * Ubuntu 22.04LTS Linode/Akamai.

## Ansible Control Dependencies
   * community.general

## Current Installation Process
1. Ensure your Ansible control node can communicate with your desired Netbox server
2. Copy `inventory.example.yml` to `inventory.yml` and modify the IP address and `ansible_user` to reflect your environment
3. Copy `config.example.yml` to `config.yml` and modify usernames and passwords.
***Do not use the passwords included in the example file, they are not secure.***
***Do not adjust the Netbox version - as 3.5.4 is the only tested version***
1. Run `ansible-playbook main.yml`
