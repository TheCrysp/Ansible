## Ansible Terms

- **Controller Machine**: The machine where Ansible is installed, responsible for running the provisioning on the servers you are managing.
- **Inventory**: An initialization file that contains information about the servers you are managing.
- **Playbook**: The entry point for Ansible provisioning, where the automation is defined through tasks using YAML format.
- **Task**: A block that defines a single procedure to be executed, e.g. Install a package.
- **Module**: A module typically abstracts a system task, like dealing with packages or creating and changing files. Ansible has a multitude of built-in modules, but you can also create custom ones.
- **Role**: A pre-defined way for organizing playbooks and other files in order to facilitate sharing and re-
using portions of a provisioning.
- **Play**: A provisioning executed from start to finish is called a play. In simple words, execution of a play book is called a play.
- **Facts**: Global variables containing information about the system, like network interfaces or operating
system.
- **Handlers**: Used to trigger service status changes, like restarting or stopping a service.
