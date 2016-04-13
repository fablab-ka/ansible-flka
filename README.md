# Fablab Karlsruhe ansible definitions

currently only used for the main server felix.


## General

```` bash
# get dependencies
ansible-galaxy install -r requirements.yml -p roles

# start vagrant test system
vagrant up

# reprovision test system
ansible-playbook -i .vagrant/provisioners/ansible/inventory/vagrant_ansible_inventory felix.yml --user=vagrant
````


## Felix (central server)

```` bash
# provision live system
ansible-playbook -i hosts felix.yml --ask-sudo-pass
````
