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

![Microsoft Honeypot](https://github.com/user-attachments/assets/17781ba0-6987-41d3-9fc3-4fa09880a9ea)

### Steps
1. I created a virtual environment using Microsoft Azure consisting of a Windows Server 2019, Windows 10 Home, and Ubuntu Linux. Each virtual machine belonged to the same resource group and on the same virtual network. <br>
<br> ![Microsoft Sentinel Lab (1) Created Virtual Environment](https://github.com/user-attachments/assets/f922134b-6772-4230-ad28-2f3a0653932e)
2. I then created my own Log Analytics workspace for logs to be sent towards, and enabled continuous export for each PC to export their security alerts and recommendations. <br>
<br> ![Microsoft Sentinel Lab (10) Enable Microsoft Continuous Logs](https://github.com/user-attachments/assets/c2abd617-2fe3-41ca-9ef9-84718a85500f)
3. On the Windows 10 VM, I ensured that the Microsoft Defender Firewall was off and I allowed all Inbound activity through the firewall, thus creating a honeypot for the PC. I also allowed all activity for the Linux firewall as well. <br>
4. As soon as I had exposed the network firewall, I immediately noticed attempts of brute force towards my honeypot devices. This revealed a lot to me about the quickness of network attacks when leaving devices vulnerable over the network without any protection.
5. I review the logs of both Linux and Windows 10 Event Viewer, to prove that there were attempts of brute force towards my device. Sure enough, there were many Audit Logs that showed up. <br>
<br> ![Microsoft Sentinel Lab (7) Failed Linux Login Attempts](https://github.com/user-attachments/assets/77e7b1aa-8b6d-4f54-ba77-c98729ea9310) <br>
<br> ![Microsoft Sentinel Lab (6) Event Viewer](https://github.com/user-attachments/assets/b1391696-41bf-40b6-b32d-99fec64ed4e2) <br>
6. I created a watchlist for various geoIPs, to discover the landscape and origin of attacks by geography. I connected this watchlist to a workbook to display the results visually on a map. <br>
<br> ![Microsoft Sentinel Lab (14) Workbook Json Codes](https://github.com/user-attachments/assets/784d21bb-6b5d-4368-b19b-6452ac82e873) <br>
<br> ![Microsoft Sentinel Lab (15) Workbook Json Codes Results](https://github.com/user-attachments/assets/809a4406-c586-4c6e-9d83-4719f0b5e8ee) <br>
7. I navigated to Sentinel to investigate any incidents related to this activity, and I investigated one incident of brute force activity in Sentinel. I assigned the incident to myself, and remediated it by disabling the Allow Any Inbound rules for the target machine. I closed the ticket and provided a description of the remediation. <br>
![Microsoft Sentinel Lab (16) Incidents](https://github.com/user-attachments/assets/f90bff53-b6e8-4ce1-83c8-29b81c8769ab) <br>
<br> ![Microsoft Sentinel Lab (17) Closed Tickets](https://github.com/user-attachments/assets/6a6c39e0-31aa-4cfc-bbbc-10235608c10e) <br>
8. I had left the Windows 10 Honeypot exposed for 24 hours, and logged back into Sentinel to observe the total amount of incidents. Sentinel generated about 32 events towards the honeypot. 
![Microsoft Sentinel Lab (20) 24 Hour Incidents](https://github.com/user-attachments/assets/fd3ffa1a-9842-43d7-9688-80d63e7c9a61)
9. I experimented with KQL by querying certain Syslog Tables, AuditLog Tables, and performed analysis on the events provided by Microsoft Sentinel. <br>
<br> ![Microsoft Sentinel Lab (13) Audit Logs Telemetery](https://github.com/user-attachments/assets/eda00dd0-23bc-4c63-980a-1a3ec0e5c4fa) <br>
<br> ![Microsoft Sentinel Lab (12) Syslog Generated for Linux](https://github.com/user-attachments/assets/e5f61c0f-7f93-4167-982c-5140f5aa4974) <br> 
10. I also experimented with the different guidelines and policies that you can implement in your Sentinel environment, for example the NIST 800-53 standard, to analyze the gaps and compliance of your Azure environment. <br>
<br> ![Microsoft Sentinel Lab (19) Enable NIST compliance](https://github.com/user-attachments/assets/75ad210f-65e2-4dcd-aedb-832366fd03d0)







