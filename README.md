# DELLEMC-DPS-ansible 

You can find more information on https://galaxy.ansible.com/docs/finding/content_types.html#ansible-roles about roles with ansible.

Ansible can be installed on your laptop. Please refer to https://phoenixnap.com/kb/install-ansible-on-windows for windows 10 installation.

Install Ansible on Mac OSX documentation can be found at https://hvops.com/articles/ansible-mac-osx/


This is the place to find Ansible scripts/roles for diferent use cases like configuration.
## DataDomain

Here you will find a yml playbook what you can walk thorugh to get a DDVE already deployed for Block Storage or Object Storage enabled so the filesystem is up and running. Object Storage is here for aws while block stroage can work on all DDVE and phyical DDs.
## role
creation of ansibles roles for easier use. this was done with  ansible-galaxy init datadomain-gen  
Directories underneath the roles directory are:  
datadomain-gen
Role for DDVE post deploy on aws with object storage -> ddve6-post-block-storage  
Role for DDVE post deploy on block storage -> ddve6-post-object-aws

 ## yml files
 yml playbooks do show all available ansible roles and how to execute. Please make sure that you edit the required vars in the roles/vars directory  
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

Here is a good place to talk about ansible vault, the way to encrypt passwords or yaml files.  
Encrypting content with Ansible Vault  https://docs.ansible.com/ansible/latest/user_guide/vault.html


Encrypted Specific Variables in Ansible
Ansible vault will prompt you for the password and later require you to confirm it. Next, type the string value that you want to encrypt. Finally, press ctrl + d. Thereafter, you can begin assigning the encrypted value in a playbook.

This can be achieved in a single line as shown below.  

```
# ansible-vault encrypt_string 'Password123!' --name 'New_User_Password'  
.....will ask you for a new vault password  
New Vault password:  
Confirm New Vault password:  
New_User_Password: !vault |  
          $ANSIBLE_VAULT;1.1;AES256  
          32383234303863346236653732333035633162656365313764366265356464633831303432383262  
          6532356666353164303532623831326333363135313332310a656261393564356437643366363433  
          61656261333438383063346666383630323130646432316630346232643438616136386563623664  
          6131386562643462650a383334303863323664393363626534336332613262393264623732393064  
          6239  
Encryption successful  
```