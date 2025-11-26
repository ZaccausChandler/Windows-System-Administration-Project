Networking \& Domain Configuration Lab



This lab demonstrates how I configured a Windows Server VM as a domain controller, installed necessary management tools, and connected two separate client VMs to the domain. It also includes verification steps using networking commands, adapter configuration, and user validation.



Environment Setup



1\. Installed Server Manager Inside a Windows Server VM

\- Created a Windows Server virtual machine.

\- Installed Server Manager to manage roles and features.

\- Enabled the necessary components for domain services.



2\. Installed RSAT Tools

Using Server Manager:

\- Installed Remote Server Administration Tools (RSAT), including:

&nbsp; - Active Directory Domain Services tools  

&nbsp; - DNS Management tools  

&nbsp; - Group Policy Management tools



These tools allowed me to administer the domain and DNS from the server VM.



3\. Installed and Configured DNS

\- Added the DNS Server role on the domain controller.

\- Verified the Forward Lookup Zone was created for the domain.

\- Confirmed DNS service was running inside DNS Manager.



Domain Integration



4\. Joined Two Client VMs to the Domain

\- Created two separate Windows client VMs.

\- Set each computer’s DNS server address to the "ZCCORP.LOCAL" IP.

\- Joined both machines to the domain through system properties  



\- Restarted each VM to complete the domain join.



Verification Steps



5\. Verified Network Connectivity Using Ping

From each client VM: Ping ZCCORP.LOCAL or PING 10.1.10.2



\- Confirmed both clients could resolve and communicate with the domain controller.



6\. Confirmed Users With Command Prompt

On each client VM: Net User



\- Verified domain users appeared, confirming successful domain membership and replication.



7\. Checked Network Adapter Settings Through CMD

Ran: IPCONFIG /ALL



Confirmed:

\- Correct IPv4 address  

\- DNS pointing to the domain controller  

\- Network interface active and properly bound



VirtualBox Network Configuration



8\. Ensured Proper NIC Settings for Client VMs

Inside VirtualBox:

\- Set network adapter for each client VM to:

&nbsp; Host-Only Adapter

&nbsp; 

This allowed the clients to communicate exclusively with the server VM for domain operations while maintaining a controlled virtual network environment.



9\. DNS Forward Lookup Zone Verification

After installing the DNS Server role, I verified the Forward Lookup Zone to ensure proper name resolution inside the domain.



Steps performed:

\- Opened DNS Manager using `dnsmgmt.msc`.

\- Expanded Forward Lookup Zones.

\- Confirmed the domain zone `zccorp.local` was created when the domain controller was promoted.

\- Verified required DNS records:

&nbsp; - SOA (Start of Authority)

&nbsp; - NS (Name Server)

&nbsp; - A records for the domain controller and clients

\- Ensured the DNS service was running and resolving hostnames correctly.





This lab demonstrates practical experience with:

\- Installing and configuring Server Manager, RSAT, and DNS  

\- Creating a functional domain controller  

\- Joining Windows clients to a domain  

\- Verifying domain connectivity using ping, net user, and ipconfig  

\- Properly configuring VirtualBox network adapters for isolated lab networking  



Networking\\Media\\Server Manager.png

Networking\\Media\\DC IPv4 CONFIG.png

Networking\\Media\\CLIENT PING DC.png

Networking\\Media\\IPCONFIG ALL DC.png

Networking\\Media\\NET USERS.png

Networking\\Media\\NETWORK ADAPTER SETTINGS.png

Networking\\Media\\VIRTUAL BOX NETWORK SETTINGS.png

Networking\\Media\\DNS FORWARD LOOKUP.png



