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
> **Current Phase:** Environment Setup
> The virtual infrastructure is currently being provisioned and configured.

---

## Lab Progress Gallery

<details>
<summary><b>Step 1: Virtual Machine Configuration</b></summary>
<br>
Provisioning the Windows Server 2022 virtual instance. Resources are allocated with 2 vCPUs and 8GB of RAM to maintain optimal performance for the Domain Controller role.
<br><br>
<img src="https://via.placeholder.com/800x450?text=Placeholder:+VirtualBox+Configuration+Screenshot" width="100%">
</details>

<details>
<summary><b>Step 2: Windows Server Installation</b></summary>
<br>
Deployment of Windows Server 2022 (Desktop Experience). This installation provides the necessary GUI tools for administrative efficiency during the initial setup phase.
<br><br>
<img src="https://via.placeholder.com/800x450?text=Placeholder:+Windows+Server+Installation+Screenshot" width="100%">
</details>

<details>
<summary><b>Step 3: Active Directory Domain Services (Pending)</b></summary>
<br>
*Upcoming:* Installation of the AD DS role and promotion of the server to a Domain Controller for the `kevtech.local` forest.
</details>

---

## Roadmap & Future Implementation
* Configure static IP addressing and internal DNS resolution.
* Design Organizational Unit (OU) structures for Users, Groups, and Computers.
* Automate bulk user creation utilizing PowerShell scripting.
* Join Windows client workstations to the production domain.
* Implement GPOs for security hardening and desktop environment standardization.

## Key Learning Outcomes
* Proficiency in enterprise domain hierarchy and architecture.
* Practical experience in server-side troubleshooting and log analysis.
* Development of professional technical documentation habits essential for IT career growth.
