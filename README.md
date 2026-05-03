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
The virtual machine is provisioned within Oracle VirtualBox to support the Windows Server 2022 environment. The resource allocation is optimized for the Domain Controller role, ensuring stable performance for identity management tasks.
<br><br>

**Technical Specifications:**
* **VM Name:** AD-Lab-Server
* **Base Memory:** 8192 MB (8GB)
* **Processors:** 2 CPUs
* **Storage:** 50.00 GB VDI
* **Network:** NAT (Initial Setup)

<br>
<img src="https://github.com/user-attachments/assets/cbafd8b9-ae79-42ed-8fa9-ef8c8d3acefc" width="100%" alt="VirtualBox Configuration Settings">
</details>

<details>
<summary><b>Step 2: Windows Server Installation</b></summary>
<br>
Selecting the operating system edition. For this lab, **Windows Server 2022 Standard Evaluation (Desktop Experience)** is chosen to provide a full Graphical User Interface (GUI), which is essential for managing Active Directory tools visually.
<br><br>

**Key Installation Details:**
* **Architecture:** x64
* **Edition:** Standard Evaluation
* **Interface:** Desktop Experience (Full GUI)
* **Status:** Operating System Selection Phase

<br>
<img src="https://github.com/user-attachments/assets/79352460-3aeb-4eaf-854f-4f1354ed81f2" width="100%" alt="Windows Server Edition Selection">
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
