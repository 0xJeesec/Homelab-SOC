# 🛡️ Homelab SOC / Blue Team

![Status](https://img.shields.io/badge/project-active-brightgreen)
![Platform](https://img.shields.io/badge/platform-Proxmox-orange)
![Focus](https://img.shields.io/badge/focus-SOC-blue)
![Type](https://img.shields.io/badge/type-homelab-blue)

Proyecto personal enfocado en la construcción y simulación de un entorno empresarial orientado a un Security Operations Center (SOC). Este laboratorio está diseñado para desarrollar y demostrar habilidades prácticas en ciberseguridad defensiva, monitoreo, detección y análisis de amenazas.

El objetivo principal es construir un entorno funcional que permita trabajar con tecnologías utilizadas en escenarios reales de Blue Team y SOC.

---

## 🎯 Objetivo

Diseñar e implementar un laboratorio orientado a operaciones de seguridad (SOC) para simular escenarios reales mediante:

- Segmentación de red y control de tráfico
- Implementación de Active Directory
- Centralización y análisis de logs
- Detección y monitoreo de amenazas
- Simulación de incidentes
- Hardening de infraestructura
- Casos prácticos de seguridad defensiva

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
| TEKEN-DC01 | Active Directory Domain Controller |
| OUVI-WS01 | Endpoint Windows |
| PALANTIR-SIEM | Wazuh SIEM |
| HYDRA-LAB01 | Máquina vulnerable |

---

## 🌐 Diseño de red

| VLAN | Nombre | Función |
|---|---|---|
| 9 | MANAGEMENT | Administración |
| 110 | ENDPOINTS | Equipos de usuarios |
| 120 | SERVERS | Infraestructura |
| 130 | LAB | Sistemas vulnerables |
| 140 | SOC | Monitoreo y SIEM |

---

## ⚙️ Tecnologías utilizadas

### Infraestructura

- Proxmox VE
- FortiGate
- Managed Switch

### Sistemas

- Windows Server 2019
- Windows 10 LTSC
- Active Directory

### Monitoreo y seguridad

- Wazuh
- Sysmon *(próximamente)*
- Event Viewer
- Windows Security Logs

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
│
├── incidents/
│
└── screenshots/

---

## 📚 Documentación técnica

### Infraestructura

- Proxmox VE
- FortiGate
- Switch

### Sistemas

- Active Directory
- Windows Client

### SIEM

- Wazuh Installation
- Agent Integration
- Log Ingestion

### Detección

- Casos de uso
- Reglas
- Alertas

### Respuesta a incidentes

- Timeline
- Investigación
- Mitigación

---

## 📊 Estado del proyecto

### ✅ Completado

- Implementación de Proxmox
- Configuración de FortiGate
- Segmentación mediante VLANs
- Active Directory
- Integración de Windows Client
- Instalación de Wazuh

### 🔄 En progreso

- Integración de agentes Wazuh
- Centralización de logs
- Casos de detección

### ⏳ Próximas fases

- Integración de Sysmon
- Detección de ataques
- Dashboards
- Hardening
- Respuesta a incidentes

---

## 🚀 Próximos pasos

- Integración de logs de FortiGate
- Implementación de Sysmon
- Detección de brute force
- Creación de alertas
- Simulación de ataques controlados
- Casos de uso SOC

---

## 👨‍💻 Autor

Proyecto desarrollado como parte del aprendizaje práctico y fortalecimiento de habilidades en:

- SOC
- Blue Team
- Threat Detection
- Incident Response
- Defensive Security

GitHub:
https://github.com/FUZHIXx
"""
