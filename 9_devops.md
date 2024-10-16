[← Inicio](./README.md)

------

# DevOps y CI/CD: Herramientas y Prácticas

DevOps es un conjunto de prácticas que mejora la colaboración entre los equipos de desarrollo y operaciones, permitiendo una entrega continua y una mayor eficiencia en el ciclo de vida del software. La integración continua (CI) y el despliegue continuo (CD) son componentes clave que ayudan a automatizar y mejorar la calidad del software.

## Automatización del Despliegue

Usa herramientas de CI/CD para automatizar el proceso de despliegue. La automatización permite que los cambios en el código sean probados y desplegados de manera rápida y fiable, reduciendo el riesgo de errores humanos y asegurando que el software se mantenga en un estado desplegable en todo momento.

**Usos:**
- Acelera el proceso de lanzamiento de nuevas características.
- Permite la realización de pruebas automáticas, asegurando que cada cambio sea validado.
- Facilita la retroalimentación continua, ayudando a los desarrolladores a identificar y corregir problemas rápidamente.

**Ejemplo:**
Un equipo de desarrollo que utiliza CI/CD puede configurar un pipeline donde cada vez que se realiza un commit en la rama principal, se ejecutan automáticamente pruebas unitarias. Si todas las pruebas pasan, el código se despliega en un entorno de staging, donde los testers pueden verificar la funcionalidad antes de que llegue a producción.

## Herramientas

- **Jenkins**: 
  - Herramienta de automatización de CI/CD ampliamente utilizada. Permite a los desarrolladores automatizar tareas relacionadas con el desarrollo y el despliegue de aplicaciones.
  - **Usos:** Configuración de pipelines, integración con múltiples herramientas, soporte para notificaciones y análisis de calidad de código.
  
- **GitLab CI**: 
  - Integración continua y despliegue integrado en GitLab. Facilita la creación de pipelines que se ejecutan con cada push al repositorio.
  - **Usos:** Permite la definición de trabajos en archivos YAML, integración con otras herramientas de desarrollo y gestión de versiones.

## Contenedores con Docker

Usa Docker para crear entornos de desarrollo y producción consistentes. Docker permite a los desarrolladores empaquetar aplicaciones y sus dependencias en contenedores, lo que garantiza que se ejecuten de la misma manera en diferentes entornos.

**Usos:**
- Facilita la creación de entornos de desarrollo replicables.
- Permite el despliegue de aplicaciones en cualquier sistema que soporte Docker, sin preocuparse por conflictos de dependencias.
- Acelera el proceso de configuración de entornos, eliminando la necesidad de configurar manualmente servidores.

**Ejemplo:**
Un desarrollador puede crear un archivo `Dockerfile` que defina la imagen de su aplicación. Al ejecutar el comando `docker build`, se construye una imagen que puede ser desplegada en cualquier servidor con Docker. Esto elimina la preocupación de que la aplicación funcione de manera diferente en entornos de desarrollo y producción.

## Comandos Comunes de Docker

Aquí hay una lista de algunos de los comandos más comunes de Docker junto con sus descripciones:

1. **docker build [opciones] .**  
   Crea una imagen Docker a partir de un Dockerfile en el directorio actual.

2. **docker run [opciones] [imagen]**  
   Ejecuta un contenedor a partir de una imagen especificada.

3. **docker ps**  
   Lista todos los contenedores en ejecución.

4. **docker ps -a**  
   Lista todos los contenedores, incluidos los que no están en ejecución.

5. **docker stop [nombre_contenedor]**  
   Detiene un contenedor en ejecución.

6. **docker rm [nombre_contenedor]**  
   Elimina un contenedor detenido.

7. **docker rmi [nombre_imagen]**  
   Elimina una imagen Docker.

8. **docker exec -it [nombre_contenedor] [comando]**  
   Ejecuta un comando dentro de un contenedor en ejecución.

9. **docker logs [nombre_contenedor]**  
   Muestra los logs de un contenedor específico.

10. **docker-compose up**  
    Inicia todos los contenedores definidos en un archivo `docker-compose.yml`.

Al dominar estas herramientas y prácticas, los equipos de desarrollo pueden mejorar significativamente su eficiencia y la calidad del software entregado, facilitando una cultura de mejora continua.
