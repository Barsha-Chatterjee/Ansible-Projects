**Ansible Project: Web Server and Database Server Setup**

This project uses Ansible roles to configure and deploy a web server (Apache HTTPD) and a database server (PostgreSQL). The configurations are modularized into roles for better reusability and maintainability.

**1. Web Server Role (webserver)**
**Purpose:** Installs and configures Apache HTTPD on the target web server(s).
**Tasks:**
Install Apache HTTPD using the apt module.
Copy a file (barsha_file) to the specified directory on the server.
**File**: barsha_file is located under roles/webserver/files/.

**2. Database Server Role (dbserver)**
**Purpose:** Installs and configures PostgreSQL on the target database server(s).
**Tasks:**
Install PostgreSQL using the apt module.
Start the PostgreSQL service.
