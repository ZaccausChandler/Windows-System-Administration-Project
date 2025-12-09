# Windows System Administration Project 

Hands-on system administration and help desk labs built to simulate a real-world enterprise environment. This portfolio showcases my work with Active Directory, Group Policy, organizational structure, workstation management, and troubleshooting skills practiced through virtual machines.

##  Lab Environment

Domain Controller: Windows Server (Active Directory, DNS, Server Manager)

Client Workstations: Windows 10/11 (2 machines joined to the domain)

Virtualization Platform: (Hyper-V, VirtualBox, VMware – choose yours)

Tools Used: RSAT, Group Policy Management Console, PowerShell, CMD, Remote Desktop

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

##  Projects & Labs
### 1. Domain Controller Build & AD Configuration

Description:
Installed Windows Server, promoted it to a Domain Controller, configured DNS automatically through the AD DS role, and created a structured organizational layout for future users and workstations.

Key Tasks Performed:

Installed Active Directory Domain Services
 ![Image Alt]([image_url](https://github.com/ZaccausChandler/IT-Labs-Portfolio-VM/blob/3b0fe4884ea3eb79e7e40a0ba7e25d2df3bafc0c/Active%20Directory/Media/ADUC.png))
Created domain: yourdomain.local

Set up OUs for HR, IT, and Workstations

Verified DNS health and domain functionality

Connected two client VMs to the domain using System Properties

Screenshots:
(Insert your DC screenshots here)

### 2. User & Group Management

Description:
Created real-world organizational structure inside Active Directory to simulate enterprise-level user management.

Key Tasks:

Created users (e.g., Amanda in the HR OU)

Assigned roles with least privilege in mind

Managed password resets, account unlocks, and AD attributes

Organized computers into correct OUs

Screenshots:
(Insert user/group screenshots)

### 3. Group Policy Administration

Description:
Created multiple GPOs to enforce security and user restrictions. Applied them to specific OUs and tested via Group Policy Results.

GPO Examples Implemented:

Disable Task Manager

Disable Log Off option

Password complexity & lockout settings

Drive mapping (if you add this later)

Verification Methods:

gpresult /r on Desktop02

Group Policy Results Wizard

Force updates with gpupdate /force

Screenshots:
(Insert GPMC or gpresult screenshots)

## 4. RSAT Tools & Remote Administration

Description:
Used RSAT from a client PC to manage AD, GPO, Users, and Computers remotely — simulating a help desk technician managing domain resources.

Key Tasks:

Installed RSAT on a Windows 10/11 client

Managed users and GPOs without logging into the server

Performed remote desktop connections to the server

Tested permissions and policy application from the client side

Screenshots:
(Insert RSAT tools shots)

### 5. Help Desk Troubleshooting Simulations

Description:
Performed real-world troubleshooting scenarios within the lab environment.

Examples:

RPC server unavailable issue during GPO Results (troubleshooting DNS / services)

Joined and rejoined workstations to the domain

Verified network connectivity with ping, nslookup, ipconfig

Tested role-based access and restrictions

Screenshots:
(Add troubleshooting screenshots if available)

### 6. Imaging & Deployment

Description:
Created a system image using WDS to simulate enterprise workstation deployment.

Tasks Performed:

Booted into imaging tool

Captured full disk image

Restored image to another VM

Screenshots:
(Insert imaging screenshots later if you do this lab)

## Tools & Technologies

Windows Server / AD DS

Group Policy Management

RSAT

PowerShell

CMD

Server Manager

DHCP / DNS (as part of DC setup)

VirtualBox / VMware

Remote Desktop

Imaging Tools (Windows Deployment System)

Contact

LinkedIn: https://www.linkedin.com/in/zaccaus-chandler-b87891114/

Email: chandlerzaccaus@gmail.com
