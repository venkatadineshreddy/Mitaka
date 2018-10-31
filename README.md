# Openstack-Mitaka_With-Ansible
Openstack Mitaka With Ansible
#Prerequisites:-
One node with Ansible installed. (You can use ansible in any one of openstack nodes or in separate node)
2 nodes with below configurations.

i. VM1(Controller) - Hard disk 50GB, RAM 4 GB, 1 CPU, Interfaces 3 ( 2 Host only adapter vboxnet0, 1 NAT )

ii. VM2(Compute) - Hard disk 50GB, RAM 2 GB, 2 CPU, Interfaces 3 ( 2 Host only adapter vboxnet0, 1 NAT )

Inside of code, we are using the only 2 interfaces(Host only). Here we are using NAT for internet connectivity purpose.

All 2 VMs should communicate with each other and with ansible node.

Software Versions
i. Ubuntu 14.04
ii. Ansible 2.4
   
And edit the below two file.

i. inventory/hosts :- Host file to ansible. Define the controller and compute IPs here.

ii. group_vars/all:- Define IPs, user names and passwords. 

And you can simply install the OpenStack with single command from openstack_main.yml file location.

#command:-
ansible-playbook -i inventory/ openstack_main.yml -vvv
--------------------------------------------------------
P. VENKATA DINESH REDDY
