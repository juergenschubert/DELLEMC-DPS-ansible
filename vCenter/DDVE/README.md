# DELLEMC-DPS-ansible vCenter deployment of a DDVE
This is a short excurse on how to deploy a DDVE into your vCenter environment.  

What you need is Ansible, ansible-galaxy collection community.vmware and a pimped ova with hostname and ip addresses added. 
unpack the ova from DELL and add the ovf which is attached and that repackage the ova.

I have created the whole environment on a Windows 2019 wsl with ubuntu 20.04.  

The playbook contains the variable.yml as well as the deploy-ddve-vcenter-stack.yml for the deployment of a DDVE.  

You start is with # ansible-playbook deploy-ddve-vcenter-stack.yml 
