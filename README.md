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

This project focuses on setting-up Controlled and isolated  environment using Virtual box & Kali Linux where Hands - on practice on VAPT ,Scanning,cyber security Tools  and other security-testing [...]
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

![Architecture](Screenshot%201)

Additional target machines can be added to the same virtual network in future projects.
-----------------------------------------------------------------------------------------

## ⚙️ Lab Configuration

| 🧩 Component | ⚙️ Configuration |
| :--- | :--- |
| 🖥️ Host OS | Windows 11 |
| 🧠 Host RAM | 8 GB |
| ⚡ Processor | Intel Core i7 |
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
![Architecture](Screenshot-2.png.png%201)

This compression software  installed to compress the documents and programs so that they take less space and could be transported easily.  The software was required because the downloaded Kali Linux virtual machine package was highly compressed and needed to be extracted before it could be imported and used in Oracle VirtualBox.

**Tool:**  7-zip

---

## Step 2. Install VirtualBox
Oracle VirtualBox 7.2 was downloaded and installed as the hypervisor for creating and managing the virtual cybersecurity laboratory. VirtualBox provides the virtualization environment required for operating systems like  Kali Linux /windows and other virtual machines on the host computer.

---

## Step 3. Create the NAT Network

A standalone NAT Network was configured inside Oracle VirtualBox .
**Configuration:**
- **Network Name:** NatNetwork
- **IPv4 Prefix:** 10.0.0.0/24
- **DHCP:** Enabled
- **IPv6:** Disabled

A *NAT Network* was selected because multiple virtual machines connected to the same NAT Network can communicate with each other while also having external network connectivity.

This will allow future attacker and target VMs to communicate within the lab.
