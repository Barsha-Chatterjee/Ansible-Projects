This playbook helps to provision EC2 instance using ansible. Also shows how ansible-vault can encrypt sensitive data like passwords, API tokens etc.,within a playbook

**Syntax to create ansible-vault :**

1. _Create a random password for vault_ 
   
           openssl rand -base64 2048 > vault.pass

  
2. _Create a file with sensitive data and encrypt it_
   
           ansible-vault create group_vars/all/pass.yml --vault-password-file vault.pass





