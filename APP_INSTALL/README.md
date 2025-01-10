**Ansible Playbook: Web Server and Database Server Setup**

**_Overview:_**

This Ansible playbook is designed to automate the configuration of both web servers and database servers. It utilizes Ansible Built-in Modules to perform the tasks efficiently. Below is a detailed description of the operations performed.

**_Web Servers:_**

1.Installs Apache HTTP Server (HTTPD) on target web servers.

2.Copies a file (My_file) to a specified directory (/home/ubuntu/users/) on the web servers with specific ownership and permissions.

**_Database Servers:_**

1.Installs PostgreSQL on target database servers.

2.Ensures the PostgreSQL service is started and running.
