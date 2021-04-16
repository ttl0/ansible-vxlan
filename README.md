# Ansible VXLAN

An ansible playbook to provision a VXLAN + EVPN LAB on EVE-NG using the
following topology:

![topology](topology.jpg)

## Instructions

This lab is using NKOSv9K-9.2.2 on EVE-NG and has DHCP enabled on the mgmt0
interfaces for reachability.

1. Update the hosts file with the proper IP addresses to reach each mgmt0
interfaces.
2. Update the group_vars/all.yml file with the proper username/password. I'm
using admin/admin for this example.
3. Make sure you have paramiko installed. 
```
pip3 install paramiko --user
```
4. Install the cisco.nxos module if you don't have it. 
```
ansible-galaxy collection install cisco.nxos
```
The playbook was tested with version 1.4.0
3. Run the playbook. 
```
ansible-playbook site.yml
```
