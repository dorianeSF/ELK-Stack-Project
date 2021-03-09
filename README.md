# ELK-Stack
## Automated ELK Stack Deployment

This repository is home to the files, images, and instructions used to configure the below network:

![Image of Elk Stack Diagram](Images/DorianeF_ELK-Stack_Diagram.png)

The successful ELK deployment from these files have been used and tested on Azure. If you would like to recreate the entire deployment of this network, you may do so. Otherwise, you may install an individual piece, such as metricbeat:

Ansible/metricbeat-playbook.yml

The document which you are reading contains the the following elements:
- A description of the network Topology
- Access Policies
- ELK Configuration
  - Beats in use
  - Machines that are monitored
- Instructiosn to use the Ansible Build


### Description of the Topology

The purpose of the configured network is to expose a load-balanced and carefully monitored DVWA (D*mn Vulnerable Web Application) instance.
The use of load balancing ensures a secure application by protecting against distributed denial-of-service (DDoS) attacks, while optimizing traffic through an even load distribution, improving user experience.
Load balancing protects the availability of a network. Using a jump-box in addition to a load balancer adds an additional layer of security by acting as a single point of entry when connecting to the internet.  
Our network is protected further by the use of an SSH Key when connecting to the jump-box server. Connecting to your jump-box through SSH provides a simple and secure access point to your server. 
Overall, these precautions decrease your surface attack area and protect your network's availability.

Integrating an ELK server assists users in easily monitoring vulnerable VMs for changes to the logs and system applications. As an analytics tool, ELK Stack aggregates data in a simple form. In addition, ELK stack allows analysts to collect logs from several machines into a single database and quickly execute complex searches.
- Filebeat is used to monitor the log files
- Metricbeat collects and records data regarding the metrics of a system or service.. 

Please see below for the configuration details of each machine:

| Name     	| Function          	| IP Address                               	| Operating System 	|
|----------	|-------------------	|------------------------------------------	|------------------	|
| Jump Box 	| Gateway           	| Public: 137.117.96.250 Private: 10.0.0.4 	| Linux            	|
| ELK-1    	| Monitor/Analytics 	| Public: 52.184.224.203 Private: 10.1.0.5 	| Linux            	|
| Web-1    	| Web server        	| Public: N/A Private: 10.0.0.7            	| Linux            	|
| Web-2    	| Web server        	| Public: N/A Private: 10.0.0.6            	| Linux            	|
| Web-3    	| Web server        	| Public: N/A Private: 10.0.0.8            	| Linux            	|

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the _____ machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- _TODO: Add whitelisted IP addresses_

Machines within the network can only be accessed by _____.
- _TODO: Which machine did you allow to access your ELK VM? What was its IP address?_

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes/No              | 10.0.0.1 10.0.0.2    |
|          |                     |                      |
|          |                     |                      |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _TODO: What is the main advantage of automating configuration with Ansible?_

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![TODO: Update the path with the name of your screenshot of docker ps output](Images/docker_ps_output.png)

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
SAMPLE URL:  [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables)
