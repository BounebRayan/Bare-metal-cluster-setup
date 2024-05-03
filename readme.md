# Kubernetes Cluster Setup with Vagrant and Ansible

![Kubernetes Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/3/39/Kubernetes_logo_without_workmark.svg/120px-Kubernetes_logo_without_workmark.svg.png) ![Vagrant Logo](https://upload.wikimedia.org/wikipedia/commons/8/87/Vagrant.png) ![Ansible Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/2/24/Ansible_logo.svg/120px-Ansible_logo.svg.png)

This repository provides all the necessary files to effortlessly set up and configure a Kubernetes cluster using Vagrant and Ansible. Leveraging VirtualBox as the hypervisor, this solution ensures seamless virtual machine creation.

## Prerequisites

Before diving in, make sure your system meets the following requirements:

- [VirtualBox](https://www.virtualbox.org/): Version 6.1 is recommended, as newer versions might not be fully supported by Ansible at the time of this work.
- [Vagrant](https://www.vagrantup.com/): Use Vagrant 2.2.16 for compatibility.
- [Ansible](https://www.ansible.com/): Ensure you have Ansible Core 2.16.5 installed.

If you're utilizing WSL, refer to [this guide](https://developer.hashicorp.com/vagrant/docs/other/wsl) for additional setup instructions.

## Installation

1. Clone this repository to your local machine:

git clone https://github.com/BounebRayan/cluster-setup.git

2. Navigate to the cloned repository and run Vagrant to create and provision the virtual machines:
   
vagrant up

This command will create the VMs according to the configuration specified in the Vagrantfile and provision them using Ansible playbooks.

3. Once the provisioning is complete, you can access the Kubernetes cluster.

## Usage

- To start the VMs:
  vagrant up

- To SSH into a specific VM:
  vagrant ssh <vm-name>

- To stop the VMs:
  vagrant halt or vagrant suspend depending on your usecase

- To destroy the VMs:
  vagrant destroy

## Customization

You can customize the Kubernetes cluster configuration by modifying the parameters in the `Vagrantfile` and the Ansible playbooks located in the `kubernetes-setup` directory.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

