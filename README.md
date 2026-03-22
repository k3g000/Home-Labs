 Help Desk & Active Directory 
 
 Home Lab By: Kegan Tripp
 
 Project Objective: The goal of this lab was to build a functional, enterprise-grade network environment from scratch. 
 
 This allowed me to practice core Help Desk skills such as User Provisioning, Group Policy Management, and Network Troubleshooting in a controlled, virtualized setting. 
 
 Tools & Technologies:
 
 Used Hypervisor: Oracle VirtualBox 
 
 Directory Services: Windows Server 2022 (Active Directory Domain Services) 
 
 Endpoint: Windows 10 
 
 EnterpriseScripting: PowerShell (for bulk user creation)
 
 Networking: Internal Virtual Switching (NAT & Private Network) Lab Architecture 
 
 Domain Controller (DC-01): Running Windows Server 2022. Acts as the "Brain" of the network, handling DNS, DHCP, and Active Directory.
 
 Client Workstation (CL-01): Running Windows 10. Joined to the KeganTech.local domain to simulate a corporate employee's computer. 
 
 Key Milestones & Skills Demonstrated:
 
 1. Active Directory Setup & User Provisioning Successfully promoted the server to a Domain Controller.
 
 2. Created a logical Organizational Unit (OU) structure (e.g., IT, Accounting, Sales).
 
 Challenge: I needed to add 100 users quickly.
 
 Solution:
 
 1. I wrote a PowerShell script to pull names from a .csv file and automatically generate accounts with default passwords.
 
 2. Group Policy Objects (GPO) Implemented a "Security Policy" that prevents regular users from accessing the Command Prompt or Control Panel. Created a "Login Banner" that displays a legal warning whenever a user logs in.

3. Troubleshooting Domain Connectivity Problem: The Windows 10 Client could not find the Domain Controller during the "Join Domain" process.
 
 Diagnostic: Used ping and nslookup to find that the Client was looking at Google’s DNS ($8.8.8.8$) instead of the Server’s IP.
 
 Resolution: Manually configured the Client’s IPv4 settings to point to the Server as the Primary DNS. 
 
 Result: Joined successfully. Learning Outcomes Through this lab, 
 
 I gained hands-on experience that mirrors the daily tickets handled by a Subject Matter Expert or Support Analyst:Managing the "User Lifecycle" (Joiners, Movers, Leavers). Understanding how DNS is the backbone of a corporate network. Documenting technical processes for both internal teams and end-users.# Home-Labs
