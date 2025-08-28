# Playbooks

Ansible uses YAML as its back-end data source and Jinja2 for templating. It refers to its documents with collections of tasks as playbooks. Ansible uses an inventory file to describe all the nodes which can be configured by Ansible; /etc/ansible/inventory.&#x20;

The tasks are run in the order specified in a playbook against all these hosts in parallel, and Ansible waits until all hosts have completed a task before moving to the next task.&#x20;

As example, this is a simple Playbook to install Apache.

```
---
- name: This sets up an httpd webserver
  hosts: www.local
  tasks:
  - name: Install the httpd rpm
    yum: name=httpd
  - name: start the httpd service
    service: name=httpd state=started
  - name: Open port 80
    firewalld: service=http permanent=true state=enabled
  - name: start the firewalld service
    service: name=firewalld state=restarted
```

Go [here](http://docs.ansible.com) and begin to have a look around at the Ansible docs.
