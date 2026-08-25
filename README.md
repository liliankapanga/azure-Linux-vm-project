# Azure Linux VM Project
## Project overview
This project involved deploying and configuring an Ubuntu Linux Virtual Machine in Microsoft Azure, covering networking, security, Linux administrator, Apache web server, and access management.
## Technologies and Azure Services
* ** Cloud platform; ** Microsoft Azure
*  ** Compute and OS; ** Ubuntu Linux VM (Standard SSD)
*  ** Networking and security; ** Virtual Network (VNet), Subnet, Network Security Group (NSG)
*  ** Web Server; ** Apache HTTP Server
*  ** Identity and Governance; ** Azure RBAC, Resource Tags, Auto-Shutdown 
## What I Configured
* Created an Ubuntu Linux virtual machine
* Configured a Virtual Network and subnet
* Configured NSG rules for SSH (port 22) and HTTP (port 80)
* Connected to the VM using SSH
* Installed and configured Apache
* Configured auto-shutdown
* Added resource tags
* Implemented Azure RBAC using the Reader
## Challenges and solutions
* ** RBAC scope;* Learned the difference between assigning a role at te resource group level versus the subscription, and applied the Reader role at the appropriate scope to avoid over provisioning access
*  ** Cost management; ** Realized the VM would keep accumulating cost while running idle, so i configured the auto shutdown to automatically deallocate it during off hours
*  ** NSG rules; ** Initially couldn't reach the webserver over HTTP because port 80 wasn't open in the network security group. Adding an inbound rule for port 80 (alongside SS on port 22) resolved it this taught me how NSG act as the first layer of the network security in Azure, separate from anything configuring on the VM Itself

