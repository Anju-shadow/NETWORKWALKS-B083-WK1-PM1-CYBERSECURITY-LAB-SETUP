:safety_pin:   **Cybersecurity Lab Environment Setup**



##**Building an isolated virtual lab for penetration testing and ethical hacking practice**
![Cybersecurity](https://img.shields.io/badge/Skill-Cybersecurity-red)
![Virtualbox](https://img.shields.io/badge/Ver-Virtualbox%20v7.2-0078D7?logo=virtualbox)
![Kali Linux](https://img.shields.io/badge/Kali%20Linux-v2026.2-black?logo=kalilinux)
![Linux](https://img.shields.io/badge/Skill-Linux-E95420)
![Network](https://img.shields.io/badge/Network-10.0.0.0/24-008080)
![Penetration Testing](https://img.shields.io/badge/Penetration%20Testing-crimson?logo=hackthebox)
![Virtualization](https://img.shields.io/badge/Skill-Virtualization-purple)
![GitHub](https://img.shields.io/badge/GitHub-black?logo=github)
![NetworkWalks](https://img.shields.io/badge/NetworkWalks-darkslategray)
![Ethical Hacking](https://img.shields.io/badge/Ethical%20Hacking-darkorange)
![Author](https://img.shields.io/badge/ANJU%20-red)

----------------------------------------------------------------------------
## 📌 Project Overview

This project focuses on setting-up Controlled and isolated  environment using Virtual box & Kali Linux where Hands - on practice on VAPT ,Scanning,cyber security Tools  and other security-testing [...[...]
The lab is configured on a private virtual network so that additional machines can be added later and used as targets for authorized security testing

---------------------------------------------------------------------------------------

## 🎯 Objectives

The main objectives of this project are to:

- Install and configure VirtualBox.
- import Kali Linux as a virtual machine[VM]
- Create a private NAT Network for the cybersecurity lab.
- Configure network connectivity for Kali Linux.
- Assign a consistent IP address to the Kali VM.
- Verify network connectivity and DNS resolution.
- Take a clean VM snapshot for recovery.
- Document the complete setup process.
- Prepare the environment for future cybersecurity projects.

------------------------------------------
## 🛡️ Purpose of the Lab

The lab aims to provide an isolated environment for cyber -security practices & learning .This lab does not  compromise the systems in unethical way.

It can be used for activities such as:
Network reconnaissance
Port scanning
Vulnerability assessment
Packet analysis
Web security testing
Exploitation practice
Security-tool experimentation

⚠️ Important: This laboratory must only be conducted only for systems that are personaly owned  or have explicit permission granted by  the authorisation to test. 


## 🏗️ **Lab Architecture**

       HOST COMPUTER
          ⬇️
        Virtual box
          ⬇️
        Nat network
          ⬇️
       10.0.0.0/24
           ⬇️
        Kali Linux
           ⬇️
        10.0.0.24
         
         
Additional target machines can be added to the same virtual network in future projects.
-----------------------------------------------------------------------------------------

## ⚙️ Lab Configuration

| 🧩 Component | ⚙️ Configuration |
| :--- | :--- |
| 🖥️ Host OS | Windows 11 |
| 🧠 Host RAM | 8 GB |
| ⚡ Processor | Intel (R) Celeron(R) |
| 🧰 Hypervisor | VirtualBox 7.2 |
| 🐉 Security OS | Kali Linux 2026.2 |
| 🧠 Kali RAM | 2048 MB |
| 🌐 Virtual Network | NAT Network |
| 📡 Network Address | 10.0.0.0/24 |
| 🐧 Kali IP Address | 10.0.0.2/24 |
| 🚪 Default Gateway | 10.0.0.1 |
| 🌍 DNS Server | 8.8.8.8 | or  | 10.0.0.1 |
| 🔮 Future VM Range | 10.0.0.3–10.0.0.99 |

---

**# 🪜 Lab Setup Procedure**

## Step 1. Install 7-zip 
![7-zip](Screenshot-2.png)

**Purpose:** 7-zip is a free and open-source file archiver used for compressing and extracting files. It supports multiple compression formats and provides excellent compression ratios for large f[...[...]

**Tool:** 7-zip
---

## Step 2. Install VirtualBox
Oracle VirtualBox 7.2 was downloaded and installed as the hypervisor for creating and managing the virtual cybersecurity laboratory. VirtualBox provides the virtualization environment required fo[...]

---

## Step 3. Create the NAT Network

A standalone NAT Network was configured inside Oracle VirtualBox .
**Configuration:**
- **Network Name:** NatNetwork
- **IPv4 Prefix:** 10.0.0.0/24
- **DHCP:** Enabled
- **IPv6:** Disabled

![NAT Network Configuration](Screenshot%20-3.png)

A *NAT Network* was selected because multiple virtual machines connected to the same NAT Network can communicate with each other while also having external network connectivity.

This will allow future attacker and target VMs to communicate within the lab.
--------------------
## Step 4. Import Kali Linux

Now, let's import Kali Linux from the official website of kaliorg. The Kali Linux acts as an attacking machine. It is best to download the new version according to the hypervisor VirtualBox syste[...]

### VM Adapter Network Configuration:

| Configuration Item | Value |
| :--- | :--- |
| **Adapter** | Adapter 1 |
| **Attached to** | NAT Network |
| **Network** | NatNetwork |
| **Adapter Type** | Intel PRO/1000 MT Desktop |
| **RAM** | 2048 MB (2GB) |



---------------
## Step 5. Configure the Network :-

Now by edit connection ➡️ Wired connection ↘️

The Kali Linux network configuration was checked and configured with a consistent IPv4 address:
- IP Address: 10.0.0.2
- Subnet mask: /24
- Gateway: 10.0.0.1
- DNS: 8.8.8.8

![Kali Linux Network Configuration Step 5](Screenshot%20-6.png)
--------------------------------------------------------------------
## Step 6.  Take VM  Snapshot .
After completing the initial configuration, a VirtualBox snapshot was created.

Example snapshot name:

I started my Kali in VM today .(Anything could be written here)
The snapshot represents the clean baseline of the laboratory.

If a future exercise changes or damages the VM configuration, the machine can be restored to this baseline.
--------------------------------------------------------------------------------------------------------------
🐛**Problem I encountered and how i solved it?**
Documenting the problem we faces in setup is vital part of the project.
PROBLEM 1 :- setup of VM machine.
During setting up vertual box i encountered problem as i was confused in the official website which host should be downloaded and extension should also downloaded or not and then i was not able to see the network manager and then i try to find ,delete again and again .FInaly i found it in the media option that i have to enable as it was 2026 new version vm machine so some features were move to other part of the vm .
PROBLEM 2:- Import kali linux
During extraction i was not able to see the difference b/w kali zip v/s 7.zip .and was not able to add this to my vm .My storage was also not enough to extract the file however i  uninstall the kali vm +unnecessary files and started again to do step wise step with fresh .I successfully imported it in my virtual box.

