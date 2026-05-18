# 📊 Wazuh SIEM - Installation & Setup

## 🎯 Objetivo

Implementar un SIEM basado en Wazuh para centralizar, analizar y correlacionar logs de seguridad provenientes de diferentes sistemas dentro del laboratorio SOC.

---

## 🧱 Entorno

- Plataforma: Wazuh  
- OS: Ubuntu Server  
- Red: VLAN 140 (SOC)  
- IP: 172.168.140.10  
- RAM: 4 GB | vCPU: 2 | Disk: 40 GB  

---

## ⚙️ Implementación

### 1. Creación de la máquina virtual

- VM creada en Proxmox  
- Recursos asignados para procesamiento de logs  

📸  
![VM Creation](../screenshots/wazuh/vm.png)

---

### 2. Instalación de Wazuh

Se utiliza el instalador oficial para desplegar todos los componentes:

```bash
curl -sO https://packages.wazuh.com/4.x/wazuh-install.sh
sudo bash wazuh-install.sh -a
```

Este comando instala:

- Wazuh Manager  
- Wazuh Indexer  
- Wazuh Dashboard  

---

### 3. Acceso a la interfaz web

Acceso vía navegador:

https://172.168.140.10

📸  
![Dashboard](../screenshots/wazuh/dashboard.png)

---

### 4. Verificación de servicios

Se valida que los servicios estén activos:

```bash
systemctl status wazuh-manager
systemctl status wazuh-indexer
systemctl status wazuh-dashboard
```

---

## 📸 Evidencia

- Acceso al dashboard funcional  
- Servicios activos  
- Interfaz cargando correctamente  

---

## ✅ Validación

- Acceso al dashboard vía HTTPS  
- Servicios de Wazuh ejecutándose correctamente  
- Sistema listo para recibir agentes  
- Sin errores en servicios principales  

---

## 🔐 Consideraciones de seguridad

- Acceso restringido a VLAN SOC  
- Uso de HTTPS para el dashboard  
- Configuración de credenciales seguras  
- Recomendado limitar acceso solo a red de administración  

---

## 📊 Rol dentro del SOC

Wazuh actúa como el núcleo del SOC, permitiendo:

- Centralización de logs  
- Correlación de eventos  
- Generación de alertas  
- Visibilidad del entorno  

---

## 🧠 Notas

- Se recomienda ubicar el SIEM en una red separada (SOC)  
- El rendimiento depende de recursos asignados  
- Base para detección y análisis de incidentes  

---

## 🔗 Relación con el SOC

Este componente permite:

- Monitorear toda la infraestructura  
- Detectar actividades sospechosas  
- Analizar eventos de seguridad  
- Preparar el entorno para respuesta a incidentes  
