

 ## Automated ELK Stack Deployment
The files in this repository were used to configure the network depicted below.
![TODO Update the path with the name of your diagram](topology.png)
These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the _____ file may be used to install only certain pieces of it, such as Filebeat.
  see playbook.yml. for the DVWA and ELK playbook builds. 
This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build
### Description of the Topology
The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the Damn Vulnerable Web Application.
Load balancing ensures that the application will be highly redundant, in addition to restricting  unauthorized accessing to the network.
- What aspect of security do load balancers protect? What is the advantage of a jump box? it allows connectivity into the vitual network from external sources and obfuscates internal machines by allowing connectivity via private addresses_
Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the __container___ and system _logs____.
- What does Filebeat watch for?_watch system logs
- What does Metricbeat record?_watches the ELK logs
The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.
| Name     | Function | IP Address | Operating System |
|----------|----------|------------|------------------|
| Jump Box | Gateway  | 10.0.1.5   | Linux            |
| DVWA1-VM | 10.0.1.5 | 10.0.1.2   | Linux            |                  
| DVWA2-VM | 10.0.1.5 | 10.0.1.3   | Linux            |                  
| DVWA3-VM | 10.0.1.5 | 10.O.1.4   | Linux            |
  ELK-VM   | 10.0.1.5 | 10.1.1.2   | LInux           
### Access Policies
The machines on the internal network are not exposed to the public Internet. 
Only the _jumpbox____ machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- _TODO: Add whitelisted IP addresses_
Machines within the network can only be accessed by _____.
- _TODO: Which machine did you allow to access your ELK VM? What was its IP address?_
A summary of the access policies in place can be found in the table below.
| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|-------------------|----------------------|
| Jump Box | Yes                 | 10.0.1.2 10.0.1.3    |
|          |                     | 10.0.1.4             |
|          |                     |                      |
### Elk Configuration
Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
:What is the main advantage of automating configuration with Ansible?_it reduces the human error especially at scale and makes the job essier and faster. 
The playbook implements the following tasks:
- ... In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...ssh to jumpbox
- ...install docker.io
- ...pull Ansible container 
- ...build and run ELK playbook
- ...configure security rules to allow inbound ports 9200,5601
Collapse




