This Ansible playbook is designed to perform system validation and Docker installation on a list of hosts defined in the inventory file. It includes three primary tasks executed sequentially on each target host:

**1. Check for OpenSSH and OpenSSL:** The playbook verifies if both OpenSSH and OpenSSL are installed on the system.

**2. Check for Docker:** It checks whether Docker is already installed on the host.

**3. Install Docker (if not present):** If Docker is not found, the playbook proceeds to install it on the respective host.

****What if error handling is not used:****

If a task fails on any specific host, Ansible will not execute the subsequent tasks on that host.

However, if the task succeeds on other hosts, the playbook will continue execution for those successful hosts.

**Example Scenario:**

If Task 1 (checking for OpenSSH and OpenSSL) fails on Node 1, then Tasks 2 and 3 will be skipped for Node 1.

If the same task succeeds on Node 2 and Node 3, the playbook will continue and execute Tasks 2 and 3 on those nodes.

_But, when error handling is used, even if a task fails at any point on a server, the next task will still continue to execute on that same server._

**Syntax: ** 
1. ignore all types of errors
          ignore_errors: yes
2. ignore only particular type of errors
          failed_when:
                 - <condition 1>
                 - <condition 2>
