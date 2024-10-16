[← Inicio](./README.md)

------

# Clean Code: Mejores Prácticas y Reglas Fundamentales

Este documento cubre las reglas clave para escribir **Clean Code**, un enfoque que promueve la claridad, legibilidad y mantenibilidad del código.

## Índice
1. [Definición de Clean Code](#definición-de-clean-code)
2. [Reglas de Clean Code](#reglas-de-clean-code)
   - [Nombres Claros y Significativos](#nombres-claros-y-significativos)
   - [Funciones Simples y Cortas](#funciones-simples-y-cortas)
   - [Evitar Comentarios Innecesarios](#evitar-comentarios-innecesarios)
   - [Control de Flujo Reducido](#control-de-flujo-reducido)
   - [Evitar el Código Repetido](#evitar-el-código-repetido)
   - [Utilizar Excepciones y No Retornos de Error](#utilizar-excepciones-y-no-retornos-de-error)
   - [Organización Estructurada del Código](#organización-estructurada-del-código)
   - [Mantener los Test Unitarios](#mantener-los-test-unitarios)
3. [Conclusión](#conclusión)

---

## 1. Definición de Clean Code

### Explicación:
**Clean Code** se refiere a la práctica de escribir código que sea fácil de leer, entender y mantener. Se enfoca en la claridad, simplicidad y en minimizar la cantidad de errores posibles a lo largo del tiempo.

---

## 2. Reglas de Clean Code

### Nombres Claros y Significativos

- **Explicación**: Los nombres de variables, funciones y clases deben ser descriptivos y reflejar su propósito. Evita usar abreviaturas o nombres genéricos como `temp` o `data`. Los nombres deben hacer obvia la intención del código.
  
### Funciones Simples y Cortas

- **Explicación**: Las funciones deben realizar una sola tarea y hacerlo bien. Mantén las funciones cortas para que sean fáciles de entender y probar. Idealmente, no deberían tener más de 20 líneas de código, y deben ser fáciles de seguir.

### Evitar Comentarios Innecesarios

- **Explicación**: En lugar de escribir comentarios para explicar el código, escribe código que se explique por sí mismo. Los comentarios pueden volverse obsoletos o no reflejar correctamente el comportamiento del código. Úsalos solo cuando sea absolutamente necesario, como para explicar decisiones de diseño complejas.

### Control de Flujo Reducido

- **Explicación**: Evita estructuras de control complicadas como múltiples bucles anidados o muchas condiciones. Utiliza `if`, `else`, y `switch` de manera clara y evita los "efectos secundarios" (por ejemplo, cambiar el estado del programa dentro de condiciones o bucles).

### Evitar el Código Repetido

- **Explicación**: No dupliques código. Si encuentras que necesitas escribir el mismo bloque de código más de una vez, refactorízalo en una función o método separado. Esto mejora la mantenibilidad y facilita realizar cambios en el futuro.

### Utilizar Excepciones y No Retornos de Error

- **Explicación**: En lugar de devolver códigos de error y forzar al usuario a manejarlos, lanza excepciones. Las excepciones permiten un manejo de errores más limpio y hacen que el código sea más fácil de seguir.

### Organización Estructurada del Código

- **Explicación**: Estructura tu código de manera lógica. Agrupa funciones y clases que estén relacionadas, y sigue convenciones de organización dentro de tu equipo o comunidad de desarrollo. El código debe estar organizado de forma que otros desarrolladores puedan entender fácilmente el flujo general del programa.

### Mantener los Test Unitarios

- **Explicación**: El código limpio debe ser probado. Mantén una buena cobertura de pruebas unitarias para asegurar que el código funcione como se espera. Asegúrate de que los tests sean claros y fáciles de entender, y actualízalos cuando se realicen cambios en el código.

---

## 3. Conclusión

**Clean Code** se trata de escribir código que sea fácil de leer y mantener. Siguiendo estas reglas, puedes mejorar la calidad de tu código y hacer que sea más fácil de entender, modificar y extender para otros desarrolladores o para ti mismo en el futuro.
