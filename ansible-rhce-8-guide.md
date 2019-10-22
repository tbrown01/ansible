# Ansible RHCE 8 Exam Objectives

This guide will cover the RHCE 8 Exam Objectives which focuses heavily on Ansible.

## Install and Configure an Ansible Control Node

- **Install Required Packages**
```
~]$ yum install -y ansible
```
- **Create a Static Host Inventory File**
```
~]$ vim ansible-playbook -i /opt/ansible/hosts

[webservers]
webserver[01:99].example.com

[dbservers]
dbserver01.example.com
dbserver02.example.com

~]$ ansible -i /opt/ansible/hosts webservers -m ping
```
- **Create a configuration File**
```
~]$ cp /etc/ansible/ansible.cfg   /opt/ansible/

/etc/ansible/ansible.cfg          # Default Location
```
Configuration Locations (In Order Processed):

1. ANSIBLE_CONFIG (Environment Variable)
2. ansible.cfg file in current directory.
3. ansible.cfg file in home directory.
4. ansible.cfg file in default location.


## Understand core components of Ansible

- **Inventories**
An inventory is a list of hosts that Ansible manages.
```
~]$ vim /etc/ansible/hosts                    # Default Location

~]$ ansible-playbook -i /opt/ansible/hosts   # CLI Specified Location
```
- **Modules**
Ansible ships with a number of modules (called the ‘module library’) that can be executed directly on remote hosts or through Playbooks.
```
~]$ ansible-doc <modue_name>          # Documentation Availabe for Each Module
```
More Information: https://www.github.com/tbrown01/ansible/1-ansible-rhce8-modules.md

- **Variables**

- **Facts**
- **Plays**
- **Playbooks**
- **Configuration files**

## Configure Ansible managed nodes

- Create and distribute SSH keys to managed nodes
- Configure privilege escalation on managed nodes
- Validate a working configuration using ad hoc Ansible commands

## Script administration tasks

- Create simple shell scripts
- Create simple shell scripts that run ad hoc Ansible commands
