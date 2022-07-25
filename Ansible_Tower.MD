# Ansible Tower:
Ansible Tower (formerly ‘AWX’) is a web-based solution that makes Ansible even more easy to use for IT teams of all kinds. 
It’s designed to be the hub for all of your automation tasks.

Tower allows you to control access to who can access what, even allowing sharing of SSH credentials without someone being able to transfer those credentials. 
Inventory can be graphically managed or synced with a wide variety of cloud sources. 
It logs all of your jobs, integrates well with LDAP, and has an amazing browsable REST API. 
Command line tools are available for easy integration with Jenkins as well. Provisioning callbacks provide great support for autoscaling topologies.

![ScreenShot](https://github.com/kumarrkslinux/Ansible/blob/main/Anbile-Tower-strategy.png)

### Features:
1. A graphical user interface dashboard.
2. Role-based access control.
3. Job scheduling.
4. Graphical inventory management.
5. A multi-playbook workflow.
6. RESTful APIs.
7. External logging integrations.
8. Real-time job status updates.
9. Integrated Notification 
10. PostgreSQL DB has been used and before 3.1 it was Mongodb 
11. Rabbitmq messaging
12. From 3.1 version Active/Active Cluster will support


### Procedure of installtion: 
1. Ansible package need to be install and password has to be set in the inventory file in the downloaded files
2. ./setup.sh has to be run 
3. Password less authentication need to be created on all the servers client and master. 

## Components: 

### Project:
A Project is a logical collection of Ansible playbooks, represented in Tower. 

### Credential:
- Credentials are utilized by Tower for authentication when launching Jobs against machines, synchronizing with inventory sources, and importing project content from a version control system.
- You can grant users and teams the ability to use these credentials, without actually exposing the credential to the user. If you have a user move to a different team or leave the organization, you don’t have to re-key all of your systems just because that credential was available in Tower

### Inventory:
An Inventory is a collection of hosts against which jobs may be launched, the same as an Ansible inventory file. Inventories are divided into groups and these groups contain the actual hosts. Groups may be sourced manually, by entering host names into Tower, or from one of Ansible Tower’s supported cloud providers.

### Job Templates
A job template is a definition and set of parameters for running an Ansible job. Job templates are useful to execute the same job many times. Job templates also encourage the reuse of Ansible playbook content and collaboration between teams. While the REST API allows for the execution of jobs directly, Tower requires that you first create a job template.
