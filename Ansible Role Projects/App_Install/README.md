**Ansible Project: Web Server and Database Server Setup**

This project uses Ansible roles to configure and deploy a web server (Apache HTTPD) and a database server (PostgreSQL). The configurations are modularized into roles for better reusability and maintainability.

**Roles Overview**

**_1. Web Server (webserver)_:**

Installs Apache HTTPD.

Copies barsha_file to /home/ubuntu/users/.

**_2. Database Server (dbserver)_:**

Installs PostgreSQL.

Starts the PostgreSQL service.

playbook.yml          # Main playbook to execute roles
roles/
├── webserver/
│   ├── tasks/
│   │   └── main.yml   # Web server tasks
│   ├── files/
│   │   └── barsha_file # File to copy to the web server
├── dbserver/
│   ├── tasks/
│   │   └── main.yml   # Database server tasks

