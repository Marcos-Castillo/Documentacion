[← Inicio](./README.md)

------

# Patrones de Diseño: Guía Simplificada

# Índice

1. [Patrones Creacionales](#patrones-creacionales)
   1. [Factory Method](#factory-method)
   2. [Abstract Factory](#abstract-factory)
   3. [Builder](#builder)
   4. [Prototype](#prototype)
   5. [Singleton](#singleton)
   
2. [Patrones Estructurales](#patrones-estructurales)
   1. [Adapter](#adapter)
   2. [Bridge](#bridge)
   3. [Composite](#composite)
   4. [Decorator](#decorator)
   5. [Facade](#facade)
   6. [Flyweight](#flyweight)
   7. [Proxy](#proxy)
   
3. [Patrones de Comportamiento](#patrones-de-comportamiento)
   1. [Chain of Responsibility](#chain-of-responsibility)
   2. [Command](#command)
   3. [Iterator](#iterator)
   4. [Mediator](#mediator)
   5. [Memento](#memento)
   6. [Observer](#observer)
   7. [State](#state)
   8. [Strategy](#strategy)
   9. [Template Method](#template-method)
   10. [Visitor](#visitor)

4. [Otros Patrones](#otros-patrones)
   1. [MVC (Modelo-Vista-Controlador)](#mvc-modelo-vista-controlador)
   2. [Microservicios](#microservicios)
   3. [Message Broker](#message-broker)
   4. [Gateway](#gateway)


## Patrones Creacionales
Estos patrones proporcionan mecanismos para la creación de objetos que incrementan la flexibilidad y reutilización del código.

### Factory Method
- **Uso**: Cuando las subclases deben decidir qué clase instanciar.
- **Ejemplo**: Crear diferentes tipos de notificaciones (email, SMS, etc.).
- **Microservicios**: Útil para crear objetos de servicio basados en el contexto.

### Abstract Factory
- **Uso**: Cuando necesitas crear familias de objetos relacionados sin especificar sus clases concretas.
- **Ejemplo**: Generar componentes de UI (botones, cuadros de texto) para diferentes plataformas.
- **Microservicios**: Ayuda a crear diferentes implementaciones de servicios según la infraestructura.

### Builder
- **Uso**: Cuando necesitas construir un objeto complejo paso a paso.
- **Ejemplo**: Construir una casa con características opcionales como puertas, ventanas y techos.
- **Microservicios**: Útil para construir solicitudes HTTP o respuestas complejas en servicios.

### Prototype
- **Uso**: Cuando necesitas clonar un objeto sin depender de su clase concreta.
- **Ejemplo**: Clonar un objeto de configuración para reutilizarlo en varios contextos.
- **Microservicios**: Útil para replicar configuraciones comunes de servicios o datos compartidos.

### Singleton
- **Uso**: Cuando necesitas garantizar que solo exista una instancia de una clase y proporcionar un único punto de acceso.
- **Ejemplo**: Administrar la conexión a una base de datos que debe ser única en una aplicación.
- **Microservicios**: Útil en componentes compartidos como el registro o la gestión de configuración.

## Patrones Estructurales
Estos patrones ayudan a organizar clases y objetos en estructuras más grandes, manteniéndolos flexibles y eficientes.

### Adapter
- **Uso**: Cuando necesitas que dos interfaces incompatibles trabajen juntas.
- **Ejemplo**: Adaptar una clase de pagos para que funcione con diferentes proveedores de tarjetas.
- **Microservicios**: Útil para integrar servicios externos con una API interna.

### Bridge
- **Uso**: Para separar la abstracción de la implementación, permitiendo que ambas evolucionen independientemente.
- **Ejemplo**: Crear una jerarquía de formas (círculo, cuadrado) y separar cómo se dibujan (2D, 3D).
- **Microservicios**: Separa la lógica de negocio de la infraestructura que la soporta.

### Composite
- **Uso**: Para tratar objetos individuales y colecciones de objetos de manera uniforme.
- **Ejemplo**: Estructuras jerárquicas como árboles de archivos donde las carpetas y archivos se manejan de forma similar.
- **Microservicios**: Útil para estructuras de datos jerárquicas en microservicios, como la gestión de dependencias de servicios.

### Decorator
- **Uso**: Añadir responsabilidades adicionales a un objeto de manera dinámica.
- **Ejemplo**: Agregar funcionalidades a un objeto de ventana (como bordes, scroll, etc.).
- **Microservicios**: Se puede usar para agregar funcionalidades adicionales a respuestas o peticiones de servicios sin alterar su estructura original.

### Facade
- **Uso**: Proporcionar una interfaz simplificada para un subsistema complejo.
- **Ejemplo**: Simplificar el uso de un sistema de archivos, bases de datos y redes con una sola interfaz.
- **Microservicios**: Útil cuando un microservicio necesita ocultar la complejidad interna de sus múltiples operaciones detrás de una API simple.

### Flyweight
- **Uso**: Para compartir instancias comunes y evitar duplicación de objetos.
- **Ejemplo**: Reutilizar objetos en un sistema gráfico donde muchos elementos comparten los mismos datos (por ejemplo, caracteres en un editor de texto).
- **Microservicios**: Puede usarse en la gestión de recursos comunes entre microservicios para mejorar la eficiencia.

### Proxy
- **Uso**: Para controlar el acceso a un objeto o agregar funcionalidad antes de acceder a él.
- **Ejemplo**: Un proxy de seguridad que controla el acceso a una base de datos.
- **Microservicios**: Usado en la implementación de gateways para proteger o controlar el acceso a microservicios.

## Patrones de Comportamiento
Estos patrones gestionan la interacción y responsabilidad entre objetos.

### Chain of Responsibility
- **Uso**: Para pasar una petición a lo largo de una cadena de handlers hasta que uno la procese.
- **Ejemplo**: Sistemas de manejo de errores o validación de formularios.
- **Microservicios**: Puede ser útil en cadenas de servicios donde cada uno realiza una tarea y luego pasa la petición al siguiente.

### Command
- **Uso**: Encapsular una operación en un objeto para poder parametrizarla o deshacerla.
- **Ejemplo**: Implementar un sistema de deshacer/rehacer en una aplicación.
- **Microservicios**: Puede usarse para orquestar tareas entre servicios (por ejemplo, en un servicio de pedidos).

### Iterator
- **Uso**: Para recorrer los elementos de una colección sin exponer su representación interna.
- **Ejemplo**: Recorrer una lista de elementos o nodos de un árbol.
- **Microservicios**: Útil para procesar lotes de datos que un servicio devuelve.

### Mediator
- **Uso**: Para centralizar la comunicación entre objetos, evitando dependencias directas.
- **Ejemplo**: Un sistema de chat donde el servidor centraliza la comunicación entre usuarios.
- **Microservicios**: Se puede utilizar en patrones de orquestación de microservicios para coordinar la comunicación.

### Memento
- **Uso**: Guardar y restaurar el estado anterior de un objeto sin violar su encapsulamiento.
- **Ejemplo**: Sistemas de guardar/recuperar estados en videojuegos.
- **Microservicios**: Se puede usar para mantener el estado temporal de una operación compleja en un microservicio.

### Observer
- **Uso**: Para notificar a múltiples objetos cuando el estado de otro cambia.
- **Ejemplo**: Un sistema de notificaciones que actualiza a los observadores cuando hay un cambio.
- **Microservicios**: Ideal para sistemas event-driven o donde se manejan eventos de publicación/suscripción.

### State
- **Uso**: Cambiar el comportamiento de un objeto según su estado interno.
- **Ejemplo**: Un semáforo que cambia su comportamiento según su estado (rojo, verde, amarillo).
- **Microservicios**: Puede ser útil en servicios que cambian su comportamiento según el estado del negocio o de la aplicación.

### Strategy
- **Uso**: Para definir una familia de algoritmos, encapsularlos, e intercambiarlos según la necesidad.
- **Ejemplo**: Diferentes estrategias de ordenación (rápida, burbuja, etc.).
- **Microservicios**: Puede aplicarse en diferentes estrategias de procesamiento de datos o respuestas según las condiciones.

### Template Method
- **Uso**: Definir el esqueleto de un algoritmo, dejando algunos pasos a las subclases.
- **Ejemplo**: Un método de procesamiento de datos donde los detalles específicos se definen en subclases.
- **Microservicios**: Puede ayudar a definir el flujo de operaciones comunes en servicios, permitiendo que los detalles sean específicos por servicio.

### Visitor
- **Uso**: Permitir agregar nuevas operaciones a clases existentes sin modificar su estructura.
- **Ejemplo**: Un sistema de procesamiento de objetos donde se añade nueva funcionalidad (como calculadora de impuestos).
- **Microservicios**: Se puede aplicar para agregar operaciones adicionales a los datos gestionados por microservicios sin cambiar la lógica principal.

## Otros Patrones

### MVC (Modelo-Vista-Controlador)
- **Uso**: Separar la lógica de la aplicación (modelo), la interfaz de usuario (vista) y el control de entradas (controlador).
- **Ejemplo**: Aplicaciones web donde la entrada del usuario controla el procesamiento de datos y la presentación.
- **Microservicios**: Ayuda a organizar servicios que manejan la interacción del usuario, la lógica de negocio y el acceso a datos por separado.

### Microservicios
- **Uso**: Descomponer una aplicación en servicios independientes y acoplados de manera flexible que se comunican en red.
- **Ejemplo**: Una aplicación grande con servicios individuales para autenticación de usuarios, pagos y notificaciones.
- **Microservicios**: Se aplica directamente a la arquitectura de microservicios.

### Message Broker
- **Uso**: Desacoplar servicios enviando mensajes entre ellos a través de un intermediario.
- **Ejemplo**: Una cola de mensajes que gestiona solicitudes entre servicios en un sistema de comercio electrónico.
- **Microservicios**: Ideal para comunicación asíncrona entre servicios.

### Gateway
- **Uso**: Proporcionar un único punto de entrada a múltiples servicios.
- **Ejemplo**: Un API gateway que enruta las solicitudes a los microservicios correspondientes.
- **Microservicios**: Un patrón arquitectónico común en microservicios para gestionar el acceso y la seguridad de los servicios.



# Patrones de Diseño: Guía Simplificada

Esta guía cubre los patrones de diseño más comunes, categorizados en creacionales, estructurales y de comportamiento.

## Patrones Creacionales
- **Factory Method**
- **Abstract Factory**
- **Builder**
- **Prototype**
- **Singleton**

## Patrones Estructurales
- **Adapter**
- **Bridge**
- **Composite**
- **Decorator**
- **Facade**
- **Flyweight**
- **Proxy**

## Patrones de Comportamiento
- **Chain of Responsibility**
- **Command**
- **Iterator**
- **Mediator**
- **Memento**
- **Observer**
- **State**
- **Strategy**
- **Template Method**
- **Visitor**
