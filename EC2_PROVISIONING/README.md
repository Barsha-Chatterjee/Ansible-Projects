This playbook helps to provision EC2 instance using ansible.

**Ansible Vault:** Its used to secure sensitive data like passwords, API tokens, encrypt a file etc., within the ansible playbooks/roles.

1. Create a password for vault
   
           _openssl rand -base64 2048 > vault.pass_
  
2. Add your AWS credentials using the below vault command
   
           _ansible-vault create group_vars/all/pass.yml --vault-password-file vault.pass_
