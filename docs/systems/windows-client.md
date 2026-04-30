# 💻 Windows Client - Domain Integration

## 🎯 Objetivo

Implementar un endpoint Windows dentro del dominio para simular el comportamiento de un usuario corporativo, generar actividad real y servir como fuente de logs para el SIEM.

---

## 🧱 Entorno

- OS: Windows 10 LTSC  
- Rol: Endpoint corporativo  
- Red: VLAN 110 (ENDPOINTS)  
- IP: Asignada por DHCP  
- RAM: 4 GB | vCPU: 2 | Disk: 40 GB  

---

## ⚙️ Implementación

### 1. Creación de la máquina virtual

- VM creada en Proxmox  
- Recursos asignados según entorno  

📸
![VM Creation](../screenshots/client/vm.png)

---

### 2. Configuración de red

- Obtención de IP mediante DHCP  
- Verificación de conectividad con el dominio  

📸
![Network](../screenshots/client/network.png)

---

### 3. Configuración de DNS

- DNS configurado apuntando al Domain Controller  
- Validación de resolución de dominio  

📸
![DNS](../screenshots/client/dns.png)

---

### 4. Unión al dominio

- Unión al dominio (`lab.local`)  
- Reinicio del sistema  

📸
![Domain Join](../screenshots/client/domain-join.png)

---

### 5. Inicio de sesión con usuario de dominio

- Login con usuario creado en AD  

📸
![Login](../screenshots/client/login.png)

---

### 6. Aplicación de políticas (GPO)

- Validación de políticas aplicadas desde AD  

📸
![GPO](../screenshots/client/gpo.png)

---

## 📸 Evidencia

- Equipo unido al dominio  
- Usuario autenticado correctamente  
- Políticas aplicadas  
- Conectividad con el Domain Controller  

---

## ✅ Validación

- Resolución DNS hacia el dominio  
- Inicio de sesión exitoso con usuario de AD  
- Aplicación de GPO en el sistema  
- Comunicación estable con el servidor  

---

## 🔐 Consideraciones de seguridad

- Uso de autenticación centralizada  
- Aplicación de políticas de seguridad mediante GPO  
- Base para generación de eventos de seguridad  

---

## 📊 Logs relevantes para el SOC

El endpoint genera eventos clave que serán enviados al SIEM:

- Event ID 4624 → Inicio de sesión exitoso  
- Event ID 4625 → Intento fallido  
- Event ID 4688 → Ejecución de procesos  
- Event ID 4719 → Cambios en políticas  

👉 Estos eventos permiten detectar actividad sospechosa en el entorno.

---

## 🧠 Notas

- El DNS debe apuntar siempre al Domain Controller  
- El cliente depende del AD para autenticación  
- Genera actividad normal que sirve como baseline  

---

## 🔗 Relación con el SOC

El Windows Client es fundamental para el SOC:

- Genera eventos de usuario  
- Permite detectar comportamientos anómalos  
- Sirve como punto de origen de incidentes  
- Proporciona datos para análisis en el SIEM  
