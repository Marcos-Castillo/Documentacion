[← Inicio](./README.md)

------

# Seguridad en el Desarrollo de Software

La seguridad es clave en el desarrollo de software. A medida que las aplicaciones se vuelven más complejas y se integran en entornos en línea, la protección contra amenazas y vulnerabilidades se convierte en una prioridad fundamental.

## OWASP Top 10
El **OWASP Top 10** es una lista de las vulnerabilidades más críticas en aplicaciones web, que se actualiza periódicamente. Las vulnerabilidades identificadas en esta lista son comunes y pueden ser explotadas por atacantes si no se toman las medidas adecuadas. A continuación, se presentan algunas de estas vulnerabilidades y sus soluciones:

1. **Inyección**: Ocurre cuando un atacante puede insertar código malicioso en una consulta.  
   - **Ejemplo**: Un atacante envía una entrada SQL maliciosa a través de un formulario para obtener acceso no autorizado a la base de datos.  
   - **Solución**: Usa consultas preparadas o procedimientos almacenados para evitar la inyección de SQL.

2. **Autenticación Rota**: Las aplicaciones que no manejan correctamente la autenticación pueden permitir a los atacantes comprometer cuentas de usuario.  
   - **Ejemplo**: Uso de contraseñas débiles o falta de bloqueo de cuentas tras múltiples intentos fallidos.  
   - **Solución**: Implementa políticas de contraseñas fuertes y mecanismos de bloqueo de cuenta.

3. **Exposición de Datos Sensibles**: Cuando una aplicación no protege adecuadamente los datos sensibles, como contraseñas o información personal.  
   - **Ejemplo**: Almacenar contraseñas en texto claro en una base de datos.  
   - **Solución**: Usa algoritmos de hash seguros y cifrado para proteger datos sensibles.

4. **XML External Entities (XXE)**: Este ataque involucra la inclusión de entidades externas en documentos XML.  
   - **Ejemplo**: Un atacante puede cargar archivos confidenciales del sistema.  
   - **Solución**: Deshabilita la carga de entidades externas en los analizadores XML.

5. **Control de Acceso Roto**: Ocurre cuando los usuarios pueden acceder a recursos o funciones que no deberían estar permitidos.  
   - **Ejemplo**: Un usuario estándar accede a la página de administración.  
   - **Solución**: Implementa controles de acceso robustos y verifica los permisos en cada solicitud.

## Autenticación y Autorización
La **autenticación** se refiere al proceso de verificar la identidad de un usuario, mientras que la **autorización** determina qué recursos puede acceder un usuario autenticado. Para gestionar la autenticación y autorización de manera segura, se recomienda el uso de protocolos como **OAuth** y **JWT** (JSON Web Tokens).

- **OAuth**: Es un protocolo de autorización que permite a los usuarios conceder acceso a sus recursos en un servidor a aplicaciones de terceros sin compartir credenciales.  
  - **Uso**: Cuando una aplicación necesita acceso a datos en otra aplicación (por ejemplo, permitir que una app de gestión de redes sociales publique en nombre del usuario).  
  - **Ejemplo**: Iniciar sesión en una aplicación usando una cuenta de Google.

- **JWT (JSON Web Tokens)**: Es un estándar abierto que define un método compacto y autónomo para transmitir información segura entre partes como un objeto JSON.  
  - **Uso**: Comúnmente utilizado para la autenticación en aplicaciones web y móviles.  
  - **Ejemplo**: Tras iniciar sesión, un servidor emite un JWT que el cliente almacena y envía en futuras solicitudes para demostrar su identidad.

## Prevención de Ataques

### SQL Injection
La **inyección SQL** es una técnica que permite a un atacante interferir con las consultas que una aplicación realiza a su base de datos. Puede permitir al atacante acceder a datos sensibles, modificar o eliminar registros.

- **Cómo funciona**: Si una aplicación construye consultas SQL mediante la concatenación de cadenas, un atacante puede inyectar código SQL malicioso.  
- **Ejemplo**: Un formulario que permite a un usuario ingresar su nombre de usuario. Si la consulta se construye de la siguiente manera: 
  `SELECT * FROM usuarios WHERE nombre_usuario = 'input_usuario';`  
  Un atacante podría ingresar `admin' --` para alterar la consulta y obtener acceso a la cuenta de administrador.
  
- **Solución**: Validar y escapar entradas del usuario. Utilizar consultas preparadas y ORM (Object-Relational Mapping).

### XSS (Cross-Site Scripting)
El **Cross-Site Scripting (XSS)** es una vulnerabilidad que permite a un atacante inyectar scripts maliciosos en páginas web vistas por otros usuarios.

- **Cómo funciona**: Un atacante puede insertar scripts en contenido dinámico que se muestra a otros usuarios.  
- **Ejemplo**: Un comentario en un blog que contiene un script que roba cookies de sesión.
  
- **Solución**: Escapar todas las salidas que se muestran en el navegador y utilizar Content Security Policy (CSP) para limitar qué scripts pueden ejecutarse.

### CSRF (Cross-Site Request Forgery)
El **Cross-Site Request Forgery (CSRF)** es un ataque que permite a un atacante inducir a un usuario autenticado a ejecutar acciones no deseadas en una aplicación web.

- **Cómo funciona**: Un atacante engaña a un usuario para que realice una acción no intencionada, como cambiar su dirección de correo electrónico o realizar un pago.  
- **Ejemplo**: Un correo electrónico que contiene un enlace malicioso que, al hacer clic, realiza una acción en el banco en línea del usuario sin su conocimiento.
  
- **Solución**: Usar tokens de verificación únicos para formularios. Esto garantiza que la solicitud provenga de la fuente legítima.

---

Recuerda que la seguridad es un proceso continuo y siempre es necesario estar al tanto de las mejores prácticas y las nuevas vulnerabilidades que puedan surgir.
