# 🖥️ Active Directory Homelab (Work in Progress)

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/d/d5/VirtualBox_logo.svg" width="150" title="VirtualBox" alt="VirtualBox">
  &nbsp;&nbsp;&nbsp;&nbsp;
  <img src="https://upload.wikimedia.org/wikipedia/commons/4/44/Microsoft_Active_Directory_Logo.svg" width="200" title="Active Directory" alt="Active Directory">
</p>

## 📌 Overview
This project documents my journey building a hands-on Active Directory (AD) homelab using **VirtualBox**. The goal is to simulate a real-world enterprise IT environment, focusing on the core foundations of Help Desk and System Administration. By the end of this lab, I will have a fully functional Domain Controller managing a Windows client machine.

## 🎯 Objectives
* **Deploy & Configure:** Setup Windows Server 2022 as a Domain Controller.
* **Identity Management:** Practice user and group management via AD DS.
* **Network Services:** Understand the role of DNS and DHCP in a domain.
* **Policy Enforcement:** Implement Group Policy Objects (GPO) to manage client settings.
* **Support Readiness:** Simulate real IT support scenarios like password resets and account lockouts.

## 🛠️ Technologies Used
* **Virtualization:** Oracle VirtualBox 7.1.4
* **Server OS:** Windows Server 2022 (Desktop Experience)
* **Client OS:** Windows 11 / Windows 10
* **Networking:** Active Directory Domain Services (AD DS)

## 📂 Project Status
> [!IMPORTANT]
> **Current Status:** 🚧 Environment Setup (Following Kevtech Lab)
> This project is currently under development as I configure the virtual infrastructure.

## 📸 Lab Progress Gallery

<details>
<summary><b>Step 1: Virtual Machine Configuration (Click to expand)</b></summary>
<br>
Setting up the Windows Server 2022 VM. Configured with 2 CPUs and 8GB of RAM to ensure smooth performance for the Domain Controller.
<br>
<img src="https://via.placeholder.com/800x450?text=Placeholder:+Add+your+VirtualBox+settings+screenshot+here" width="100%">
</details>

<details>
<summary><b>Step 2: Windows Server Installation</b></summary>
<br>
Installing the Windows Server 2022 OS using the ISO. Selecting the "Desktop Experience" to have a full GUI for management.
<br>
<img src="https://via.placeholder.com/800x450?text=Placeholder:+Add+your+Windows+Server+Desktop+screenshot+here" width="100%">
</details>

<details>
<summary><b>Step 3: Active Directory Domain Services (Pending)</b></summary>
<br>
Future update: Installing AD DS roles and promoting the server to a Domain Controller (kevtech.local).
</details>

---

## 📘 Future Plans
* [ ] Configure static IP and DNS settings.
* [ ] Create Organizational Units (OUs) for Users and Computers.
* [ ] Bulk-create users using PowerShell scripts.
* [ ] Join a Windows 10/11 client machine to the domain.
* [ ] Create a GPO to restrict Wallpaper or Control Panel access for end-users.

## 💡 Key Learning Outcomes
* Understanding the hierarchy of an enterprise domain environment.
* Hands-on experience with server-side troubleshooting.
* Developing documentation habits essential for IT professional growth.
