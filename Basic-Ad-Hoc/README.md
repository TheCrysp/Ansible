# Ansible Ad Hoc Commands

Ansible ad hoc commands are CLI commands used for simple and one-time tasks. One-time tasks include checking whether the nodes are reachable over SSH, shutting down all nodes, and so on. They can easily be run at scale and even concurrently on several hosts at the same time with a single command. 

![Ad-Hoc Syntax](/media/syntax.png)

## Ansible Modules

Modules represent distinct units of code, each one with specific functionality. Basically, they are standalone scripts written for a particular job and are used in tasks as their main functional layer.

Some example of modules are:
- Setup Module
- Apt Module
- Yum Module
- File Module
- Copy Module
- Ping Module
- Shell Module
- Service Module


**Note**: Use ```-become -u username``` to execute command from another user account. 

**File Creation:** 
```
ansible website -m file -a "path=/tmp/newfile state=touch mode=0755"
```

**Copy File: Local to Remote**
```
ansible website -m copy -a 'src=/home/loki/Desktop/Ansible/Basic-Ad-Hoc/inventory dest=/tmp'
```

**Install Package**
```
ansible website -m apt -a 'name=neofetch state=present' --become --ask-become-pass
```

**Note**: Use ```--become --ask-become-pass``` to execute command with sudo(default). 

**Shell Command**
```
ansible website -m shell -a 'neofetch'
```

**Services**
```
ansible website -m service -a 'name=sshd state=started' -become --ask-become-pass
```