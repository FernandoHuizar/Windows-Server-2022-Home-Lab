# Windows Server 2022 Home Lab Environment

## Overview
Enterprise-level Active Directory environment built for hands-on learning and skill development in system administration, identity management, and network services.

## Infrastructure
- **Virtualization Platform:** Oracle VirtualBox 7.0
- **Domain Controller:** Windows Server 2022 (CA-DC-01.fernandotech.com)
- **Client Machine:** Windows 10 Pro 22H2 (Desktop01.fernandotech.com)
- **Domain:** fernandotech.com
- **Network:** 10.1.10.0/24 subnet

## Technologies Implemented

### Active Directory Domain Services (AD DS)
- Configured domain controller with DNS integration
- Created organizational units (OUs) for Computers, Users, Domain Controllers
- Implemented security groups for role-based access control (RBAC)
- Joined Windows 10 client to domain

### Group Policy Management
- Enforced password complexity requirements (12-character minimum)
- Configured account lockout policies (3 invalid attempts)
- Set password history (24 passwords remembered)
- Implemented password age restrictions (90-day maximum, 1-day minimum)

### Network File Sharing
- Created and configured network shares (NETLOGON, SYSVOL, FernandoTech)
- Implemented NTFS permissions with security group-based access control
- Mapped network drives (Z: drive) on domain-joined clients
- Tested cross-machine file sharing and permissions

### Patch Management & Security
- Deployed Action1 RMM platform for centralized management
- Configured automated vulnerability scanning
- Deployed 6+ critical security updates (.NET Framework, Windows patches)
- Remediated 1,000+ identified vulnerabilities
- Monitored patch compliance across endpoints

### User & Group Management
- Created domain user accounts with appropriate permissions
- Configured security groups (Tech, Personal)
- Assigned users to security groups for resource access
- Managed user accounts via Active Directory Users and Computers (ADUC)

## Lab Setup Process

### Prerequisites
- Oracle VirtualBox installed
- Windows Server 2022 ISO
- Windows 10 Pro ISO
- Minimum 16GB RAM, 100GB storage

### Step 1: Domain Controller Setup
1. Created Windows Server 2022 VM (4GB RAM, 50GB storage)
2. Installed Active Directory Domain Services role
3. Promoted server to domain controller
4. Configured DNS services
5. Created fernandotech.com domain

### Step 2: Client Configuration
1. Created Windows 10 VM (4GB RAM, 40GB storage)
2. Configured network settings (static IP: 10.1.10.3)
3. Set DNS to point to domain controller (10.1.10.2)
4. Joined Desktop01 to fernandotech.com domain
5. Verified domain authentication

### Step 3: Group Policy Implementation
1. Opened Group Policy Management Console
2. Created and linked GPOs to domain
3. Configured password policies under Security Settings
4. Tested policy enforcement on client machine

### Step 4: File Sharing Configuration
1. Created shared folder structure on domain controller
2. Configured NTFS permissions for security groups
3. Created network share with appropriate access controls
4. Mapped network drives on client machines
5. Tested file access and permissions

### Step 5: Patch Management Deployment
1. Downloaded and installed Action1 Deployer on DC
2. Configured service account with domain admin credentials
3. Enabled Active Directory discovery
4. Deployed Action1 agents to domain computers
5. Configured vulnerability scanning schedule
6. Deployed critical security updates automatically

## Skills Demonstrated
- Windows Server 2022 administration
- Active Directory Domain Services (AD DS)
- DNS configuration and management
- Group Policy Object (GPO) creation and enforcement
- NTFS permissions and access control
- Network file sharing and drive mapping
- Remote monitoring and management (RMM)
- Patch management and vulnerability remediation
- Virtualization (Oracle VirtualBox)
- Network configuration (TCP/IP, subnetting)

## Key Learnings
- Understanding of enterprise identity management
- Hands-on experience with domain controller operations
- Group Policy enforcement for security hardening
- Role-based access control implementation
- Centralized patch management workflows
- Troubleshooting domain authentication issues

## Screenshots
Active Directory Users and Computers - <img width="1588" height="1015" alt="image" src="https://github.com/user-attachments/assets/c8652832-34e1-49fd-bb5f-739a87e521e4" />
Group Policy Management Console - <img width="1147" height="522" alt="image" src="https://github.com/user-attachments/assets/c4ab5d89-b37c-4764-bd6b-6d05348db884" />
Group Policy settings (password policy) - <img width="1167" height="383" alt="image" src="https://github.com/user-attachments/assets/2db9398c-b0ba-44a4-8180-06c0460bb1a5" />
Network Shares - <img width="1005" height="514" alt="image" src="https://github.com/user-attachments/assets/6b0590ec-6988-4577-b98f-d2ebf1c85676" />
Network drive mapped - <img width="1580" height="1004" alt="image" src="https://github.com/user-attachments/assets/42f7f790-5e9f-4db0-bcc2-7429565fd913" />
Domain-joined computer - <img width="1188" height="868" alt="image" src="https://github.com/user-attachments/assets/48b584d2-9bf5-40c9-af4c-c8ca83f947b6" />
Action1 Dashboard - <img width="1890" height="791" alt="image" src="https://github.com/user-attachments/assets/a411d675-5ca2-4726-b1ba-f17906345c2e" />
<img width="1124" height="309" alt="image" src="https://github.com/user-attachments/assets/c5cf1245-456f-4819-896b-1a0430394bc6" />
<img width="1066" height="696" alt="image" src="https://github.com/user-attachments/assets/af347577-772e-4ca3-858d-344559856b36" />

## Future Enhancements
- Implement Windows Server Update Services (WSUS)
- Configure DHCP services
- Set up additional organizational units
- Create more complex GPO structures
- Add redundant domain controller
- Implement file server role

## References
- KevTech IT Support YouTube Tutorial Series
- Microsoft Official Documentation
- Action1 RMM Documentation

---

**Author:** Fernando Huizar  
**Contact:** fernando.huizar.jr@gmail.com  
