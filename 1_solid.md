[← Inicio](./README.md)

------

# Principios SOLID

Los principios SOLID son un conjunto de cinco principios de diseño que ayudan a los desarrolladores a crear software más mantenible y flexible.

## 1. **Single Responsibility Principle (SRP)**
- **Descripción**: Cada clase debe tener una única responsabilidad.
- **Explicación**: Cada clase debe tener una única responsabilidad.
Esto significa que una clase debe hacer solo una cosa. Si una clase tiene más de una razón para cambiar, está violando este principio. Tener clases con responsabilidades múltiples hace que el código sea más difícil de mantener, ya que un cambio en una funcionalidad podría afectar otra funcionalidad no relacionada.

- Ejemplo en la vida real: Imagina que tienes un empleado en una tienda. Este empleado no debería hacer las ventas, el inventario, y las finanzas al mismo tiempo. Es mejor asignar cada tarea a una persona diferente (en el código, una clase diferente).

---

## 2. **Open/Closed Principle (OCP)**
- **Descripción**: Las clases deben estar abiertas a la extensión, pero cerradas a la modificación.
- **Explicación**: El software debe estar abierto a la extensión, pero cerrado a la modificación.
Este principio implica que una clase debe permitir que se le agreguen nuevas funcionalidades sin necesidad de modificar su código fuente. Esto se logra utilizando la herencia o interfaces. Si sigues este principio, puedes mejorar o extender el comportamiento del sistema sin arriesgarte a romper el código ya existente.

- Ejemplo en la vida real: Piensa en una aplicación que procesa pagos. Si quieres agregar un nuevo método de pago, no deberías tener que cambiar todo el código relacionado con los pagos ya existentes (como tarjetas de crédito). En su lugar, simplemente deberías extender el sistema y agregar el nuevo método (por ejemplo, PayPal) sin modificar el código ya implementado.

---

## 3. **Liskov Substitution Principle (LSP)**
- **Descripción**: Los objetos de una clase derivada deben poder reemplazar a los objetos de la clase base sin alterar el funcionamiento del programa.
- **Explicación**: Los objetos de una clase derivada deben poder reemplazar a los de una clase base sin alterar el comportamiento del programa.
Este principio establece que las subclases deben ser capaces de sustituir a sus superclases sin que el programa falle o se comporte de manera inesperada. Básicamente, las subclases deben cumplir con los contratos que la superclase establece, respetando sus comportamientos y reglas.

- Ejemplo en la vida real: Piensa en una aplicación que gestiona animales. Si tienes una clase base "Animal" con un método "HacerSonido()", las subclases "Perro" y "Gato" deben poder sustituir a "Animal" sin romper el comportamiento del programa. Es decir, "Perro" debe hacer el sonido de un perro, y "Gato" el de un gato, pero ambos siguen siendo tratados como "Animal".
---

## 4. **Interface Segregation Principle (ISP)**
- **Descripción**: Los clientes no deben verse obligados a depender de interfaces que no utilizan.
- **Explicación**: Los clientes no deben verse obligados a depender de interfaces que no utilizan.
Este principio promueve que las interfaces deben ser específicas para lo que los clientes realmente necesitan, en lugar de tener una interfaz general con muchos métodos que podrían no ser necesarios. Es mejor tener varias interfaces pequeñas y específicas, que obligar a los usuarios a implementar métodos que no utilizan.

- Ejemplo en la vida real: Imagina que tienes un teléfono móvil con diferentes aplicaciones. Cada aplicación debería usar solo las funcionalidades que necesita (por ejemplo, la cámara, GPS, etc.). Si una aplicación solo necesita acceder a la cámara, no debería verse obligada a manejar también la función de GPS, ya que eso complicaría su uso innecesariamente.

---

## 5. **Dependency Inversion Principle (DIP)**
- **Descripción**: Las dependencias deben ser abstraídas, lo que implica que las clases de alto nivel no deben depender de clases de bajo nivel.
- **Explicación**: Los módulos de alto nivel no deben depender de los de bajo nivel, ambos deben depender de abstracciones.
Esto significa que las clases más generales y de alto nivel no deben depender directamente de clases concretas o detalles de implementación. En su lugar, deben depender de interfaces o clases abstractas, que definan contratos generales. Esto permite que los detalles de implementación puedan cambiar sin afectar a la clase principal.

- Ejemplo en la vida real: Piensa en una lámpara y un interruptor. El interruptor no debería depender de una lámpara específica (por ejemplo, una lámpara de mesa), sino de un tipo genérico de lámpara (una interfaz). De esta forma, el interruptor funcionará para cualquier tipo de lámpara que conectes, como una lámpara de pie o una bombilla inteligente.


## Conclusión:
Los principios SOLID te ayudan a crear sistemas que son fáciles de mantener, mejorar y escalar con el tiempo. Aplicar estos principios reduce el riesgo de errores, facilita la adición de nuevas características y mejora la calidad del software en general.

* SRP: Mantén responsabilidades claras y separadas.
* OCP: Extiende, no modifiques.
* LSP: Las subclases deben comportarse como la clase base.
* ISP: Interfaces específicas para evitar implementar lo innecesario.
* DIP: Dependencias hacia abstracciones, no hacia implementaciones concretas.