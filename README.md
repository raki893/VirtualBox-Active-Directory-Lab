# Active Directory Home Lab Setup (VirtualBox)
### Description
A comprehensive guide and associated scripts for setting up a functional Active Directory domain controller and a Windows 10 client machine within a virtualized environment using VirtualBox. This project demonstrates proficiency in network configuration, server administration, user management, and virtualization technologies.

---

### Features
* **Domain Controller (Windows Server 2025):**
    * Installation and initial configuration.
    * Active Directory Domain Services (AD DS) installation and domain creation.
    * DHCP server setup for automatic IP assignment.
    * NAT and routing configuration for internet access from the internal network.
    * PowerShell script to automate the creation of 1000 Active Directory users.
* **Client Machine (Windows 10):**
    * Installation and network configuration.
    * Domain join and user login with domain accounts.
* **Network Configuration:**
    * Implementation of a private internal network for secure communication between virtual machines.
    * NAT network adapter for internet connectivity on the domain controller.

---

### Technologies Used
* **Virtualization:** Oracle VirtualBox
* **Operating Systems:**
    * Windows Server 2025 (for Domain Controller)
    * Windows 10 (for Client Machine)
* **Scripting:** PowerShell (for user creation)
* **Networking Concepts:** DNS, DHCP, NAT, Routing, Private Networks

---

### Project Structure
/
├── scripts/
│   └── create_ad_users.ps1        # PowerShell script to bulk-create AD user accounts
├── images/
│   ├── vm_network_diagram.png     # Visual diagram of the virtual network setup
│   └── ad_users_screenshot.png    # Screenshot showing successfully created users in AD
└── README.md                      # Project documentation and setup instructions


---

### Setup Instructions
1.  **Prerequisites:**
    * Download and install [Oracle VirtualBox](https://www.virtualbox.org/).
    * Obtain ISOs for Windows Server 2025 and Windows 10 (mention where they can legally be obtained, e.g., Microsoft Evaluation Center or your licensed source).
2.  **Create Domain Controller VM:**
    * Detailed steps for VirtualBox VM creation (memory, CPU, storage).
    * Networking setup (NAT and Host-only adapter configuration).
    * Windows Server 2025 installation.
    * Post-installation configuration (IP addressing, server naming).
    * Steps to install AD DS, promote to domain controller, and create the domain.
    * DHCP server configuration steps.
    * NAT/routing setup (if you configured it on the DC).
    * Instructions on how to run `create_ad_users.ps1`.
3.  **Create Windows 10 Client VM:**
    * Detailed steps for VirtualBox VM creation.
    * Networking setup (connect to the same Host-only adapter as the DC).
    * Windows 10 installation.
    * Steps to join the domain and log in.

---

### Learning Outcomes
* Gained hands-on experience in **Active Directory administration**, including domain setup, user/group management, and DNS integration.
* Developed skills in **virtualization** using VirtualBox to create isolated lab environments.
* Strengthened understanding of **network services** like DHCP and the principles of NAT and routing.
* Practiced **Windows Server installation** and initial configuration.
* Enhanced **PowerShell scripting** abilities for automation of administrative tasks.

---

### Future Enhancements (Optional)
* Implement Group Policy Objects (GPOs).
* Add a second domain controller or a read-only domain controller (RODC).
* Integrate with a Linux server or another network service.
* Set up a WSUS server for patch management.
