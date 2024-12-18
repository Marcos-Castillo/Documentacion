[← Inicio](./README.md)

------
# Manual de Git y GitHub

## Índice

1. [Introducción](#introduccion)
2. [Configuración Inicial](#configuracion-inicial)
3. [Comandos Básicos](#comandos-basicos)
4. [Ramas y Control de Versiones](#ramas-y-control-de-versiones)
5. [Trabajo con GitHub](#trabajo-con-github)
6. [Buenas Prácticas](#buenas-practicas)

---

## Introducción

Git es un sistema de control de versiones distribuido que permite a los desarrolladores colaborar, rastrear cambios y gestionar código de manera eficiente. GitHub, por su parte, es una plataforma basada en la nube que facilita el almacenamiento remoto de repositorios Git y ofrece herramientas para la colaboración y la gestión de proyectos.

**Ventajas de usar Git y GitHub:**
- Seguimiento de cambios en el código.
- Colaboración entre equipos.
- Almacenamiento seguro en la nube.
- Integración con otras herramientas de desarrollo.

---

## Configuración Inicial

Antes de comenzar a usar Git y GitHub, es necesario realizar algunas configuraciones básicas:

1. **Instalar Git:** Descarga e instala Git desde [git-scm.com](https://git-scm.com/).

2. **Configurar usuario y correo:**
   ```bash
   git config --global user.name "Tu Nombre"
   git config --global user.email "tuemail@example.com"
   ```

3. **Verificar configuración:**
   ```bash
   git config --list
   ```

---

## Comandos Básicos

### Inicializar un repositorio
Crea un nuevo repositorio en el directorio actual:
```bash
git init
```

### Clonar un repositorio
Copia un repositorio remoto a tu máquina local:
```bash
git clone <URL-del-repositorio>
```

### Ver el estado del repositorio
Muestra los cambios en el repositorio:
```bash
git status
```

### Agregar cambios al área de preparación (staging)
Selecciona los archivos para incluir en el próximo commit:
```bash
git add <archivo>
```
Para agregar todos los archivos:
```bash
git add .
```

### Realizar un commit
Guarda los cambios en el repositorio local:
```bash
git commit -m "Mensaje del commit"
```

### Ver el historial de commits
Muestra los commits realizados:
```bash
git log
```

---

## Ramas y Control de Versiones

### Crear una rama
Crea una nueva rama:
```bash
git branch <nombre-rama>
```

### Cambiar a otra rama
Cambia a una rama existente:
```bash
git checkout <nombre-rama>
```

### Fusionar ramas
Une una rama a la rama actual:
```bash
git merge <nombre-rama>
```

### Eliminar una rama
Borra una rama que ya no se necesita:
```bash
git branch -d <nombre-rama>
```

---

## Trabajo con GitHub

### Subir un repositorio local a GitHub
1. Crea un repositorio en GitHub.
2. Vincula el repositorio local con el remoto:
   ```bash
   git remote add origin <URL-del-repositorio>
   ```
3. Sube los cambios:
   ```bash
   git push -u origin main
   ```

### Obtener cambios del repositorio remoto
Actualiza el repositorio local con los cambios remotos:
```bash
git pull origin main
```

### Colaboración con pull requests
1. Crea una rama para trabajar en una nueva funcionalidad.
2. Realiza los cambios y haz commits.
3. Sube la rama al repositorio remoto:
   ```bash
   git push origin <nombre-rama>
   ```
4. En GitHub, crea un pull request desde la rama creada hacia `main`.

---

## Buenas Prácticas

1. **Commits claros y frecuentes:** Haz commits pequeños con mensajes descriptivos.
2. **Uso de ramas:** Trabaja en ramas para mantener el código organizado.
3. **Actualiza regularmente:** Mantén tu rama sincronizada con `main` para evitar conflictos.
4. **Revisiones de código:** Realiza pull requests para que otros revisen tus cambios antes de fusionarlos.
5. **Ignorar archivos innecesarios:** Usa un archivo `.gitignore` para excluir archivos o carpetas que no deban ser rastreados.

Ejemplo de `.gitignore`:
```
/node_modules
.env
*.log
```

---

Con este manual básico, estás listo para comenzar a trabajar con Git y GitHub de manera eficiente y colaborativa.
