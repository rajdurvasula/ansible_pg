# ansible_pg
Ansible Playbook for PostgreSQL

# Setup
To setup specific version of PostgreSQL, edit vars/pg.yml

# Run
To run playbook follow these steps:
* Update /etc/ansible/hosts for static inventory
* For AWS dynamic inventory, ensure ec2.py, ec2.ini variables are set
* Run the command for static inventory
ansible-playbook pg_site.yml
* Run the command for AWS dynamic inventory
ansible-playbook pg_site.yml -e aws_access_key=$AWS_ACCESS_KEY_ID -u ec2-user -e aws_secret_key=$AWS_SECRET_ACCESS_KEY -e variable_host=tag_Name_$INSTANCE_NAME
