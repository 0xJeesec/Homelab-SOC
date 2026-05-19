# 🛡️ Homelab SOC / Blue Team

![Status](https://img.shields.io/badge/project-active-brightgreen)
![Platform](https://img.shields.io/badge/platform-Proxmox-orange)
![Focus](https://img.shields.io/badge/focus-SOC-blue)
![Type](https://img.shields.io/badge/type-homelab-blue)

Proyecto personal orientado a la simulación de un entorno empresarial enfocado en un Security Operations Center (SOC), diseñado para fortalecer habilidades prácticas en infraestructura, monitoreo, detección y análisis de amenazas.

---

## 🎯 Objetivo

Diseñar e implementar un laboratorio orientado a Blue Team para simular escenarios reales de seguridad defensiva mediante:

- Segmentación de red
- Active Directory
- SIEM
- Recolección y análisis de logs
- Detección de amenazas
- Simulación de incidentes
- Hardening

---

## 🏗️ Arquitectura

📸

![Network Diagram](docs/screenshots/architecture/network-diagram.png)

---

## 🧱 Infraestructura

| Componente | Función |
|---|---|
| LORA-PVE | Hypervisor Proxmox |
| ARES-FW | Firewall FortiGate |
| ARES-SW | Switch administrable |
| TEKEN-DC01 | Active Directory |
| OUVI-WS01 | Windows Client |
| PALANTIR-SIEM | Wazuh SIEM |
| HYDRA-LAB01 | Máquina vulnerable |

---

## ⚙️ Tecnologías utilizadas

- Proxmox VE
- FortiGate
- TP-Link Managed Switch
- Windows Server 2019
- Windows 10 LTSC
- Wazuh
- Active Directory
- VLANs
- DNS
- DHCP

---

## 📂 Estructura del proyecto

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
├── incidents/
└── screenshots/

---

## 📊 Estado del proyecto

### ✅ Completado

- Infraestructura base
- Segmentación mediante VLANs
- Active Directory
- Windows Client
- Instalación de Wazuh

### 🔄 En progreso

- Integración de agentes
- Ingesta de logs
- Casos de detección

---

## 🚀 Próximos pasos

- Integración de logs del firewall
- Detección de brute force
- Integración de Sysmon
- Correlación de eventos
- Simulación de ataques controlados

---

## 👨‍💻 Autor

Proyecto desarrollado como parte de aprendizaje práctico en:

- SOC
- Blue Team
- Detección de amenazas
- Ciberseguridad defensiva

GitHub: https://github.com/FUZHIXx
