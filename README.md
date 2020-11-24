# ACI Ansible Guide

Ansible is an increasingly popular tool for network automation, it allows engineers to define playbooks which carry out tasks you are looking to automate by interacting with a device or controller through the CLI or API. It is particularly popular in data centre and cloud environments. In this short exercise we're going to show how Ansible can be used with Cisco's data centre networking solution ACI to look at building the beginngings of an Infrastructure as Code solution with Ansible. 

It should be said that Ansible is just one automation tool that can be used, you might have also heard of the tool Terraform which we also have a guide to look at getting started automating ACI using and can be found [here](https://github.com/sttrayno/Terraform-Lab-Guide).

Today in ACI, there are over 100 modules in Ansible for working with ACI which will allow you to work quite extensively with both ACI and MSO (Multi service orchestrator). A full list can be found [here](https://docs.ansible.com/ansible/latest/modules/list_of_network_modules.html#network-modules) which is constantly being added to. Today we'll look at a few of them and show you how you can get started.

## Prerequsites

For these exercises we'll first need a machine with Ansible installed so that we can run our playbooks.

A popular way of running Ansible is through Ansible Tower, commercial offering intended for teams looking to operationalise Ansible. Tower provides many features ontop of Ansible including a frontend, RBAC, a lot of out the box integrations and provides reporting, a GUI and a REST API. Organisations looking to operationalise Ansible may use this for the advantages mentioned. However for someone learning we can drive our playbooks from the CLI using the classic Ansible packages.

There are are multiple guides for installing Ansible that can be found from the Ansible documentation, it's probably best to start [here](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) for your platform for the most up to date walkthrough. Please note that the playbooks in this exercise have not yet been adapted to the newest version of Ansible 2.10 and will need 2.9 to run.

To test Ansible is installed and configured correctly simply run the command `Ansible --version` from your terminal you should see an output like below. 

![](./images/ansible-version.png)

To run these exercises you will need an instance of ACI. [dCloud](dcloud.cisco.com) has a couple of instances of ACI that you can reserve and use in this lab aswell as the DevNet sandbox. We'll be using the ["Cisco ACI Simulator 4.2"](https://devnetsandbox.cisco.com/RM/Topology) and running our Ansible playbooks from the DevBox included in this reservation. This works well for this exercise as it has Ansible 2.9 preinstalled which is what our exercises are based on.

## Exercise 1 - Running your first playbook

### The inventory file

Most of the time when working with Ansible, you will need an inventory file in order that Ansible knows the APIC it is going to manage. In this lab we have a sample inventory file for the DevNet ACI 4.2 sandbox which we will be using. You can see how it is laid out below.

```yaml
[apic:vars]
username=admin
password=C1sco12345
ansible_python_interpreter="/usr/bin/env python"

[apic]
10.10.20.14
```

If your environment is different you can edit the file to suit your setup. It can be found under `inventory/host.yaml`. This file is specifically wrote for those using the DevNet sandbox.

### The playbooks

### The variables

### Running a playbook

### A few more...


