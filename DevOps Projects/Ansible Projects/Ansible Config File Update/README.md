To manage all servers within the stack using Ansible, the Nautilus DevOps team is planning to use a common sudo user among all servers. Ansible will be able to use this to perform different tasks on each server. This is not finalized yet, but the team has decided to first perform testing. The DevOps team has already installed Ansible on jump host using yum, and they now have the following requirement:

On jump host make appropriate changes so that Ansible can use ravi as a default ssh user for all hosts. Make changes in Ansible's default configuration only —please do not try to create a new config.

Solution:

sudo vi /etc/ansible/ansible.cfg
#Add below changes to end of file.
remote_user = ravi