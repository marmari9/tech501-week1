- [Vnet:](#vnet)
- [Create a virtual network:](#create-a-virtual-network)
- [Create a Public/private keys on local machine:](#create-a-publicprivate-keys-on-local-machine)
- [Create an SSH key on Azure:](#create-an-ssh-key-on-azure)
- [Create a virtual machine:](#create-a-virtual-machine)
- [Connect local machine to VM:](#connect-local-machine-to-vm)
- [when deleting VM from resource group delete:](#when-deleting-vm-from-resource-group-delete)
- [connect Git to Github:](#connect-git-to-github)


### Vnet:
- VNet space(CIDR) block:
10.0.0.1/16 which will give 65,000 IP addresses(private).


<br>

### Create a virtual network:
- Create Vnet name: tech501-maram-2-subnet-vnet
- Create 2 subnets ; a public and private
    - public subnet : 10.0.2.0/24 ~ 256 IPs
    - Private subnet: 10.0.3.0/24 ~ 256 IPs
- paste your public .ssh key pair.(ensure private is kept secret).
- ARM (Azure resource manager), Azure API.
- to delete; go to resource group and delete vnet.
- Always double check before deleting. 

<br>

### Create a Public/private keys on local machine:
  - ssh-keygen -t rsa -b 2048 -f ~/onedrive/Documents/azurepractice/azure_key.
  - then upload public key on azure; on ssh key and create.

<br>

### Create an SSH key on Azure:
- Resource group: tech501
- Key pair name: tech501-maram-az-key
- Upload an existing key
- from bash go to ~/.ssh
  ```bash
  cat tech501-maram-az-key-pub
  ```
- copy all and paste on azure 
- Tages: Owner: Maram
- Create 


### Create a virtual machine:

- VM has NIC(network interface card) which the IP address will be associated with allocated IP from the pool of /24 CIDR.

- Name: tech501-maram-first-vm
- Region: UK South
- Security: standard
- Image (i.e. the OS that will go onto the disc): Ubuntu Pro 18.04 LTS Gen 2 [LTS means long term support for ~7 years]
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

<br>

### Connect local machine to VM:
- from vm select connect and choose Native ssh connect.
- paste the pathway of the private key.
  - ~/.ssh/ tech501-maram-az-key 
- use this on git terminal to connect to the VM on azure : ssh-copy-id -i ~/.ssh/id_rsa maram@192.168.1.244
- paste the address into git and type yes.
- exit to go back to local machine. 


<br>

### when deleting VM from resource group delete:

- Disk
- network interface
- security group
- Public IP 
- Actual VM

### connect Git to Github:
- cd to your repo 
  - cd onedrive/Documents/github/tech501-week1
- Run the following command:
```bash
git remote add origin https://github.com/mrmari9/tech501-week1-git
```
- git status
- git add .
- git commit -m""
- git push -u original main; first time you push must specify the branch.
  - files and folders and changes are pushed.
- history












