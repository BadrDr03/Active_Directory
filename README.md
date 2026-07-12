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

## 🎯 Implementation Phases
- [ ] Phase 1: Core Network Setup & Static IP Routing Configuration
- [ ] Phase 2: Active Directory Deployment & Domain Provisioning
- [ ] Phase 3: Splunk Server Deployment & Auditing Policy Configuration (Sysmon/GPO)
- [ ] Phase 4: Threat Simulation (Kerberoasting / Brute Force)
- [ ] Phase 5: Security Monitoring, Dashboards & Root-Cause Analysis (5 Whys)
