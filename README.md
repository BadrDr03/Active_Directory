# Active Directory Defensive & Offensive Security Lab (SOC Telemetry)

## 📌 Project Overview
This project demonstrates the deployment, security hardening, attack simulation, and incident monitoring of an enterprise Active Directory (AD) environment. By routing endpoint and server telemetry into a centralized Splunk SIEM instance, this lab replicates real-world corporate SOC visibility against common modern threat vectors.

## 🛠️ Infrastructure Architecture
The entire environment is built using isolated hypervisor environments under a strictly non-routable host-only topology to avoid bleeding live exploitation traffic onto production networks.

* **Domain Name:** `badr.local`
* **Network Subnet:** `192.168.10.0/24`
* **Domain Controller (AD DS):** `192.168.10.7` — Windows Server 2022
* **SIEM Core Server:** `192.168.10.10` — Ubuntu Linux Server (Splunk Enterprise)
* **Target Workstation:** `192.168.10.X` — Windows 10/11 Enterprise Client
* **Attack Platform:** `192.168.10.250` — Kali Linux

### Network Diagram
![Network Topology](topology/ad_diagramme.png)

## 💻 Virtual Environment Sizing (VirtualBox)

| Machine Name | Operating System | vCPU | RAM | Base Role |
| :--- | :--- | :--- | :--- | :--- |
| **ADDC01** | Windows Server 2022 (Evaluation) | 2 | 4 GB | Domain Controller & DNS Server |
| **Ubuntu-SIEM**| Ubuntu Server 24.04 LTS | 2 | 4 GB | Splunk Enterprise Core |
| **Win10-Target**| Windows 10 Enterprise | 1 | 2 GB | Domain Joined Client |
| **Kali-Attacker**| Kali Linux | 1 | 2 GB | Pentesting Platform |

> ⚠️ **Troubleshooting Note:** After the initial Windows Server setup, ensure to remove the installation ISO from the VirtualBox virtual optical drive to prevent the boot order from cycling back into the installer loop.
