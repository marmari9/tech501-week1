## Azure:

- [Azure:](#azure)
  - [Create a virtual network:](#create-a-virtual-network)
  - [Create a virtual machine:](#create-a-virtual-machine)
  - [Connect local machine to VM:](#connect-local-machine-to-vm)
  - [when deleting VM delete:](#when-deleting-vm-delete)


### Create a virtual network:
- Create Vnet name: tech501-maram-2-subnet-vnet
- Create 2 subnets ; a public and private
    - public subnet : 10.0.1.0/24 ~ 256 IPs
    - Private subnet: 10.0.3.0/24 ~ 256 IPs
- paste your public .ssh key pair.(ensure private is kept secret).
- ARM (Azure resource manager), Azure API.

### Create a virtual machine:

- Name: tech501-your_name-first-vm
- Region: UK South
- Security: standard
- Image (i.e. the OS that will go onto the machine): Ubuntu Pro 18.04 LTS Gen 2 [LTS means long term support for ~7 years]
- Size: Standard_B1s — 1 vcpu, 1 GiB [very important to set correctly because this impacts pricing]
- Administrator account: adminuser
- Use existing key pair stored in Azure (use the one with your name)
- Select inbound ports: allow HTTP and SSH traffic
- Disks tab: disk type: Standard SSD
Networking tab:
- Virtual network: your named version
- Subnet: public-subnet
- Choose Delete public IP and NIC when VM is deleted option
- make sure to stop VM when logged off. 


### Connect local machine to VM:
- from vm select connect and choose Native ssh connect.
- paste the pathway of the private key.
- paste the address into git and type yes. 


### when deleting VM delete:
- disk
- network interface
- security group
- public IP 
- VM





