## Automated Elastic Stack Deployment

The files in this repository were used to configure the network depicted below.

![Elk-stack-Simulation](/images/VNET.JPG)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the yaml playbook file may be used to install only certain pieces of it, such as Filebeat.

  - filebeat-playbook.yml.

This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly reliable and available, in addition to restricting any form of  destributed denial of service to the network.
It does this by shifting attack traffic from the corporate server to a public cloud provider. 

A jump box is a secure computer that all admins first connect to before launching any administrative task or use as an origination point to connect to other servers or untrusted environments. It also helps protect unauthorized access to the network by providing a controlled means.

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the files and system configuration.

- Filebeat is a lightweight shipper for forwarding and centralizing log data. Installed as an agent on your servers, Filebeat monitors the log files or locations that you specify, collects log events, and forwards them either to Elasticsearch or Logstash for indexing.

-Metricbeat is a lightweight shipper that you can install on your servers to periodically collect metrics from the operating system and from services running on the server. Metricbeat takes the metrics and statistics that it collects and ships them to the output that you specify, such as Elasticsearch or Logstash.

The configuration details of each machine may be found below.

| Name     | Function | IP Address | Operating System |
|----------|----------|------------|------------------|
| Jump Box | Gateway  | 10.0.0.4   | Linux            |
| Web 1    | Webserver| 10.0.0.5   | Linux            |
| Web 2    | Webserver| 10.0.0.6   | Linux            |
| Web 3    | Webserver| 10.0.0.7   | Linux            |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the Provisioning machine machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- _TODO: Add whitelisted IP addresses_

Machines within the network can only be accessed by _____.
- _TODO: Which machine did you allow to access your ELK VM? What was its IP address?_

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes                 | 75.87.171.148        |
|  Web1    | Yes                 |  10.0.0.4            |
|  Web2    | Yes                 |  10.0.0.5            |
|  Web3    | Yes                 |  10.0.0.6            |
|  ELK     | Yes                 |10.0.0.7/75.87.171.148|

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...

- One of the prominent advantages of Ansible also refers to the language in which it is written. Python is a human-readable language and serves as the basis for Ansible. It provides better facilities for getting up Ansible and running it due to the presence of Python libraries on the majority of Linux distributions by default.

- Ansible manages all the master-agent communications through Standard SSH or Paramiko module. The Paramiko module is a Python implementation of SSH2 and is crucial for managing nodes. Therefore, Ansible does not require any form of agents installed on remote systems for ensuring management. As a result, maintenance overheads and performance degradations reduce considerably by huge margins with Ansible.


The playbook implements the following tasks:
- Installs Docker
- Download image
- The managed nodes to target, using a pattern at least one task to execute.

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![Elk-stack-Simulation](/images/docker-ps-command.png2)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_

We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running?

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._
