This playbook helps to provision EC2 instance using ansible.

**Ansible Vault:** Its used to secure sensitive data like passwords, API tokens, encrypt a file etc., within the ansible playbooks/roles.

1. _Create a password for vault_
   
           openssl rand -base64 2048 > vault.pass
  
2. _Add your AWS credentials using the below vault command_
   
           ansible-vault create group_vars/all/pass.yml --vault-password-file vault.pass
