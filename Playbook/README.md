# Ansible Playbook

An Ansible® Playbook is a blueprint of automation tasks—which are complex IT actions executed with limited or no human involvement. Ansible Playbooks are executed on a set, group, or classification of hosts, which together make up an Ansible inventory.

## Playbook Contents
Ansible playbook can have one or more of the following items in it:
- Variable
- Tasks
- Files
- Templates
- Modules
- Handlers

 ## Ansible Variables
In Ansible, variables provide the much-needed flexibility in Playbooks, templates and inventories.

Ansible variables can be classified into two categories:
- System defined variables (built-in variables):
    - hostvars,groups, group_names etc.
- User defined variables (custom variables):
    - myvar, var, var200, tune_01 etc.

## Ansible Tags
Tags are metadata that you can attach to the tasks in an Ansible playbook. They allow you to selectively target certain tasks at runtime, telling Ansible to run (or not run) certain tasks. While you would typically run an entire Ansible playbook from start to finish, it can be extremely useful to run specific tasks within a playbook on demand.

### Command
```
ansible-playbook -v playbook/apache.playground.yml --tags="restart_tag" --become --ask-become-pass
```

## Ansible Roles
Roles provide a framework for fully independent, or interdependent collections of variables, tasks, files, templates, and modules.

In Ansible, the role is the primary mechanism for breaking a playbook into multiple files. This simplifies writing complex playbooks, and it makes them easier to reuse. The breaking of playbook allows you to logically break the playbook into reusable components.