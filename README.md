 <div align="center">

# 🛡️ Cybersecurity Lab & Network Security Investigation

**A hands-on virtual cybersecurity environment with Kali Linux and practical SOC investigations using Wireshark.**

<img src="https://img.shields.io/badge/Domain-Cybersecurity-DC3545?style=for-the-badge" />
<img src="https://img.shields.io/badge/Virtualization-Oracle%20VirtualBox-246BCE?style=for-the-badge&logo=virtualbox&logoColor=white" />
<img src="https://img.shields.io/badge/Operating%20System-Kali%20Linux-557C94?style=for-the-badge&logo=kalilinux&logoColor=white" />
<img src="https://img.shields.io/badge/Network-10.0.0.0%2F24-198754?style=for-the-badge" />
<img src="https://img.shields.io/badge/Packet%20Analysis-Wireshark-1679A7?style=for-the-badge&logo=wireshark&logoColor=white" />

</div>

---

## 📖 Introduction

This project documents the implementation of a virtual cybersecurity laboratory using **Oracle VirtualBox and Kali Linux**, followed by practical network security investigations using Wireshark.

The virtual lab provides a dedicated environment for cybersecurity experimentation, network configuration, and ethical hacking practice. A custom NAT Network was configured to establish a virtual network with a defined IP addressing scheme.

Alongside the lab setup, six SOC investigation exercises were completed to explore network traffic analysis, suspicious communication, exposed credentials, brute-force activities, and VoIP investigations.

## 🎯 Project Objectives

- Build a virtual cybersecurity environment using VirtualBox.
- Deploy Kali Linux as the primary security testing machine.
- Configure a custom NAT Network with IPv4 subnet `10.0.0.0/24`.
- Assign a static IP address to Kali Linux.
- Establish network connectivity and internet access.
- Configure host-to-guest integration and shared resources.
- Practice network packet analysis using Wireshark.
- Investigate suspicious network activities through practical SOC exercises.

---

## 🏗️ Virtual Lab Architecture

The environment uses Oracle VirtualBox as the virtualization platform, with Kali Linux connected to a custom NAT Network.

### Network Topology

```text
                 INTERNET
                    |
                    |
             HOST COMPUTER
              Windows OS
                    |
                    |
             ORACLE VIRTUALBOX
                    |
                    |
              NAT NETWORK
              10.0.0.0/24
                    |
                    |
               KALI LINUX
                10.0.0.2
                    |
             SECURITY TESTING
```

The network is designed to accommodate additional virtual machines for future security testing and network investigation exercises.

## ⚙️ Environment Configuration

| Component | Implemented Configuration |
|---|---|
| Host Platform | Windows |
| Virtualization | Oracle VirtualBox |
| Guest Operating System | Kali Linux 2026.3 |
| Virtual Network | NAT Network |
| Network Name | NatNetwork |
| IPv4 Network | `10.0.0.0/24` |
| Subnet Mask | `255.255.255.0` |
| Kali Linux Address | `10.0.0.2/24` |
| Default Gateway | `10.0.0.1` |
| DNS Server | `8.8.8.8` |
| DHCP | Enabled |
| IPv6 | Disabled |

---

## 🔧 Implementation & Configuration

### 1. Virtualization Environment

Oracle VirtualBox was installed and configured to host the cybersecurity virtual machine.

7-Zip was also used as the archive utility for handling virtual machine packages.

**Tools:**
- Oracle VirtualBox
- 7-Zip

### 2. Custom NAT Network Configuration

A custom NAT Network named `NatNetwork` was configured in VirtualBox.

Network parameters:

```text
Network Name : NatNetwork
IPv4 Prefix  : 10.0.0.0/24
DHCP         : Enabled
IPv6         : Disabled
```

This configuration provides a virtual networking environment for connected virtual machines and outbound network connectivity.

![VirtualBox NAT Network Configuration](2-screenshot-network-settings-1.png)

### 3. Kali Linux Deployment

Kali Linux 2026.3 was imported into VirtualBox and successfully started as the primary virtual machine for the lab.

The virtual machine was connected to the previously configured NAT Network.

![Kali Linux Desktop](1-screenshot-kali-linux.png)

### 4. Static IP Configuration

The Kali Linux network interface was configured with a manual IPv4 address.

```text
IPv4 Method : Manual
IP Address  : 10.0.0.2
Netmask     : 24
Gateway     : 10.0.0.1
DNS         : 8.8.8.8
```

A static address provides a consistent network identity for the Kali Linux machine within the virtual lab.

![Kali Linux IPv4 Configuration](3-screenshot-kali-network-settings.png)

### 5. Virtual Machine Integration

The VirtualBox integration settings were configured to support interaction between the host system and Kali Linux.

- Shared Clipboard: Bidirectional
- Drag and Drop: Bidirectional
- Shared Folder: Host downloads directory
- Auto-mount: Enabled

These features simplify file transfer and interaction between the host and guest operating systems.

### 6. Snapshot and Recovery

A baseline snapshot was created after the initial Kali Linux configuration to preserve the configured environment and provide a recovery point for subsequent experiments.

---

## 🔍 SOC Analyst Practical Investigations

In addition to building the virtual environment, six browser-based Wireshark investigation labs were completed.

Each lab contained ten investigation tasks, providing practical exposure to different network security scenarios.

### Investigation 01 — Attacker IP Identification

**Focus:** Network traffic investigation.

Identified suspicious source IP activity by examining captured packets and their communication patterns.

[Open Lab 3](https://networkwalks.com/wireshark-lab3/)

### Investigation 02 — TCP Stream Analysis

**Focus:** Communication reconstruction.

Used Follow TCP Stream to reconstruct conversations and inspect information exchanged between network endpoints.

[Open Lab 4](https://networkwalks.com/wireshark-lab4/)

### Investigation 03 — TCP Stream Analysis & Hidden Data

**Focus:** Network data inspection.

Investigated TCP communication and examined transmitted information to identify hidden data.

[Open Lab 5](https://networkwalks.com/wireshark-lab5/)

### Investigation 04 — HTTP Credential Exposure

**Focus:** Clear-text credential investigation.

Examined unencrypted HTTP communication to identify usernames and passwords transmitted through network requests.

[Open Lab 6](https://networkwalks.com/wireshark-lab6/)

### Investigation 05 — Brute-Force Attack Detection

**Focus:** Suspicious authentication activity.

Analyzed repeated login attempts and investigated the source responsible for password-guessing activity.

[Open Lab 7](https://networkwalks.com/wireshark-lab7/)

### Investigation 06 — VoIP Scam Investigation

**Focus:** Voice communication analysis.

Examined captured VoIP traffic, reconstructed the recorded call, and investigated the suspicious caller.

[Open Lab 8](https://networkwalks.com/wireshark-lab8/)

---

## 📊 Investigation Summary

| No. | SOC Investigation | Tasks |
|---|---|---:|
| 01 | Attacker IP Identification | 10 |
| 02 | TCP Stream Analysis – Part 1 | 10 |
| 03 | TCP Stream Analysis – Part 2 | 10 |
| 04 | HTTP Plain-Text Credentials | 10 |
| 05 | Brute-Force Attacker Detection | 10 |
| 06 | VoIP Scam Investigation | 10 |
| | **Total** | **60** |

---

## 🧠 Skills & Technical Knowledge

The project provided practical experience in the following areas:

**Virtualization & Linux**
- Virtual machine deployment and management
- Kali Linux environment configuration
- Virtual network administration
- Static IPv4 configuration

**Networking**
- IPv4 addressing and subnetting
- NAT Network configuration
- Gateway and DNS configuration
- Virtual machine networking

**Network Security & SOC**
- Packet inspection using Wireshark
- TCP stream reconstruction
- HTTP traffic investigation
- Clear-text credential identification
- Brute-force activity detection
- VoIP traffic analysis
- Network threat investigation

---

## 🔐 Ethical Considerations

This project is intended for cybersecurity education and authorized security testing.

All security experiments should be conducted only within controlled laboratory environments or on systems for which explicit permission has been obtained.

---

## 📚 References & Resources

- [Oracle VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- [Kali Linux](https://www.kali.org/get-kali/)
- [Wireshark](https://www.wireshark.org/)
- [7-Zip](https://www.7-zip.org/download.html)
- [Networkwalks](https://www.networkwalks.com/)

---

## 👨‍💻 Project Information

| Category | Details |
|---|---|
| Project Title | Cybersecurity Lab & Network Security Investigation |
| Domain | Cybersecurity |
| Virtualization Platform | Oracle VirtualBox |
| Security Operating System | Kali Linux |
| Network Configuration | NAT Network – `10.0.0.0/24` |
| Packet Analysis Tool | Wireshark |
| Practical SOC Labs | 6 |
| Investigation Tasks | 60 |

**Project Outcome:** Successfully established a Kali Linux-based virtual cybersecurity environment and completed six practical network traffic investigation labs covering fundamental SOC analysis techniques.

---

<div align="center">

**Learn • Configure • Investigate • Secure**

*Hands-on cybersecurity practice through virtual labs and network forensics.*

</div>
