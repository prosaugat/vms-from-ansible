# vms-from-ansible
This GitHub repository contains two Ansible playbooks designed to streamline the process of creating multiple virtual machines (VMs) on vCenter/vSphere environments simultaneously. With these playbooks, users can automate the VM creation process, saving time and effort.

Playbook 1: create_vm.yml
This playbook is responsible for creating a single VM using the `vmware_guest` module. The playbook takes input parameters such as vCenter server credentials, datacenter name, datastore name, network details, VM specifications, and more. Users need to customize the template name, IP addresses, and other specific parameters according to their vSphere environment.

Playbook 2: deploy_vms.yml
The second playbook is a high-level orchestration playbook that leverages the `create_vm.yml` playbook to deploy multiple VMs concurrently. Users can define VM names and their respective IP addresses in the `vm_specs` variable within this playbook. The playbook uses the `include_tasks` module to execute the `create_vm.yml` tasks in a loop for each VM specification.

By using these playbooks, users can create a batch of VMs with ease, providing a scalable and efficient solution for managing VM deployments in vCenter/vSphere environments. Feel free to customize the playbooks and contribute to the repository, making it even more powerful and adaptable to various use cases.
