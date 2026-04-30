# 🖥️ Proxmox VE - Hypervisor Setup

## 🎯 Objetivo

Implementar un hypervisor basado en Proxmox VE para la virtualización de todos los sistemas del laboratorio SOC, permitiendo la creación y gestión de máquinas virtuales en un entorno segmentado.

---

## 🧱 Entorno

- Plataforma: Proxmox VE
- Tipo: Bare Metal
- Equipo: Mini PC
- Storage: Local-LVM
- Red: VLAN 9 (MANAGEMENT)
- IP: 192.168.9.2

---

## ⚙️ Implementación

### 1. Instalación de Proxmox VE

- Descarga de la ISO oficial
- Instalación en bare metal
- Configuración inicial de red

📸
![Instalación Proxmox](docs/screenshots/proxmox/1.png)

---

### 2. Acceso a la interfaz web

Acceso vía navegador:
https://192.168.18.2:8006

📸
![Web UI](https://github.com/FUZHIXx/Homelab-SOC/blob/5e27cf706793d8c04f5e92464ae4bbcd671c458b/docs/screenshots/proxmox/9.png)

---

### 3. Configuración de red

- Asignación de IP estática en VLAN de management  
- Configuración de bridge de red (`vmbr0`)  
- Asociación del bridge a la interfaz física  
- Conexión hacia FortiGate para segmentación por VLAN
- 
📸
![Network Config](https://github.com/FUZHIXx/Homelab-SOC/blob/719af60edb8032c438942ede09b3850235de7664/docs/screenshots/proxmox/10.png)

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

- Acceso al panel web vía HTTPS  
- Máquinas virtuales operativas  
- Conectividad verificada mediante ping entre VMs  
- Comunicación exitosa con gateway (FortiGate)
  

---

## 🧠 Notas

- Se utilizó bridge para permitir comunicación con FortiGate  
- Se recomienda mantener Proxmox en VLAN de management  
- Acceso restringido solo a red administrativa  

---

## 🔐 Consideraciones de seguridad

- Acceso restringido a la VLAN de management    
- Recomendado cambiar credenciales por defecto  
- Posible implementación futura de autenticación adicional
  
---

## 🔗 Relación con el SOC

Proxmox es la base del laboratorio, permitiendo:

- Despliegue de infraestructura SOC  
- Aislamiento de entornos (LAB, SERVERS, SOC)  
- Simulación de entornos empresariales virtualizados  
