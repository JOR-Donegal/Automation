# Gathering Facts

Before Ansible starts any serious configuration, it gathers facts. This is the process of querying the target host and extracting any relevant information for its configuration. If you find a CentOS server, you might use yum for configuration, if it’s a Debian-based distro, you will use apt.

* CPU architecture
* Operating system
* Version
* Memory architecture
* Disc architecture&#x20;

Ansible uses a module called set up to do this, you can call this module from the command line to see what Ansible sees. In terms of Python, the return structure is a dictionary. Interestingly, you can leave a facts file on any host, and access and utilise the content.  
