
![Awesome ReadME](https://i.ibb.co/Km4c4wF/Untitled.png)

# Bare Metal Kubernetes Cluster Setup

This repository provides all the necessary files to effortlessly spin up and configure a Kubernetes cluster using Vagrant and Ansible. Leveraging VirtualBox as the hypervisor, this solution ensures seamless virtual machine creation.

## Getting Started

These instructions will give you a kubernetes cluster up and running on
your machine for development and testing purposes.

### Prerequisites

Before diving in, make sure your system meets the following requirements:

- [VirtualBox](https://www.virtualbox.org/): Version 6.1 is recommended, as newer versions might not be fully supported by Ansible at the time of this work.
- [Vagrant](https://www.vagrantup.com/): Use Vagrant 2.2.16 for compatibility.
- [Ansible](https://www.ansible.com/): Ensure you have Ansible Core 2.16.5 installed.

If you're utilizing WSL, refer to [this guide](https://developer.hashicorp.com/vagrant/docs/other/wsl) for additional setup instructions.

### Installing

You'll first need to clone the repository

    git clone https://github.com/BounebRayan/Bare-metal-cluster-setup.git

Navigate to the cloned repository and run 

    vagrant up

This command will create the VMs according to the configuration specified in the Vagrantfile and provision them using the Ansible playbooks.
## Usage

To ssh into a specific VM

    vagrant ssh <vm-name>

For WSL users, If you incounter issues while trying to ssh try

    vagrant plugin install virtualbox_WSL2
and

    chmod 600 the private_key file 

P.S: The last command requires WSL to be mounted with metadata mount option.

### Stoping the cluster:
Depending on your usecase you need to run 

     vagrant halt # shuts down the running machines
     vagrant suspend # hibernate the running machines
### Deleting the cluster:
If you want to delete the cluster all together do

    vagrant destroy

## Deployment

Deploying and exposing your application in a similar cluster may require additional configurations, such as setting up port forwarding rules. 
You can refer to the setup in this [application repository](https://github.com/BounebRayan/Devops-To-do-app) for detailed instructions.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.
