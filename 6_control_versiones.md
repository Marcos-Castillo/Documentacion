[← Inicio](./README.md)

------

# Control de Versiones con Git

Git es una herramienta esencial para el control de versiones que permite a los desarrolladores gestionar y realizar un seguimiento de los cambios en el código a lo largo del tiempo. Facilita la colaboración entre múltiples desarrolladores y asegura que el código se mantenga organizado y accesible.

## Flujos de Trabajo

- **Git Flow**: Es un modelo de ramificación que define roles específicos para cada rama. Este flujo de trabajo ayuda a organizar las tareas de desarrollo en función de las diferentes etapas del ciclo de vida del desarrollo de software. Incluye ramas como:
  - **master**: La rama principal que contiene el código en producción.
  - **develop**: La rama donde se integra el desarrollo de nuevas funcionalidades antes de ser fusionadas en la rama principal.
  - **feature**: Ramas dedicadas a desarrollar nuevas características.
  - **release**: Ramas que preparan el código para una nueva versión.
  - **hotfix**: Ramas que permiten corregir errores críticos en la rama principal.

## Manejo de Ramas

Crea ramas para nuevas funcionalidades y corrige errores sin afectar el código principal. El uso de ramas permite trabajar en paralelo y facilita la integración de cambios.

**Usos:**  
- Aislar el trabajo en características específicas.
- Realizar pruebas sin interrumpir el flujo de trabajo principal.
- Facilitar la revisión de código mediante pull requests.

**Ejemplo:**  
Imagina que estás trabajando en una nueva funcionalidad de usuario. En lugar de trabajar directamente en la rama principal, creas una nueva rama llamada `feature/user-profile`, donde puedes hacer todos los cambios necesarios sin afectar el código en producción. Una vez que terminas, puedes fusionar esta rama de nuevo en `develop` después de la revisión.

## Resolución de Conflictos

Aprende a resolver conflictos de manera efectiva para mantener la integridad del código. Los conflictos pueden surgir cuando múltiples desarrolladores realizan cambios en la misma línea de código o en archivos relacionados.

**Usos:**  
- Garantizar que el código final sea una combinación correcta de los cambios realizados por diferentes desarrolladores.
- Mantener el historial del proyecto limpio y comprensible.

**Ejemplo:**  
Si dos desarrolladores modifican el mismo archivo y Git no puede decidir cuál es la versión correcta, marcará el archivo como en conflicto. Los desarrolladores deben revisar los cambios y decidir cómo fusionarlos, ya sea eligiendo una versión, combinando ambos cambios o creando una nueva solución.

## Comandos Comunes de Git

Aquí hay una lista de algunos de los comandos más comunes en Git junto con sus descripciones:

1. **git init**  
   Inicializa un nuevo repositorio Git en el directorio actual.

2. **git clone [url]**  
   Crea una copia local de un repositorio remoto.

3. **git add [archivo]**  
   Agrega cambios en el archivo especificado al área de preparación (staging area).

4. **git commit -m "mensaje"**  
   Guarda los cambios en el repositorio con un mensaje descriptivo.

5. **git status**  
   Muestra el estado actual del repositorio, incluyendo archivos modificados y no rastreados.

6. **git push**  
   Envía los cambios locales al repositorio remoto.

7. **git pull**  
   Descarga y fusiona cambios del repositorio remoto en la rama actual.

8. **git branch**  
   Lista todas las ramas en el repositorio, indicando la rama actual.

9. **git checkout [rama]**  
   Cambia a la rama especificada.

10. **git merge [rama]**  
    Fusiona la rama especificada en la rama actual.

11. **git log**  
    Muestra el historial de commits en el repositorio.

12. **git revert [commit]**  
    Crea un nuevo commit que deshace los cambios de un commit anterior.

    [Manual de Git y GitHub](./Manual_de_Git_y_GitHub.md)

Al dominar estos conceptos y comandos de Git, los desarrolladores pueden trabajar de manera más eficiente y colaborar de manera efectiva en proyectos de software.
