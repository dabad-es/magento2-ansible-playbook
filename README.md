# Magento 2 Ansible Playbook

This is an Ansible Playbook for Magento 2. It is used to launch the following steps:

1. Install the software requeriments (if they aren't installed yet).
2. Retrieve Magento project content from a GIT repository.
3. Deploy Magento project.

More info in [www.dabad.es](https://dabad.es)

## Author

- [David Abad](https://dabad.es)
- This playbook is forked from [mjah/magento2-ansible-playbook](https://github.com/mjah/magento2-ansible-playbook). Thank you!


## Installation and use

1. Install Ansible:

```bash
sudo apt update
sudo apt install software-properties-common
sudo add-apt-repository --yes --update ppa:ansible/ansible
sudo apt install ansible
```

2. Clone this Playbook:

```bash
git clone https://github.com/dabad-es/magento2-ansible-playbook.git ~/ansible
```

3. Define the remote server host in the `hosts` file: 

```bash
[magento]
host01 ansible_host=X.X.X.X ansible_user=XXXX ansible_password=XXXX ansible_become_password=XXXX
```

4. Define settings in the `group_vars/all.yml`:


5. Launch the Playbook: 

```bash
ansible-playbook -i hosts site.yml
```


## Software requeriments

This Playbook installs the following software requeriments (if they aren't installed on the remote server yet):

- Nginx
- PHP
- Composer
- MariaDB (MySQL)
- Open Search
- RabbitMQ
- Redis
- Certbot

