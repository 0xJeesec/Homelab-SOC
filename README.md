# 🛡️ Homelab SOC / Blue Team

![Status](https://img.shields.io/badge/project-active-brightgreen)
![Type](https://img.shields.io/badge/type-home--lab-blue)
![Platform](https://img.shields.io/badge/platform-Proxmox-orange)
![Focus](https://img.shields.io/badge/focus-SOC_%2B_Blue_Team-blue)

Personal project focused on building and simulating an enterprise-like Security Operations Center (SOC) environment to develop practical skills in defensive security, monitoring, and threat detection.

> 🎯 Goal: Build a functional SOC environment focused on visibility, detection, hardening, and incident analysis.

---

## 🏗️ Architecture

![Network Diagram](docs/screenshots/architecture/network-diagram.png)

---

## 🧱 Infrastructure

| Component | Role |
|---|---|
| `LORA-PVE` | Proxmox Hypervisor |
| `TEKEN-DC01` | Active Directory Domain Controller |
| `OUVI-WS01` | Windows Client Endpoint |
| `PALANTIR-SIEM` | Wazuh SIEM |
| `HYDRA-LAB01` | Vulnerable Machine |

---

## 🌐 Network Design

| VLAN | Purpose |
|---|---|
| VLAN 9 | Management |
| VLAN 110 | Endpoints |
| VLAN 120 | Servers |
| VLAN 130 | Lab |
| VLAN 140 | SOC |

---

## ⭐ Key Features

- Network segmentation using VLANs
- Active Directory environment
- Centralized log collection
- Security monitoring with Wazuh
- Threat detection use cases
- Incident simulation scenarios

---

## 📚 Documentation

### Infrastructure
- [Proxmox](docs/infrastructure/proxmox.md)
- [FortiGate](docs/infrastructure/fortigate.md)
- [Switch](docs/infrastructure/switch.md)

### Systems
- [Active Directory](docs/systems/active-directory.md)
- [Windows Client](docs/systems/windows-client.md)

### SIEM
- [Wazuh Installation](docs/siem/wazuh-installation.md)
- [Agent Integration](docs/siem/agents.md)

---

## 📊 Project Phases

### ✅ Phase 1 — Core Infrastructure
- [x] Proxmox deployment
- [x] FortiGate configuration
- [x] VLAN implementation
- [x] Active Directory deployment
- [x] Windows endpoint deployment

### 🔄 Phase 2 — Monitoring & Visibility
- [x] Wazuh deployment
- [ ] Agent integration
- [ ] Log centralization
- [ ] Event validation

### ⏳ Phase 3 — Detection & Incident Simulation
- [ ] Detection rules
- [ ] Alert creation
- [ ] Attack simulations
- [ ] Incident analysis

---

## 🚀 Next Steps

- Integrate FortiGate logs
- Deploy Sysmon
- Create brute-force detection
- Build SOC use cases

---

## 👨‍💻 Author

Personal project developed for hands-on learning in:

SOC • Blue Team • Threat Detection • Incident Response
