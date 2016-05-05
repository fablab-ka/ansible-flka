# Fablab Karlsruhe ansible definitions

## General

```` bash
# get dependencies
ansible-galaxy install -r requirements.yml -p roles --ignore-errors

# start vagrant test system
vagrant up

# reprovision test system
vagrant provision

# edit vault file
ansible-vault edit vars/lasersaur.vault.yml

# list all available facts for a host
ansible -m setup hostname
````

## Machines

### Felix (central server)

```` bash
ansible-playbook -i hosts felix.yml --ask-sudo-pass
````

### Lasersaur
```` bash
ansible-playbook -i hosts lasersaur.yml --ask-vault-pass --ask-sudo-pass
````
