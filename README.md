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

1. **Open VirtualBox** -> Select **New**.
2. **Name:** AD-Lab-Server.
3. **Hardware:** Allocated **8192 MB (8GB) RAM** and **2 CPUs**.
4. **Storage:** Created a **50GB** virtual hard disk (VDI).

<br>
<p align="center">
  <img src="https://github.com/user-attachments/assets/f36ea48c-6081-4465-be32-04e11fd68703" width="90%" alt="VirtualBox Manager View">
</p>
</details>

<details>
<summary><b>Step 2: Windows Server Installation</b></summary>
<br>

1. **Power on VM** -> Followed the Windows Setup prompts.
2. **OS Selection:** Chose **Windows Server 2022 Standard Evaluation (Desktop Experience)**.
3. **Installation Type:** Selected **Custom** to perform a clean install.
4. **Initial Setup:** Set the Administrator password and arrived at the lock screen.

<br>
<p align="center">
  <img src="https://github.com/user-attachments/assets/662b4742-45a3-4d67-98e5-95614b150373" width="90%" alt="Windows Server OS Selection">
</p>
</details>

<details>
<summary><b>Step 3: Active Directory Domain Services (AD DS)</b></summary>
<br>

1. **Open Server Manager** -> Click **Add roles and features**.
2. **Select Role:** Checked **Active Directory Domain Services** and confirmed required features.
3. **Installation:** Clicked **Install** to deploy AD DS binaries.
4. **Promotion:** Promoted the server to a Domain Controller for the `kevtech.com` forest.

<br>
<p align="center">
  <img src="https://github.com/user-attachments/assets/8c15bddc-01a3-4686-8b78-2605158c7357" width="90%" alt="AD DS Role Installation">
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
* Proficiency in enterprise domain hierarchy and architecture.
* Practical experience in server-side troubleshooting and log analysis.
* Development of professional technical documentation habits.
