 m# Ticket ##

## Issue
Network Discovery is turned off.
## User Report
"I can't access a shared folder on the network. Error message saying "Network Discovery is turned off.Network computers and devices are not visible. Please turn on network discovery in Network and Sharing Center"
## Environment
-Server: Windows Server 2022 (Domain Controller)
-Client: Windows 10
-Virtualization: Oracle VirtualBox
-Domain: stefonlab.local
-Shared Folder: \\10.0.2.100\CompanyFiles
## Symptoms
-Error displayed when opening the Network folder.
-Network devices are not visible.
-Shared folder cannot be browsed using Network.
-Client is able to ping the server successfully.
## Investigation
-Verified server connectivity using:
ping 10.0.2.100
-Result: 
4 packets sent, 4 received (0% loss).
-Verified the shared folder exists by running:
net share
-Confirmed:
CompanyFiles    C:\CompanyFiles
-Determined that basic network connectivity was functioning and the issue was related to Network Discovery.
## Troubleshooting Steps
1:Verified IP connectivity between client and server.
2:Confirmed the CompanyFiles SMB share existed on the server.
3:Attempted to browse the network.
4:Received the Network Discovery disabled message.
5:Navigated to:
-Control Panel
-Network and Internet
-Network and Sharing Center
-Change advanced sharing settings
6:Enabled:
-Network Discovery
-File and Printer Sharing
7:Retested access to the shared folder.
## Resolution
Network Discovery and File and Printer Sharing were enabled on the Windows 10 client, allowing network resources to be discovered and accessed.
## Root Cause
Network Discovery was disabled on the Windows 10 client, preventing the operating system from discovering computers and shared resources on the network.
## Skills Used
-Windows 10 Administration
-Windows Server 2022
-Active Directory
-SMB File Sharing
-Network Troubleshooting
-ICMP (Ping)
-Command Prompt
-PowerShell
-Windows Networking
## Screenshot(s)

## Lessons Learned
This issue demonstrated that successful network connectivity (verified with ping) does not guarantee that shared resources are accessible. Troubleshooting should begin by verifying connectivity, then confirming the shared resource exists, and finally checking Windows networking features such as Network Discovery and File and Printer Sharing.