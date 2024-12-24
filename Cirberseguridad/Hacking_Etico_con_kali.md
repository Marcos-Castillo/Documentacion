# Guía Completa para Hacking Ético con Kali Linux

## Introducción
El hacking ético es el proceso de evaluar la seguridad de un sistema informático o red de manera legítima y autorizada, utilizando herramientas y técnicas similares a las que usaría un atacante malintencionado.

### Objetivos
- Identificar y mitigar vulnerabilidades.
- Proteger sistemas contra ataques reales.
- Documentar hallazgos en un informe profesional.

---

## Configuración Inicial

### Instalación de Kali Linux
1. **Descarga:** Obtén la ISO desde [kali.org](https://www.kali.org/).
2. **Instalación:**
   - Usa VirtualBox o VMware para configurar una máquina virtual.
   - Alternativamente, instala en hardware dedicado o en un entorno dual boot.
3. **Actualización del sistema:**
   ```bash
   sudo apt update && sudo apt upgrade -y
   ```

### Herramientas Clave en Kali Linux
- **Nmap:** Escaneo de redes y puertos.
- **Metasploit:** Marco de explotación.
- **Burp Suite:** Pruebas de seguridad en aplicaciones web.
- **Wireshark:** Análisis de tráfico de red.
- **Nikto:** Escaneo de vulnerabilidades en servidores web.

---

## Realización de Pruebas de Penetración

### 1. Reconocimiento
1. **Recopilación de información pasiva:**
   - Usar herramientas como `whois`, `theHarvester` o búsquedas manuales.
2. **Recopilación de información activa:**
   - Escaneo de puertos y servicios con Nmap:
     ```bash
     nmap -A -T4 <IP>
     ```

### 2. Escaneo de Vulnerabilidades
1. **Identificación de servicios vulnerables:**
   - Usa Nikto para escanear un servidor web:
     ```bash
     nikto -h <IP>
     ```
2. **Análisis de aplicaciones web:**
   - Configura Burp Suite para capturar y manipular tráfico HTTP/HTTPS.

### 3. Explotación
1. **Uso de Metasploit:**
   - Busca y configura un exploit:
     ```bash
     msfconsole
     search <vulnerabilidad>
     use <exploit>
     set RHOST <IP>
     exploit
     ```
2. **Obtención de acceso remoto:**
   - Configura payloads personalizados con herramientas como `msfvenom`.

### 4. Post-explotación
1. **Elevación de privilegios:**
   - Usa scripts de enumeración como `LinPEAS` o `WinPEAS`.
2. **Mantenimiento de acceso:**
   - Configura puertas traseras temporales para pruebas controladas.

---

## Generación del Informe de Vulnerabilidades

### Estructura del Informe
1. **Resumen Ejecutivo:**
   - Breve descripción de las pruebas y resultados.
2. **Detalles Técnicos:**
   - Lista de vulnerabilidades encontradas.
   - Evidencia de las pruebas realizadas (capturas, logs, etc.).
3. **Recomendaciones:**
   - Propuestas para mitigar cada vulnerabilidad.

### Herramientas para Documentar
- Usa plantillas en Markdown o procesadores como LibreOffice.
- Genera capturas de pantalla con `scrot` o `gnome-screenshot` para incluir evidencia visual.

---

## Manual para el Uso de Aplicaciones Requeridas

### 1. Nmap
- **Escaneo básico:**
  ```bash
  nmap <IP>
  ```
- **Detección de servicios y versiones:**
  ```bash
  nmap -sV <IP>
  ```

### 2. Metasploit
- **Iniciar consola:**
  ```bash
  msfconsole
  ```
- **Buscar exploits:**
  ```bash
  search <vulnerabilidad>
  ```

### 3. Burp Suite
- Configura el proxy para capturar tráfico HTTP.
- Usa el módulo "Repeater" para modificar y reenviar solicitudes.

### 4. Wireshark
- Selecciona una interfaz y comienza a capturar.
- Usa filtros como `http` o `tcp.port == 80` para enfocar el análisis.

### 5. Nikto
- Escaneo de vulnerabilidades en servidores web:
  ```bash
  nikto -h <IP>
  ```

---

## Buenas Prácticas
- Obtén siempre autorización previa para realizar pruebas.
- Mantén un registro detallado de las acciones realizadas.
- Asegúrate de limpiar cualquier configuración o acceso creado durante las pruebas.

---

**Descarga esta guía para comenzar con tus pruebas de hacking ético.**
