# Active Directory Homelab

<p align="center">
  <img src="https://github.com/user-attachments/assets/96d29c0d-2435-482a-ae96-5f376fffc61f" width="250" title="Active Directory" alt="Active Directory">
  &nbsp;&nbsp;&nbsp;&nbsp;
  <img src="https://github.com/user-attachments/assets/e9fcb535-ad18-4e58-a2b5-88b40246842b" width="250" title="VirtualBox" alt="VirtualBox">
</p>

---

## Overview
This project documents the deployment of a hands-on Active Directory (AD) homelab environment using VirtualBox. The primary objective is to simulate a real-world enterprise IT infrastructure, focusing on the core foundations of Help Desk operations and System Administration. By the conclusion of this lab, a fully functional Domain Controller will be managing a Windows client workstation.

## Objectives
* **Deployment & Configuration:** Provision and configure Windows Server 2022 as a primary Domain Controller.
* **Identity Management:** Execute user and group management lifecycle via AD DS.
* **Network Services:** Implement and manage DNS and DHCP roles within a domain environment.
* **Policy Enforcement:** Design and deploy Group Policy Objects (GPOs) to standardize client configurations.
* **Operational Readiness:** Simulate enterprise support scenarios including credential management and account troubleshooting.

## Technologies Used
* **Virtualization:** Oracle VirtualBox 7.1.4
* **Server OS:** Windows Server 2022 (Desktop Experience)
* **Client OS:** Windows 10 / 11 Professional
* **Networking:** Active Directory Domain Services (AD DS), DNS, DHCP

## Project Status
> [!NOTE]
> **Current Phase:** Active Directory Promotion
> The core server OS is installed, and the environment is being promoted to a Domain Controller.

---

## Lab Progress Gallery

<details>
<summary><b>Step 1: Virtual Machine Configuration</b></summary>
<br>

1. **Hypervisor Setup:** Launched Oracle VirtualBox and initialized a new virtual machine instance.
2. **Resource Allocation:** Provisioned **8GB (8192MB) of RAM** and **2 Virtual CPUs** to ensure stable server performance.
3. **Storage Provisioning:** Created a **50GB Virtual Hard Disk (VDI)** with dynamic allocation for the OS installation.
4. **Boot Media:** Mounted the Windows Server 2022 ISO to the virtual optical drive for initial deployment.

<br>
<p align="center">
  <img src="https://github.com/user-attachments/assets/f36ea48c-6081-4465-be32-04e11fd68703" width="90%" alt="VirtualBox Manager View">
</p>
</details>

<details>
<summary><b>Step 2: Windows Server Installation</b></summary>
<br>

1. **OS Initialization:** Booted the VM and selected **Windows Server 2022 Standard Evaluation (Desktop Experience)**.
2. **Disk Partitioning:** Performed a **Custom Installation** to ensure a clean partition on the virtual drive.
3. **System Naming:** Renamed the server to **NY-DC-01** to adhere to enterprise naming conventions.
4. **Security Setup:** Established a complex Administrative password to secure the local system before domain promotion.

<br>
<p align="center">
  <img src="https://github.com/user-attachments/assets/662b4742-45a3-4d67-98e5-95614b150373" width="90%" alt="Windows Server OS Selection">
</p>
</details>

<details>
<summary><b>Step 3: Active Directory Domain Services (AD DS) Installation & Promotion</b></summary>
<br>

### 3.1 Role Selection
Utilized the **Add Roles and Features Wizard** within Server Manager to install the **Active Directory Domain Services** role. This included all necessary RSAT (Remote Server Administration Tools) for forest management.

<p align="center">
  <img src="https://github.com/user-attachments/assets/03fbb1b3-2dc6-4833-9ccc-478c8a3510e2" width="85%" alt="AD DS Role Selection">
</p>

### 3.2 Post-Deployment Configuration
Post-installation, I accessed the deployment thread via the Server Manager notification flag to initiate the **Promotion to a Domain Controller**.

<p align="center">
  <img src="https://github.com/user-attachments/assets/22551917-bca1-4fb2-8687-734066ec755e" width="85%" alt="Promotion Trigger">
</p>

### 3.3 Forest & Domain Naming
Configured the deployment operation as **"Add a new forest"** and established the Root Domain Name as `kevtech.com`. This successfully initialized the directory partition.

<p align="center">
  <img src="https://github.com/user-attachments/assets/f781fbea-967f-42a6-b95f-6ce7253e89cd" width="85%" alt="Forest Naming">
</p>

### 3.4 Installation & PowerShell Execution
Verified all prerequisites and executed the promotion. The system utilized a background PowerShell script to automate the configuration of the NTDS database and SYSVOL folders.

<p align="center">
  <img src="https://github.com/user-attachments/assets/53565ab4-2b88-41e4-9150-4a3567e6acb0" width="85%" alt="Installation Progress">
</p>

### 3.5 Domain Validation
Following the mandatory reboot, I verified the success of the promotion by confirming the **Domain Login** prompt. The Server Manager dashboard now correctly identifies the system as part of the `kevtech.com` domain.

<p align="center">
  <img src="https://github.com/user-attachments/assets/6e81747f-814d-4e13-94de-7db613ae5cc9" width="85%" alt="Domain Login Confirmation">
  <br><br>
  <img src="https://github.com/user-attachments/assets/d4a0b9c5-10ef-4aa6-9d2e-dff3f0764575" width="85%" alt="Local Server Properties Verification">
</p>
</details>

---

## Roadmap & Future Implementation
* [ ] Configure static IP and DNS settings.
* [ ] Create Organizational Units (OUs) for Users and Computers.
* [ ] Bulk-create users using PowerShell scripts.
* [ ] Join a Windows 10/11 client machine to the domain.
* [ ] Implement GPOs for security hardening and standardization.

## Key Learning Outcomes
* **Directory Architecture:** Understanding of forest roots, domain partitions, and schema initialization.
* **Enterprise Identity:** Experience in transitioning from local SAM accounts to centralized Domain Accounts.
* **Server Management:** Proficiency in role-based deployment and post-installation troubleshooting.
