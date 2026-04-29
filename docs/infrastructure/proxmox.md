# 🖥️ Proxmox VE - Hypervisor Setup

## 🎯 Objetivo

Implementar un hypervisor basado en Proxmox VE para la virtualización de todos los sistemas del laboratorio SOC, permitiendo la creación y gestión de máquinas virtuales en un entorno segmentado.

---

## 🧱 Entorno

- Plataforma: Proxmox VE
- Tipo: Bare Metal
- Equipo: Mini PC
- Red: VLAN 9 (MANAGEMENT)
- IP: 192.168.9.2

---

## ⚙️ Implementación

### 1. Instalación de Proxmox VE

- Descarga de la ISO oficial
- Instalación en bare metal
- Configuración inicial de red

📸
![Instalación Proxmox](../screenshots/proxmox/install.png)

---

### 2. Acceso a la interfaz web

Acceso vía navegador:
https://192.168.18.2:8006

📸
![Web UI](../screenshots/proxmox/web-ui.png)

---

### 3. Configuración de red

- Asignación de IP estática
- Configuración del bridge de red (vmbr0)
- Conexión hacia el firewall (FortiGate)

📸
![Network Config](../screenshots/proxmox/network.png)

---

### 4. Creación de máquinas virtuales

- Windows Server (AD)
- Windows Client
- Wazuh SIEM
- Metasploitable

📸
![VM List](../screenshots/proxmox/vms.png)

---

## 📸 Evidencia

- Acceso funcional al panel web  
- Máquinas virtuales creadas correctamente  
- Conectividad de red estable  

---

## ✅ Validación

- Acceso al panel web sin errores  
- VMs encendidas correctamente  
- Comunicación entre máquinas dentro de la red  

---

## 🧠 Notas

- Se utilizó bridge para permitir comunicación con FortiGate  
- Se recomienda mantener Proxmox en VLAN de management  
- Acceso restringido solo a red administrativa  

---

## 🔗 Relación con el SOC

Proxmox es la base del laboratorio, permitiendo:

- Despliegue de infraestructura SOC  
- Aislamiento de entornos (LAB, SERVERS, SOC)  
- Simulación de entornos empresariales virtualizados  
