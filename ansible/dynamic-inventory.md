# Dynamic Inventory

Once we get to large-scale cloud environments, static configuration files are no longer adequate to tracker infrastructure. Suppose I have a flexible deployment where I provision services as required in AWS. In this case, my inventory will be dynamic in nature, new server instances will spin up and spin down as required.&#x20;

Ansible handles this by allowing an inventory file to be executable under-Python. If Ansible sees an executable file, it assumes that it should be run and that it will return a JSON object with the inventory data.&#x20;

At the other end of all this is a cloud service provider like AWS, which provides an API containing this inventory information.
