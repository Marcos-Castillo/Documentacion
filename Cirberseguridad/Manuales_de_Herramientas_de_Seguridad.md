# Manuales de Herramientas de Seguridad

## 1. **Nmap**: Escaneo de redes y detección de puertos abiertos

### Introducción
Nmap (Network Mapper) es una herramienta de código abierto para el escaneo de redes y detección de puertos abiertos en sistemas.

### Instalación
- **Linux:** `sudo apt install nmap`
- **Windows:** Descarga desde [nmap.org](https://nmap.org/download.html).
- **MacOS:** `brew install nmap`

### Uso Básico
1. **Escaneo rápido:**
   ```bash
   nmap <IP>
   ```
2. **Detección de puertos específicos:**
   ```bash
   nmap -p 80,443 <IP>
   ```
3. **Escaneo completo de puertos:**
   ```bash
   nmap -p- <IP>
   ```

### Opciones Avanzadas
- **Detección de servicios y versiones:**
  ```bash
  nmap -sV <IP>
  ```
- **Escaneo de sistema operativo:**
  ```bash
  nmap -O <IP>
  ```
- **Escaneo sigiloso:**
  ```bash
  nmap -sS <IP>
  ```

---

## 2. **Metasploit**: Marco para explotación de vulnerabilidades

### Introducción
Metasploit es un marco para pruebas de penetración y explotación de vulnerabilidades.

### Instalación
- **Linux:**
  ```bash
  curl https://raw.githubusercontent.com/rapid7/metasploit-framework/master/msfupdate | bash
  ```
- **Windows:** Descarga desde [metasploit.com](https://www.metasploit.com/).

### Uso Básico
1. **Iniciar Metasploit:**
   ```bash
   msfconsole
   ```
2. **Buscar exploits:**
   ```bash
   search <vulnerabilidad>
   ```
3. **Configurar un exploit:**
   ```bash
   use <exploit>
   set RHOST <IP>
   set PAYLOAD <payload>
   ```
4. **Ejecutar:**
   ```bash
   exploit
   ```

### Funciones Avanzadas
- **Meterpreter:** Post-explotación con sesiones interactivas.
- **Armitage:** Interfaz gráfica para Metasploit.

---

## 3. **Burp Suite**: Análisis y pruebas de aplicaciones web

### Introducción
Burp Suite es una herramienta utilizada para analizar y probar la seguridad de aplicaciones web.

### Instalación
- Descarga desde [portswigger.net](https://portswigger.net/burp).
- **Linux:** Ejecuta el archivo JAR descargado.
- **Windows/MacOS:** Instaladores disponibles en la página oficial.

### Uso Básico
1. **Configurar el proxy:**
   - Configura tu navegador para usar el proxy de Burp en `127.0.0.1:8080`.
2. **Capturar tráfico HTTP:**
   - Activa la opción "Intercept is on" en el módulo Proxy.
3. **Analizar peticiones:**
   - Usa el módulo "Repeater" para modificar y reenviar peticiones.

### Funciones Avanzadas
- **Escaneo automatizado:**
  Disponible en la versión profesional.
- **Extensiones:**
  Instala plugins desde el "Burp Suite Extender".

---

## 4. **Wireshark**: Análisis de tráfico de red

### Introducción
Wireshark es una herramienta para capturar y analizar paquetes de datos en una red.

### Instalación
- **Linux:** `sudo apt install wireshark`
- **Windows/MacOS:** Descarga desde [wireshark.org](https://www.wireshark.org/download.html).

### Uso Básico
1. **Iniciar Wireshark:**
   - Selecciona una interfaz de red.
2. **Capturar tráfico:**
   - Haz clic en "Start" para comenzar la captura.
3. **Filtrar tráfico:**
   - Usa expresiones como `http`, `tcp.port == 80`, o `ip.src == <IP>`.

### Análisis Avanzado
- **Seguimiento de conexiones TCP:**
  Clic derecho en un paquete > "Follow" > "TCP Stream".
- **Exportar datos:**
  Archivo > Export > Selected Packets.

---

**Descarga este manual en formato Markdown para tu uso.**
