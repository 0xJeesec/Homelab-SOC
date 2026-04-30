# 🏢 Active Directory - Domain Controller Setup

## 🎯 Objetivo

Implementar un controlador de dominio basado en Windows Server para centralizar la autenticación, gestión de usuarios y políticas de seguridad dentro del entorno del laboratorio SOC.

---

## 🧱 Entorno

- OS: Windows Server 2022  
- Rol: Domain Controller (AD DS, DNS)  
- Red: VLAN 120 (SERVERS)  
- IP: 172.168.120.10  
- RAM: 8 GB | vCPU: 2 | Disk: 40 GB  

---

## ⚙️ Implementación

### 1. Creación de la máquina virtual

- VM creada en Proxmox  
- Recursos asignados según necesidades del entorno  

📸
![VM Creation](../screenshots/ad/vm.png)

---

### 2. Configuración inicial del sistema

- Asignación de IP estática  
- Configuración de nombre del servidor  
- Verificación de conectividad  

📸
![Network Config](../screenshots/ad/network.png)

---

### 3. Instalación de Active Directory

- Instalación del rol **Active Directory Domain Services (AD DS)**  
- Promoción del servidor a **Domain Controller**

📸
![AD Installation](../screenshots/ad/ad-install.png)

---

### 4. Configuración del dominio

- Creación del dominio (ej: `lab.local`)  
- Configuración automática del servicio DNS  

📸
![Domain Setup](../screenshots/ad/domain.png)

---

### 5. Creación de usuarios y estructura

- Creación de usuarios de prueba  
- Organización en unidades organizativas (OU)  

📸
![Users](../screenshots/ad/users.png)

---

### 6. Configuración de políticas (GPO)

- Aplicación de políticas básicas de seguridad  
- Restricciones y configuraciones de entorno  

📸
![GPO](../screenshots/ad/gpo.png)

---

## 📸 Evidencia

- Dominio activo y funcional  
- Usuarios creados  
- Políticas aplicadas  
- DNS resolviendo correctamente  

---

## ✅ Validación

- Inicio de sesión exitoso desde cliente unido al dominio  
- Resolución DNS funcionando correctamente  
- Aplicación de GPO en el endpoint  
- Comunicación con el controlador de dominio  

---

## 🔐 Consideraciones de seguridad

- Uso de políticas (GPO) para control de acceso  
- Centralización de autenticación  
- Base para monitoreo de eventos de seguridad  

---

## 📊 Logs relevantes para el SOC

Active Directory genera eventos clave que serán enviados al SIEM:

- Event ID 4624 → Inicio de sesión exitoso  
- Event ID 4625 → Intento fallido (brute force)  
- Event ID 4720 → Creación de usuario  
- Event ID 4732 → Agregado a grupo  

👉 Estos eventos son fundamentales para detección de amenazas.

---

## 🧠 Notas

- El servidor utiliza IP estática para estabilidad de red  
- El DNS debe apuntar al controlador de dominio  
- Base fundamental para autenticación en el entorno  

---

## 🔗 Relación con el SOC

Active Directory es una de las principales fuentes de logs en un SOC:

- Permite detectar accesos sospechosos  
- Facilita el análisis de actividad de usuarios  
- Proporciona visibilidad sobre autenticación y cambios en el sistema  
