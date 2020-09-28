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
An ELK server consists of three open-source tools called Elasticsearch, Logstash, & Kibana. Elasticsearch is the database used for storing logs, Logstash collects the logs from the machines, and Kibana provides charts and graphs so analysts are able to review the data with ease.

Load balancing ensures that the application will be highly secure, in addition to restricting unauthroized access.
The load balancer protects the... the advantage of the jumpbox is ,,,

Integratating an ELK Server allows user to easily monitor the vulnerable VMs for changes to the ...
Filebeat watches for...
mtricbeat records

The configuration details of each machine may be found below.

| Name     | Function | IP Address | Operating System |
|----------|----------|------------|------------------|
| Jump Box | Gateway  | 10.0.0.1   | Linux            |
| TODO     |          |            |                  |
| TODO     |          |            |                  |
| TODO     |          |            |                  |
