# Ansible RHCE 8 Exam Objectives

This guide will cover the RHCE 8 Exam Objectives which focuses heavily on Ansible.

## Install and Configure an Ansible Control Node

- Install required packages
```
~]$ yum install -y ansible
```
- Create a static host inventory file

- Create a configuration file


## Understand core components of Ansible

- Inventories
An inventory is a list of hosts that Ansible manges.
```
~]$ vim /etc/ansible/hosts			            # Default Location

~]$ ansible-playbook -i /opt/ansible/hosts		# CLI Specified Location
```
- Modules
- Variables
- Facts
- Plays
- Playbooks
- Configuration files

## Configure Ansible managed nodes

- Create and distribute SSH keys to managed nodes
- Configure privilege escalation on managed nodes
- Validate a working configuration using ad hoc Ansible commands

## Script administration tasks

- Create simple shell scripts
- Create simple shell scripts that run ad hoc Ansible commands
