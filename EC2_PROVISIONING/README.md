This playbook helps to provision EC2 instance using ansible.

**Ansible Vault:** Its used to secure sensitive data like passwords, API tokens, encrypt a file etc., within the ansible playbooks/roles.

1. _Create a random password for vault_ 
   
           openssl rand -base64 2048 > <vault_file_name.pass>

  
2. _Create a file with sensitive data and encrypt it_
   
           ansible-vault create path/to/the/credentials.yml --vault-password-file <vault_file_name.pass>

   (Note : If you don't want to create any random password then while encrypting file, don't use --vault-password file syntax)

****ANSIBLE VAULT OPTIONS:****

**create randow password** **-**  openssl rand -base64 2048 > vault.pass

**create new vault encrypted file** **-** ansible-vault create group_vars/all/pass.yml --vault-password-file vault.pass

**Edit the file** **-** ansible-vault edit group_vars/all/pass.yml --vault-password-file vault.pass

**Decrypt the file** **-** ansible-vault decrypt group_vars/all/pass.yml --vault-password-file vault.pass

**View the Encrypted file** **-** ansible-vault view group_vars/all/pass.yml --vault-password-file vault.pass

**encrypt already existing file** **-** ansible-vault encrypt group_vars/all/pass.yml

**change existing vault the password** **-** ansible-vault rekey vault.pass  (You’ll be prompted for the current password and then to enter a new password twice)




