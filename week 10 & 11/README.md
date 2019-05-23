# Week 10 & 11 - Honeypot

Time spent: 9 hours spent in total

> Objective: Setup a honeypot and provide a working demonstration of its features.

## Overview & Setup:

A honeypot is a computer security mechanism set to detect, deflect, or, in some manner, counteract attempts at unauthorized use of information systems. Generally, a honeypot consists of data (for example, in a network site) that appears to be a legitimate part of the site, but is actually isolated and monitored, and that seems to contain information or a resource of value to attackers, who are then blocked. This is similar to police sting operations, colloquially known as "baiting" a suspect.

- MileStone 1: 
	- Create a VM instance for mhn-admin with the following specs:
		- Ubuntu 14.04 (Trusty)
		- HTTP and HTTPS traffic allowed for ports 80 and 443 respectively  
		![](https://i.ibb.co/8NXV3cy/Screen-Shot-2019-05-22-at-3-42-53-PM.png)
		- Open TCP ports 3000 and 10000 in the Firewall  
		![](https://i.ibb.co/YjkXPpg/Screen-Shot-2019-05-22-at-3-45-20-PM.png)
- MileStone 2:
	- Gain SSH access to the VM instance
	- Update repositories and install git 
	- Clone the mhn repo from ThreatStream project
	- Execute the install.sh script  
	![](https://i.ibb.co/Y2xZQKT/Screen-Shot-2019-05-22-at-3-48-13-PM.png)
- MileStone 3:
	- Create a VM instance for mhn-honeypot with the following specs:
		- Ubuntu 14.04 (Trusty)
		- HTTP and HTTPS traffic allowed for ports 80 and 443 respectively  
		![](https://i.ibb.co/kM7Ngvs/Screen-Shot-2019-05-22-at-3-54-57-PM.png)
		- Open all ports in the Firewall  
		![](https://i.ibb.co/QHkgyCZ/Screen-Shot-2019-05-22-at-3-56-28-PM.png)
- MileStone 4:
	- Log in to the honeypot admin application and generate the deply script from Deploy tab  
	![](https://i.ibb.co/238Pdkq/Screen-Shot-2019-05-22-at-4-38-38-PM.png)
	- Paste the deply command into the SSH terminal of honeypot VM  
- MileStone 5:
	- Boot into Kali Linux VM and run the nmap program against Honeypot VM public IP  
	![](https://i.ibb.co/kKjG1Bx/Screen-Shot-2019-05-22-at-7-11-12-PM.png)
	- Wait for attacks to show up in the admin sensors dashboard

## Unresolved Questions:
- I couldn't get any attacks to show up on the mhn-admin console, no matter how many times I've attacked it.
- I've tried troubleshooting the VMs, by checking whether all the necessary services are up and running, and all the ports required open by them are added in the firewall rules.
- I tore down the entire setup on GCP and tried hosting it on AWS EC2 instead, but to no avail. 
- Any feedback would be appreciated.

### Resources
- [Honeypot](https://en.wikipedia.org/wiki/Honeypot_(computing))  

Images hosted on [ImageBB](https://imgbb.com)

### License

	Copyright [2019] [Sai Kumar Juguru]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
