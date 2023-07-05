# ansible-netbox-install

My first Ansible playbook... I know I'm behind the times. Either way, a main.yml is coming soon to include all the playbooks necessary.

For the time being, they need run in this order:
* initial.yml
* postgres.yml
* redis.yml
* netbox.yml
* housekeeping.yml
* PAUSE HERE AND CREATE SUPERUSER PER NETBOX INSTALLATION
* gunicorn.yml
* http.yml
