# DELLEMC-DPS-ansible 

This is the place to find Ansible scripts for configuration.
## DataDomain

Here you will find a yml playbook what you can walk thorugh to get a DDVE already deployed for Block Storage or Object Storage enabled so the filesystem is up and running. Object Storage is here for aws while block stroage can work on all DDVE and phyical DDs.
# role
creation of ansibles roles for easier use. 
Role for DDVE post deploy on aws with object storage. 
Role for DDVE post deploy on block storage.   

 # yml files
 yml playbooks do show all available ansible roles and how to execute. Please make sure that you edit the need vars in the roles/vars directory  
 Starting a DDVE config in aws with object storage 
 
❯ ansible-playbook ddve6-post-object-aws-playbook.yml  
What it will do:   
Login to the DDVE.   
Change the default password to "Password123!".     
add a new DD license.  
Change/create new Passphrase to "Password123!"  
Enable object storage with the dev you have added.  
create the DD filesystem.   
enable the DD filesystem. 
enalbe DDBoost.  

❯ ansible-playbook ddve6-post-block-storage-playbook.yml
What it will do:   
Login to the DDVE.   
Change the default password to "Password123!".     
add a new DD license.  
Change/create new Passphrase to "Password123!"  
Enable block storage with the dev you have added.  
create the DD filesystem.   
enable the DD filesystem. 
enalbe DDBoost.  

