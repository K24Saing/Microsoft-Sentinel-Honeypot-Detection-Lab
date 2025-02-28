# Microsoft-Sentinel-Honeypot-Detection-Lab

## Objective

The Microsoft Sentinel Honeypot Detection Home Lab project aimed to establish a real-world environment for detecting cyber threats on virtual machines using cloud infrastructure. By leaving machines vulnerable to an outside environment, you create honeypots in a network where you can analyze all the attacks that are targeting your home network. By using Microsoft Sentinel and Kusto Query Language, I'm also able to perform deep investigations on these events and configure systems accordingly, for continuous hardening of network and endpoints.

### Skills Learned

- Advanced understanding of SIEM and Azure concepts and practical application.
- Learned how to create virtual machines, resource groups, and networks through the cloud infrastructure.
- Explored the Microsoft Azure environment, analyzed incidents, and responded to security alerts as they happen.
- Understand the significance of exposed cyber threats on vulnerable systems.
- Able to assign incidents, update status, and close tickets through Microsoft Sentinel.
- Experience in using Kusto Query Language for deeper investigation of security events.
- Create watchlists and workbooks using Microsoft Sentinel
- Better understanding of network infrastructure.

### Tools Used

- Security Information and Event Management (SIEM) system for log ingestion and analysis // Microsoft Sentinel.
- Setting up virtual environment through cloud infrastructure (IaaS) // Microsoft Azure.
- Operating Systems of virtual machines // Windows 10 Home, ubuntu Linux.

### Steps
![Microsoft Honeypot](https://github.com/user-attachments/assets/17781ba0-6987-41d3-9fc3-4fa09880a9ea)

1. I created a virtual environment using Microsoft Azure consisting of a Windows Server 2019, Windows 10 Home, and Ubuntu Linux. Each virtual machine belonged to the same resource group and on the same virtual network.
<img src="![Microsoft Sentinel Lab (1) Created Virtual Environment](https://github.com/user-attachments/assets/c29fe5b8-d510-473f-bf58-dd7c74347f8f)" width="50%" height="50%">


   
2. I then created my own Log Analytics workspace for logs to be sent towards, and enabled continuous export for each PC to export their security alerts and recommendations to.
3. 
4. On the Windows 10 VM, I ensured that the firewall is off and I allowed all Inbound activity through the firewall, thus creating a honeypot for the PC. 
