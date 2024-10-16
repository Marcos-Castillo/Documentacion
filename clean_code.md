[← Inicio](./README.md)

------

# Clean Code: Mejores Prácticas

Escribir código limpio mejora la mantenibilidad y comprensión del mismo, lo que facilita el trabajo en equipo y la evolución de los proyectos a lo largo del tiempo.

## Nombres de Variables Comprensibles

Usa nombres que reflejen la intención del código.

**Definición:**  
Los nombres de las variables deben ser descriptivos y comunicar claramente su propósito. Un buen nombre ayuda a los desarrolladores a entender rápidamente el código sin necesidad de comentarios adicionales.

**Usos:**  
- Facilita la legibilidad del código.
- Hace que el código sea autodescriptivo y fácil de seguir.

**Ejemplos:**  
- **Mal nombre:** `x`, `temp`, `data1`  
- **Buen nombre:** `customerAge`, `orderTotal`, `userEmail`  
  Un nombre como `customerAge` indica claramente que la variable almacena la edad del cliente.

---

## Refactorización y Simplicidad

Refactoriza regularmente y busca la simplicidad en la solución.

**Definición:**  
La refactorización es el proceso de modificar el código existente para mejorar su estructura y claridad sin cambiar su comportamiento externo. La simplicidad implica diseñar soluciones que sean lo más directas posible, evitando complicaciones innecesarias.

**Usos:**  
- Mejora la legibilidad y mantenibilidad del código.
- Elimina la complejidad innecesaria y hace que el código sea más fácil de entender.

**Ejemplos:**  
- **Antes de la refactorización:**  
  Definición de una función para calcular un descuento que incluye una lógica condicional compleja.

- **Después de la refactorización:**  
  Simplificación de la lógica para calcular el descuento en una sola línea, mejorando la legibilidad.

---

## Evitar Duplicación (DRY)

No repitas el mismo código en diferentes lugares.

**Definición:**  
El principio DRY (Don't Repeat Yourself) sugiere que la duplicación de código debe evitarse, ya que cada pieza de conocimiento debe tener una única representación en el código.

**Usos:**  
- Facilita la mantenibilidad del código, ya que los cambios solo necesitan hacerse en un lugar.
- Reduce la posibilidad de errores y comportamientos inconsistentes.

**Ejemplos:**  
- **Código duplicado:**  
  Múltiples funciones que calculan áreas de diferentes formas geométricas.

- **Código refactorizado (evitando duplicación):**  
  Una única función que calcula el área según el tipo de forma y sus dimensiones.

---

Implementar estas prácticas de Clean Code no solo mejora la calidad del código, sino que también facilita la colaboración entre los desarrolladores, reduce la posibilidad de errores y acelera el desarrollo de nuevas funcionalidades. Al seguir estos principios, podrás crear aplicaciones más sostenibles y fáciles de mantener.
