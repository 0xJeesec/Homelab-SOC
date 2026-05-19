# 🛡️ Homelab SOC / Blue Team

![Status](https://img.shields.io/badge/project-active-brightgreen)
![Type](https://img.shields.io/badge/type-home--lab-blue)
![Platform](https://img.shields.io/badge/platform-Proxmox-orange)
![Focus](https://img.shields.io/badge/focus-SOC_%2B_Blue_Team-blue)

Welcome to my **SOC / Blue Team Homelab**, a personal project focused on building and simulating an enterprise-like environment for defensive security operations.

This laboratory serves as both a practical learning environment and a portfolio project designed to strengthen hands-on experience in:

- Network segmentation and firewalling
- Active Directory and domain infrastructure
- Security monitoring and log analysis
- SIEM visibility and threat detection
- Incident simulation and defensive operations

> 🎯 Goal: Build a functional SOC environment from scratch with a focus on visibility, detection, hardening, and real-world security scenarios.

---

## 🏗️ Architecture

📸

![Network Diagram](docs/screenshots/architecture/network-diagram.png)

---

## 🧱 Infrastructure Overview

| Component | Role |
|---|---|
| `LORA-PVE` | Proxmox Hypervisor |
| `TEKEN-DC01` | Active Directory Domain Controller |
| `OUVI-WS01` | Windows Client Endpoint |
| `PALANTIR-SIEM` | Wazuh SIEM |
| `HYDRA-LAB01` | Vulnerable Machine |

---

## 🌐 Network Design

| VLAN | Name | Purpose |
|---|---|---|
| 9 | MANAGEMENT | Administrative access |
| 110 | ENDPOINTS | User systems |
| 120 | SERVERS | Infrastructure services |
| 130 | LAB | Vulnerable systems and testing |
| 140 | SOC | Monitoring and SIEM |

---

## ⚙️ Technologies Used

### Infrastructure
- Proxmox VE
- FortiGate
- Managed Switch

### Systems
- Windows Server 2019
- Windows 10 LTSC
- Active Directory

### Security & Monitoring
- Wazuh SIEM
- Windows Event Logs
- Sysmon *(planned)*

---

## 📂 Project Structure

```bash
docs/
├── infrastructure/
│   ├── proxmox.md
│   ├── fortigate.md
│   └── switch.md
│
├── systems/
│   ├── active-directory.md
│   └── windows-client.md
│
├── siem/
│   ├── wazuh-installation.md
│   ├── agents.md
│   └── log-ingestion.md
│
├── detection/
│
├── incidents/
│
└── screenshots/
```

---

## 📚 Technical Documentation

### Infrastructure
- Proxmox deployment
- FortiGate configuration
- Switch configuration

### Systems
- Active Directory setup
- Windows endpoint deployment

### SIEM
- Wazuh installation
- Agent integration
- Log ingestion

### Detection
- Detection use cases
- Rules
- Alerts

### Incident Response
- Timeline analysis
- Investigation
- Mitigation actions

---

## 📊 Project Phases

> Roadmap focused on the progressive development of a functional SOC environment.

### 🔹 Phase 1 – Core Infrastructure
- [x] Deploy Proxmox Hypervisor
- [x] Configure FortiGate Firewall
- [x] Implement VLAN segmentation
- [x] Configure managed switch
- [x] Deploy Active Directory (`TEKEN-DC01`)
- [x] Deploy Windows endpoint (`OUVI-WS01`)

### 🔹 Phase 2 – Monitoring & Log Centralization
- [x] Deploy Wazuh SIEM (`PALANTIR-SIEM`)
- [ ] Configure Wazuh agents
- [ ] Integrate Windows logs
- [ ] Centralize security events
- [ ] Validate event visibility

### 🔹 Phase 3 – Threat Detection & Analysis
- [ ] Create detection use cases
- [ ] Generate alerts
- [ ] Implement event correlation

### 🔹 Phase 4 – Incident Simulation
- [ ] Simulate brute-force attacks
- [ ] Simulate suspicious PowerShell activity
- [ ] Simulate privilege escalation scenarios

### 🔹 Phase 5 – Hardening & Visibility
- [ ] Deploy Sysmon
- [ ] Improve dashboards
- [ ] Implement security hardening

### 🔹 Phase 6 – Incident Response
- [ ] Create incident reports
- [ ] Build investigation timelines
- [ ] Document mitigation actions

---

## 🚀 Next Steps

- Integrate FortiGate logs
- Deploy Sysmon
- Create brute-force detection
- Develop SOC use cases
- Simulate controlled attacks

---

## 👨‍💻 Author

Personal project developed for hands-on learning and practical experience in:

- SOC Operations
- Blue Team
- Threat Detection
- Incident Response
- Defensive Security

GitHub:
https://github.com/FUZHIXx
