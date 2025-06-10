## How to use

This install everything I personally need on a VM at the moment.
Im also running this from the VM, you can also run this from your host machine using inventory.ini and a ssh connection to your VM in fact thats the standard

### Install ansible
# On Ubuntu/Debian
sudo apt update
sudo apt install ansible

# Copy this repo
In the repo run this command to test the connection:
```
- ansible -i inventory-local.ini all -m ping
```
If this fails asks big C for help until it works

# Run Ansible for real
```
ansible-playbook -i inventory-local.ini setup-vm.yml --ask-become-pass
```
# Don't forget to configure Git
```
git config --global user.name "Your Name"
```
```
git config --global user.email "your@email.com"
```

(And add the ssh key to your github !)

