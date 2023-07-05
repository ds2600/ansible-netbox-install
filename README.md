# Ansible: Netbox Installation

Currently a group of various playbooks to install Netbox. Soon I will push a main.yml to make easier. Also my first playbook, so if you find something that can be cleaner, go ahead and submit a pull request.

## Basics
These playbooks were designed and tested on Linode (now Akamai) running Ubuntu 22.04 LTS. In theory it should work anywhere you can push your SSH key to. The current playbooks install Netbox 3.5.4.

## Current Installation Process

1. Ensure you can log into your remote machine via SSH certificate.
2. Copy `hosts.example.ini` to `hosts.ini` and modify IP in the `hosts.ini` file to reflect your remote server and the correct `ansible_user`
3. Copy `vars.example.yml` to `vars.yml` and add a secure database password to the `db_password` variable
4. Run the playbooks in the following order:
   - initial.yml
   - postgres.yml
   - redis.yml
   - netbox.yml
   - housekeeping.yml
5. Stop here, SSH into your remote server and create a Netbox superuser:
    ``` shell
    source /opt/netbox/venv/bin/activate
    cd /opt/netbox/netbox
    python3 manage.py createsuperuser
    ```
6. Run the remaining playbooks:
   - gunicorn.yml
   - http.yml
