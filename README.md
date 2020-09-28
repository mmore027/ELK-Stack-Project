## Automated ELK Stack Deployment

This network serves to create and deploy an Elk Stack Server and configure 2 Red Team VMS within an Azure Virtual Network to monitor the web server running DVWA.

![Elk Stack Network Diagram](https://user-images.githubusercontent.com/65696057/94222445-38d71c00-fea2-11ea-8a45-5c6e6871df2f.jpg)

filebeat-playbook.yml

This document contains the following details:
- Description of the Topology
- Access Policies
- Elk Configuration
  - Beats in Use
  - Machines being monitored
- How to use the Ansible Build

### Description of the Topology
The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the Damn Vulnerable Web Application.
Load balancing ensures that the application will be highly secure, in addition to restricting unauthroized access.
The load balancer protects the distribution of the traffic on a network. The advantage of the jumpbox is a secure machine where admins first connect to before connecting to other machines/servers. 

Integratating an ELK Server allows user to easily monitor the vulnerable VMs for changes to the system.
Filebeat watches for log files and metricbeat records and collects the systems metrics.

The configuration details of each machine may be found below.

| Name       | Function  | IP Address | Operating System |
|------------|-----------|------------|------------------|
| Jump Box   | Gateway   | 10.0.0.1   | Linux            |
| Red-Team1  | Webserver | 10.10.0.10 | Linux            |
| Red-Team2  | Webserver | 10.10.0.11 | Linux            |
| Elk Server | Elk       | 10.1.0.4   | Linux            |

### Access Policies

The machines on the internal network are not exposed to the public internet.

Only the Jump Box machine can accept connections from the Internet. Access to this machine is only allowed from the following IP Addresses.

Machines within the network can only be accessed by an SSH key.

A summary of the access policies in place can be found in the table below.

| Name       | Publicly Accessible | Allowed IP Addresses |
|------------|---------------------|----------------------|
| Jump Box   | No              | 10.0.0.1 10.0.0.2        |
| Elk Server | No              | 10.1.0.4                 |


### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because the process was automated and configured rapidly.

The playbook implements the following tasks:
- Installs docker
- Configures server
- Launches container

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- Red-Team-Web-VM-1
- Red-Team-Web-VM-2

We have installed the following beat on each system:
- filebeat
- metricbeat
These Beats allow us to collect the following information from each machine:
- File beat will collect any suspicious activity on the machine while metricbeat will monitor and record the collected vulnerabilities/potential changes to the system.

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the filebeat-config.yml file to the container.
- Update the filebeat-playbook file to include metricbeat.
- Run the playbook, and navigate to host machine to check that the installation worked as expected.

