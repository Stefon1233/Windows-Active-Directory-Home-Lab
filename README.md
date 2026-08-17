# Windows Active Directory Home Lab

## Overview

This project documents the deployment and administration of a Windows Active Directory domain in a virtualized home lab environment. The lab simulates common tasks performed by IT Support, Help Desk, and junior System Administrators.

## Tools & Technologies

- Oracle VirtualBox
- Windows Server 2022
- Windows 10
- Active Directory Domain Services (AD DS)
- DNS
- DHCP
- Group Policy
- PowerShell
- Windows File Sharing

## Lab Environment

- **Domain:** STEFONLAB
- **Domain Controller:** Windows Server 2022
- **Client Workstations:** Windows 10
- **Virtualization:** Oracle VirtualBox

---

# Lab Setup

## 1. Downloaded Windows Installation Media

Downloaded the Windows Server 2022 and Windows 10 installation media required to create the virtual lab environment.

The Windows Server virtual machine was used as the domain controller, while Windows 10 virtual machines were used as domain-joined client workstations.

<img width="847" height="685" alt="Windows Server 2022 download" src="https://github.com/user-attachments/assets/e4b87016-b370-4fd3-8cd1-6a3491ad1313" />

## 2. Created Virtual Machines

Created Windows Server 2022 and Windows 10 virtual machines in VirtualBox and allocated the required CPU, memory, storage, and network resources.

## 3. Configured Windows Server 2022

Installed Windows Server 2022 and configured the server for use as the domain controller.

## 4. Installed Active Directory Domain Services

Installed the Active Directory Domain Services (AD DS) server role and promoted the Windows Server system to a domain controller.

## 5. Created the Active Directory Domain

Configured the Active Directory domain:

**Domain:** `STEFONLAB`

## 6. Created Organizational Units

Created Organizational Units (OUs) to organize users, computers, and departments within Active Directory.

Departments included:

- IT
- Human Resources
- Finance
- Sales

## 7. Created User Accounts

Created 20 Active Directory user accounts and organized users into their appropriate departmental OUs.

A standardized username convention was used:

`first initial + last name`

## 8. Configured Security Groups

Created department and role-based security groups and assigned users to the appropriate groups.

## 9. Configured DNS

Configured DNS services, including forward and reverse lookup zones and PTR records.

## 10. Configured DHCP

Configured Windows Server DHCP to automatically provide network configuration to client systems.

## 11. Joined Windows 10 Clients to the Domain

Joined Windows 10 workstations to the Active Directory domain and verified successful domain authentication.

Example workstations included:

- `WS-HR-01`
- `WS-SALES-01`

## 12. Configured Group Policy

Created and applied Group Policy Objects (GPOs) to manage user and workstation settings.

Policies included:

- Password Policy
- Desktop Wallpaper
- Disable Control Panel
- Disable USB Storage
- Disable Command Prompt
- Disable Registry Editor
- 10-Minute Screen Lock
- Chrome Homepage

## 13. Configured File Shares and Permissions

Created departmental network shares for:

- HR
- Finance
- IT
- Public

Configured access permissions and tested access from domain-joined Windows 10 clients.

## 14. Tested and Troubleshot the Environment

Verified:

- Domain authentication
- User account access
- Group membership
- DNS resolution
- DHCP configuration
- Group Policy application
- Network share permissions
- Domain client connectivity

---

# Skills Demonstrated

- Windows Server 2022 Administration
- Active Directory Domain Services
- Active Directory Users and Computers
- User and Group Management
- Organizational Units
- Group Policy
- DNS
- DHCP
- Windows 10 Domain Administration
- File Sharing and NTFS Permissions
- Identity and Access Management
- Network Troubleshooting
- Virtualization
- Technical Documentation

# Priority Screenshots



<img width="1024" height="768" alt="Active-Directory-Overview" src="https://github.com/user-attachments/assets/e7b72ca1-3fa0-4ac4-a626-f2a4c77db52a" />
