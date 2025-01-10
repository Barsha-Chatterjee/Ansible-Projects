Ansible Playbook: Web Server and Database Server Setup

Overview:

This Ansible playbook is designed to automate the configuration of web servers and database servers. It performs the following tasks:

Web Servers:

1.Installs Apache HTTP Server (HTTPD) on target web servers.

2.Copies a file (barsha_file) to a specified directory (/home/ubuntu/users/) on the web servers with specific ownership and permissions.

Database Servers:

1.Installs PostgreSQL on target database servers.

2.Ensures the PostgreSQL service is started and running.
