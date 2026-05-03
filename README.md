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
3. **ISO Image:** Select the downloaded Windows Server 2022 ISO.
4. **Edition:** Ensure **Windows Server 2022 Standard Evaluation (Desktop Experience)** is selected.
5. **Hardware:** Allocate **8192 MB (8GB) RAM** and **2 CPUs** for optimal performance.
6. **Hard Disk:** Create a Virtual Hard Disk (VDI) with **50GB** of space.

<br>
<img src="https://github.com/user-attachments/assets/6dd65478-9d0d-4e7e-a34b-e03986253d8b" width="100%" alt="VirtualBox Configuration Settings">
</details>

<details>
<summary><b>Step 2: Windows Server Installation</b></summary>
<br>

1. **Power on VM** -> Follow the Windows Setup prompts.
2. **OS Selection:** Choose **Windows Server 2022 Standard Evaluation (Desktop Experience)**.
3. **Installation Type:** Select **Custom: Install Microsoft Server Operating System only (advanced)**.
4. **Initial Setup:** Create a strong Administrator password and rename the server to **NY-DC-01**.
5. **Finalization:** The system boots to the lock screen, ready for role configuration.

<br>
<img src="https://github.com/user-attachments/assets/708efce9-7834-4a88-885f-1f4ee99f060e" width="100%" alt="Windows Server
