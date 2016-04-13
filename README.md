# Fablab Karlsruhe ansible definitions

currently only used for the main server felix.

## General

```` bash
# get dependencies
ansible-galaxy install -r requirements.yml -p roles

# start vagrant test system
vagrant up

# reprovision test system
vagrant reload --provision
````


## Felix (central server)

```` bash
# provision live system
ansible-playbook -i hosts felix.yml --user=felix --ask-sudo-pass
````
