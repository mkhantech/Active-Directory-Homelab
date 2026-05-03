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
2. **Name:** AD-Lab-Server (or preferred naming convention).
3. **ISO Image:** Select the downloaded Windows Server 2022 ISO.
4. **Edition:** Ensure **Windows Server 2022 Standard Evaluation (Desktop Experience)** is selected.
5. **Hardware:** Allocate **8GB RAM** and **2 CPUs** for optimal performance.
6. **Hard Disk:** Create a Virtual Hard Disk (VDI) with **50GB** of space.

<br>
<img src="https://github.com/user-attachments/assets/cbafd8b9-ae79-42ed-8fa9-ef8c8d3acefc" width="100%" alt="VirtualBox Configuration Settings">
</details>

<details>
<summary><b>Step 2: Windows Server Installation</b></summary>
<br>

1. **Power on VM** -> Follow the Windows Setup prompts.
2. **Installation Type:** Select **Custom: Install Microsoft Server Operating System only (advanced)**.
3. **Partitioning:** Select the unallocated space and click **Next**.
4. **Initial Setup:** Create a strong Administrator password upon completion.
5. **Post-Install:** Rename the server (e.g., `MY-DC01`) and restart to apply changes.

<br>
<img src="https://github.com/user-attachments/assets/79352460-3aeb-4eaf-854f-4f1354ed81f2" width="100%" alt="Windows Server Edition Selection">
</details>

<details>
<summary><b>Step 3: Active Directory Domain Services (AD DS)</b></summary>
<br>

1. **Open Server Manager** -> Click **Add roles and features**.
2. **Select Role:** Check **Active Directory Domain Services** -> Add Features -> Next.
3. **Installation:** Click **Install** and wait for the "Configuration required" notification.
4. **Promote Server:** Click the **yellow flag** in Server Manager -> Select **Promote this server to a domain controller**.
5. **Deployment:** Select **Add a new forest**.
6. **Root Domain Name:** `kevtech.com` (or preferred domain name).
7. **Automation (Optional):** Utilize the **PowerShell script** method for automated forest promotion.
8. **Reboot:** The server will automatically restart to finalize the Domain Controller roles.

<br>
<img src="https://github.com/user-attachments/assets/6504a742-f909-4720-bc6b-31a8128359f8" width="100%" alt="AD DS Configuration Wizard">
</details>

---

## Roadmap & Future Implementation
* [ ] Configure static IP addressing and internal DNS resolution.
* [ ] Design Organizational Unit (OU) structures for Users, Groups, and Computers.
* [ ] Automate bulk user creation utilizing PowerShell scripting.
* [ ] Join Windows client workstations to the production domain.
* [ ] Implement GPOs for security hardening and desktop environment standardization.

## Key Learning Outcomes
* Proficiency in enterprise domain hierarchy and architecture.
* Practical experience in server-side troubleshooting and log analysis.
* Development of professional technical documentation habits essential for IT career growth.
