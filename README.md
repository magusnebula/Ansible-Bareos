# Ansible-Bareos
Ansible module for rolling out a Bareos Enviroment

## Running the playbook
```
ansible-playbook site.yml -i ./hosts
```

## Runing the playbook using Ansible Vault
```
ansible-playbook site.yml -i ./hosts --vault-password-file ./vault.txt --sudo
```
Change your playbook to reflect using the vault file, and the correct user name to use. Use ``--sudo`` to sudo as that user on remote machines.

```
- hosts: clients
  user: user_name
  vars_files:
    - secret
  gather_facts: yes
  roles:
    - common
```
