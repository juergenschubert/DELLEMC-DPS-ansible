# DELLEMC-DPS-ansible 

This is the place to find Ansible scripts for configuration.
## DataDomain

Here you will find a yml playbook what you can walk thorugh to get a DDVE already deployed for Block Storage or Object Storage enabled so the filesystem is up and running. Object Storage is here for aws while block stroage can work on all DDVE and phyical DDs.

 # yml files
 yml playbooks do show all available ansible roles and how to execute. Please make sure that you edit the need vars in the roles/vars directory  
 Starting a DDVE config in aws with object storeage 
 
❯ ansible-playbook ddve-post-object-aws-playbook.yml
