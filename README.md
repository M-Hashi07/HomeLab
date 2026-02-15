**Active Directory Home Lab**
📌 **Project Overview**

Built a Windows Server domain environment to simulate enterprise 2nd Line infrastructure support tasks including AD administration, DNS troubleshooting, and Group Policy management.

---
🖥 Infrastructure Architecture

**Environment**

- VirtualBox (Internal Network: LABNET)

- Windows Server 2019 – DC01

- Windows 10 – CLIENT01

**Server Roles Installed**

- Active Directory Domain Services

- DNS Server

- File Services

---

⚙️ Advanced Configuration Tasks

**🔹 1. Domain Controller Deployment**

- Installed AD DS role

- Promoted server to Domain Controller

- Created new forest and domain

- Verified replication & SYSVOL creation

- Validated DNS integration

---
**🔹 2. Organisational Unit (OU) Design**

Created structured OUs to simulate enterprise environment:

Company.local

 ├── IT
 
 ├── Finance
 
 ├── HR
 
 └── Workstations


Applied users and computers into correct OUs.

---

**🔹 3. User & Group Management**

- Created multiple domain users

- Implemented security groups (e.g., IT_Admins, Finance_Read)

- Assigned users to role-based groups

- Applied least privilege principle

---

**🔹 4. Group Policy Management (GPO)**

- Configured and tested:

- Password policy enforcement

- Account lockout policy

- Desktop restrictions

- Mapped network drive via GPO (optional but powerful)

Validated policy application using:

gpresult /r

---

**🔹 5. File Share & NTFS Permission Configuration**

- Created shared directory on DC01

- Configured share-level permissions

- Configured NTFS permissions

- Applied group-based access control

- Tested access from CLIENT01

Confirmed:

- Finance group = read-only

- IT group = full control

---

**🔹 6. DNS Troubleshooting & Validation**

Simulated domain join failure and resolved by:

- Verifying client DNS settings

- Flushing DNS cache

- Using:

ipconfig /all
nslookup
ping domain.local


Confirmed correct A records and SRV records.

---

**🔹 7. PowerShell Automation**

Used PowerShell to:

- Create bulk users

- Add users to groups

- Verify AD objects

Example:

New-ADUser -Name "Test User" -AccountPassword (ConvertTo-SecureString "Password123!" -AsPlainText -Force) -Enabled $true

Demonstrated understanding of command-line administration beyond GUI tools.

---

**🛠 Troubleshooting Scenarios Simulated**

- Client unable to join domain (DNS misconfiguration)

- Incorrect group permissions blocking folder access

- Account lockout resolution

- Password reset via ADUC

- Network adapter misconfiguration

Used:

- Event Viewer

- Server Manager

- Services.msc

- ADUC console

- Command line diagnostics

---

**📊 Skills Demonstrated**

- Active Directory Administration

- Group Policy Management

- DNS Configuration & Troubleshooting

- NTFS & Share Permissions

- Role-Based Access Control

- Windows Server Deployment

- PowerShell for AD Management

- Incident Simulation & Resolution

- Virtual Network Configuration
