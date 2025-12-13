# Windows System Administration Project 

Hands-on system administration and help desk labs built to simulate a real-world enterprise environment. This portfolio showcases my work with Active Directory, Group Policy, organizational structure, workstation management, and troubleshooting skills practiced through virtual machines.

##  Lab Environment

Domain Controller: Windows Server (Active Directory, DNS, Server Manager)

Client Workstations: DESKTOP01 & DESKTOP02 (2 VM's joined to the domain)

Virtualization Platform: VirtualBox

Tools Used: RSAT, Group Policy Management Console, PowerShell, CMD, 

Networking: Internal virtual network simulating a production environment

##  Core Skills Demonstrated

Active Directory installation & configuration

Creating and managing Users, Groups, and OUs

Applying & enforcing Group Policies

Remote administration via RSAT

Workstation domain joins

Organizational Unit design

GPO troubleshooting (gpupdate, gpresult, Resultant Set of Policy)

Basic help desk workflows and ticket-style problem solving

Permissions, security, and role-based access

Windows Deployment Services (Imaging)

##  Projects & Labs
### 1. Domain Controller Build & AD Configuration

Description:
Installed Windows Server, promoted it to a Domain Controller, configured DNS automatically through the AD DS role, and created a structured organizational layout for future users and workstations.

Key Tasks Performed:

Installed Active Directory Domain Services
![image alt](https://github.com/ZaccausChandler/IT-Labs-Portfolio-VM/blob/3b0fe4884ea3eb79e7e40a0ba7e25d2df3bafc0c/Active%20Directory/Media/ADUC.png)

Created domain: zccorp.local
![image alt](https://github.com/ZaccausChandler/IT-Labs-Portfolio-VM/blob/03bb642e6eea1c7aae2fe99896a65a686c7db35e/Networking/Media/ZCCORP%20DOMAIN.png)

Set up OUs for HR, IT, and Security

![image alt](https://github.com/ZaccausChandler/IT-Labs-Portfolio-VM/blob/3d0de4c7392b1becb68fbdcad3ff3c13597a9693/Active%20Directory/Media/AD%20GROUPS.png)


Connected two client VMs to the domain using System Properties
![image alt](https://github.com/ZaccausChandler/IT-Labs-Portfolio-VM/blob/2e8a342d396490ffc0ae25b464bbcedfcda6cebe/Active%20Directory/Media/DOMAIN%20COMPUTERS.png)

### 2. User & Group Management

Description:
Created real-world organizational structure inside Active Directory to simulate enterprise-level user management.

Key Tasks:

Created users (e.g. Helpdesk)

![image alt](https://github.com/ZaccausChandler/IT-Labs-Portfolio-VM/blob/03bb642e6eea1c7aae2fe99896a65a686c7db35e/Active%20Directory/Media/USER%20ACCOUNT%20PROFILE.png)

Assigned roles and memberships

![image alt](https://github.com/ZaccausChandler/IT-Labs-Portfolio-VM/blob/03bb642e6eea1c7aae2fe99896a65a686c7db35e/Active%20Directory/Media/AD%20Memberships.png)

Managed password resets, account unlocks, and AD attributes


### 3. Group Policy Administration

Description:
Created multiple GPOs to enforce security and user restrictions. Applied them to specific OUs and tested via Group Policy Results.

GPO Examples Implemented:

Disable Task Manager

![image alt](https://github.com/ZaccausChandler/IT-Labs-Portfolio-VM/blob/f0e2485e4c152c101447c2f819768878cd4ee53d/Group%20Policy/Media/Disable%20Task%20Manager.png)

Disable Change Password option

![image alt](https://github.com/ZaccausChandler/IT-Labs-Portfolio-VM/blob/f0e2485e4c152c101447c2f819768878cd4ee53d/Group%20Policy/Media/Disable%20Password.png)

Password complexity & lockout settings

![image alt](https://github.com/ZaccausChandler/IT-Labs-Portfolio-VM/blob/f0e2485e4c152c101447c2f819768878cd4ee53d/Group%20Policy/Media/GP%20SETTINGS.png)

Drive mapping 

![image alt](https://github.com/ZaccausChandler/IT-Labs-Portfolio-VM/blob/f0e2485e4c152c101447c2f819768878cd4ee53d/Drive%20Mapping/Media/DRIVE%20LOCATIONS.png)

Drive Map Locations(CMD)

![image alt](https://github.com/ZaccausChandler/IT-Labs-Portfolio-VM/blob/f0e2485e4c152c101447c2f819768878cd4ee53d/Drive%20Mapping/Media/MAPPED%20DRIVES%20CMD.png)

Verification Methods:

gpresult /r on Desktop02(Amanda)

![image alt](https://github.com/ZaccausChandler/IT-Labs-Portfolio-VM/blob/f0e2485e4c152c101447c2f819768878cd4ee53d/Group%20Policy/Media/GP%20RESULT%20TASK.png)

Group Policy Results Wizard

![image alt](https://github.com/ZaccausChandler/IT-Labs-Portfolio-VM/blob/f0e2485e4c152c101447c2f819768878cd4ee53d/Group%20Policy/Media/POLICY%20ENFORCED.png)

Force updates with gpupdate /force

![image alt](https://github.com/ZaccausChandler/IT-Labs-Portfolio-VM/blob/f0e2485e4c152c101447c2f819768878cd4ee53d/Group%20Policy/Media/GP%20CMD%20PROMPT.png)

Task Manager Disabled on Desktop02(Amanda)

![image alt](https://github.com/ZaccausChandler/IT-Labs-Portfolio-VM/blob/9143d3202fedbeb7a540a9915f6916ab08e4999c/Group%20Policy/DESK2%20TASK%20FAIL.png)

![image alt](https://github.com/ZaccausChandler/IT-Labs-Portfolio-VM/blob/9143d3202fedbeb7a540a9915f6916ab08e4999c/Group%20Policy/Media/DSKTP2%20TASK%20REMOVAL.png)

## 4. RSAT Tools & Remote Administration

Description:
Used RSAT from DESKTOP01(Helpdesk user) to manage AD, GPO, Users, and Computers remotely — simulating a help desk technician managing domain resources.

Key Tasks:

Installed RSAT on a Windows 10/11 client (DESKTOP01) using server manager

![image alt](https://github.com/ZaccausChandler/Windows-System-Administration-Project/blob/5b8e70d37e2034a2c32f54fe03c08ae1ad4000a9/Networking/Media/RSAT%20TOOLS.png)


Managed users and GPOs without logging into the server

![image alt](https://github.com/ZaccausChandler/Windows-System-Administration-Project/blob/5b8e70d37e2034a2c32f54fe03c08ae1ad4000a9/Networking/Media/DESKTOP01%20AD.png)

Performed remote desktop connections to the server

![image alt]()

Tested permissions and policy application from the client side

(See previous screenshot where DESKTOP02 could not access Task Manager)

### 5. Help Desk Troubleshooting Simulations

Description:
Performed real-world troubleshooting scenarios within the lab environment.

Examples:

RPC server unavailable issue during GPO Results (troubleshooting DNS / services)

Joined workstations to the domain

![image alt](https://github.com/ZaccausChandler/Windows-System-Administration-Project/blob/c1cfbb32e9e0860b6172506d3e9dee344948b6b2/Networking/Media/DC%20IPv4%20CONFIG.png)

Verified network connectivity with ping, ipconfig

Ping client Domain Server
![image alt](https://github.com/ZaccausChandler/Windows-System-Administration-Project/blob/c1cfbb32e9e0860b6172506d3e9dee344948b6b2/Networking/Media/CLIENT%20PING%20DC.png)

Reset user "Amanda" account password using DESKTOP01(Helpdesk)

![image alt]()


### 6. Imaging & Deployment

Description:
Created a system image using WDS to simulate enterprise workstation deployment.

Tasks Performed:

Booted into imaging tool

Captured full disk image

Restored image to another VM



## Tools & Technologies

Windows Server / AD DS

Group Policy Management

RSAT

PowerShell

CMD

Server Manager

DHCP / DNS (as part of DC setup)

VirtualBox / VMware


Imaging Tools (Windows Deployment System)

Contact

LinkedIn: https://www.linkedin.com/in/zaccaus-chandler-b87891114/

Email: chandlerzaccaus@gmail.com
