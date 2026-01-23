# active-directory-enterprise-lab
A fully documented enterprise Active Directory lab built to demonstrate identity, access, and infrastructure engineering skills. This project includes OU design, RBAC, delegated administration, GPO implementation, and hybrid identity preparation. The structure and workflows reflect what IAM engineers, sysadmins, and security teams use in real enterprise environments.

---

##  Lab Sections

### **01 — Domain Controller Setup**
- Installed and configured Windows Server
- Promoted server to a domain controller
- Configured domain/forest functional levels
- Verified replication and core AD DS health

### **02 — Client Domain Join**
- ### **02 - Client Domain Join**
- Deployed Windows 10/11 client VM in same virtual network
- Configured DNS to point to domain controller
- Joined client to domain `testdomain.local`
- Verified domain membership and trust relationship
- Confirmed GPO application and user login functionality
- Captured screenshots of domain join and post-login state

### **03 — OU Structure & Design**
- Built a clean, scalable OU hierarchy
- Separated Users, Computers, and Departments
- Followed enterprise naming conventions
- Created custom admin groups
- Delegated OU-specific permissions using least privilege
- Documented delegated rights and verification steps

### **04 — Group Policy**
- Created and linked GPOs for departments
- Implemented BGInfo/branding, security baselines, and login policies
- Verified GPO application using gpresult and event logs

### **05 — Hybrid Identity Preparation**
- Added custom UPN suffix for Entra ID
- Installed and registered the Entra Cloud Sync agent
- Created gMSA for directory access
- Documented troubleshooting steps and lessons learned

---

##  Skills Demonstrated

- Active Directory Domain Services (AD DS)
- DNS administration
- OU and identity lifecycle design
- Role-Based Access Control (RBAC)
- Delegated administration
- Group Policy creation and troubleshooting
- Hybrid identity fundamentals
- Documentation and reproducible lab design

---

##  Screenshots

Each folder contains screenshots and notes documenting:
- Configuration steps  
- Verification steps  
- Troubleshooting  
- Final results  

This provides a clear, auditable record of the entire build.

---

##  Future Enhancements

- Complete Cloud Sync user provisioning
- Add Conditional Access and MFA
- Integrate Intune for device management
- Add PKI and certificate services
- Expand lab with SIEM/SOAR components

---

## Technologies Used

- Windows Server 2019
- Active Directory Domain Services
- DNS
- Group Policy Management
- Microsoft Entra ID (Azure AD)
- gMSA (Group Managed Service Accounts)
-  Windows 10
-  Proxmox
 
