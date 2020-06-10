# ACI Ansible Guide

Ansible is an increasingly popular tool for network automation, 

Today in ACI, there are over 100 modules in Ansible for working with ACI which will allow you to work quite extensively with both ACI and MSO (Multi service orchestrator). A full list can be found [here](https://docs.ansible.com/ansible/latest/modules/list_of_network_modules.html#network-modules)

## Prerequsites

For these exercises we'll also need a machine with Ansible

A popular way of running Ansible is through Ansible Tower which provides a frontend, this has a lot of out the box integrations and provides reporting, a GUI and REST API ontop of the Ansible functionality. Organisations looking to operationalise Ansible may use this for the advantages mentioned. However for someone learning we can drive our playbooks from the CLI using the classic Ansible packages.

There are are multiple guides for isntalling Ansible that can be found from the Ansible documentation, it's probably best to start [here](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) for your platform for the most up to date walkthrough.

To test Ansible is installed and configured correctly simply run the command `Ansible` from your terminal you should see an output like below. If you don't and get an error such as an unrecognised command or similar you should refer back to the documentation.

To run these exercises you will need an instance of ACI. [dCloud](dcloud.cisco.com) has a couple of instances of ACI that you can reserve and use in this lab. We'll be using the ["Cisco ACI 4.1 Automation v1" demo](https://dcloud2.cisco.com/demo/aci-4-1-automation-v1). Alternatively you can also use your own instance of ACI if you have one available or use the DevNet sandbox. The only drawback of using the sandbox is you cannot get direct API access to the ACI sim and must go through an RDP client to get access, which makes getting started a bit more convoluted, but feel free to use the sandbox if you'd prefer.

## Exercise 1
