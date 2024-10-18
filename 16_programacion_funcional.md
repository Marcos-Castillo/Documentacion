[← Inicio](./README.md)

------

# Programación Funcional

La **programación funcional** es un paradigma de programación que trata de construir software mediante la evaluación de funciones matemáticas, evitando el uso de estados mutables y efectos secundarios. En lugar de comandos, se utiliza la composición de funciones.

## Índice
1. [Definición de Programación Funcional](#definición-de-programación-funcional)
2. [Características Clave](#características-clave)
3. [Ventajas de la Programación Funcional](#ventajas-de-la-programación-funcional)
4. [Desventajas de la Programación Funcional](#desventajas-de-la-programación-funcional)
5. [Funciones Puras](#funciones-puras)
6. [Inmutabilidad](#inmutabilidad)
7. [Composición de Funciones](#composición-de-funciones)
8. [Recursión](#recursión)

---

## 1. Definición de Programación Funcional

La **programación funcional** es un paradigma donde las computaciones se estructuran como la evaluación de funciones matemáticas. Las funciones son tratadas como ciudadanos de primera clase, lo que significa que pueden ser pasadas como argumentos, retornadas como valores y asignadas a variables.

---

## 2. Características Clave

### **Funciones Puras**:
Las funciones puras no tienen efectos secundarios y siempre producen el mismo resultado para los mismos argumentos.

### **Inmutabilidad**:
Los datos no pueden cambiar una vez creados. Los objetos son inmutables, lo que significa que una vez que se ha asignado un valor, no se puede modificar.

### **Expresiones**:
En programación funcional, todo es una expresión, lo que implica que todo devuelve un valor, incluidas las construcciones de control.

### **Composición de Funciones**:
Las funciones se pueden combinar para crear nuevas funciones a partir de las ya existentes, facilitando la reutilización de código.

### **Recursión**:
La recursión se utiliza como alternativa a los bucles para repetir operaciones.

---

## 3. Ventajas de la Programación Funcional

- **Legibilidad y Mantenibilidad**: El uso de funciones puras y la inmutabilidad hacen que el código sea más predecible, claro y fácil de razonar.
- **Menor Riesgo de Errores**: Al no tener efectos secundarios ni estados mutables, se reducen los errores inesperados.
- **Facilita el Paralelismo**: Es más fácil escribir código concurrente o paralelo gracias a la inmutabilidad.
- **Modularidad**: La composición de funciones permite construir sistemas modulares y reutilizables.

---

## 4. Desventajas de la Programación Funcional

- **Curva de Aprendizaje**: Para los desarrolladores acostumbrados a la programación orientada a objetos, puede ser difícil adaptarse a los conceptos de programación funcional.
- **Rendimiento**: La inmutabilidad puede consumir más memoria, ya que se crean nuevas versiones de los datos en lugar de modificarlos directamente.
- **Gestión del Estado Global**: Manejar el estado compartido y mutable puede ser menos intuitivo en un entorno funcional.

---

## 5. Funciones Puras

Las **funciones puras** son funciones que siempre devuelven el mismo resultado para los mismos argumentos y no producen efectos secundarios, como modificar el estado global o realizar operaciones de entrada/salida.

---

## 6. Inmutabilidad

En la programación funcional, los datos no pueden cambiarse una vez creados. En lugar de modificar los datos existentes, se crean nuevas versiones con los cambios aplicados, lo que evita efectos secundarios no deseados.

---

## 7. Composición de Funciones

La **composición de funciones** es el proceso de combinar dos o más funciones para crear una nueva función. Esta característica permite la reutilización de código y mejora la legibilidad y mantenibilidad.

---

## 8. Recursión

La **recursión** es una técnica común en programación funcional, utilizada para repetir operaciones sin utilizar bucles. En lugar de iterar sobre una estructura, las funciones se llaman a sí mismas hasta cumplir una condición base.

---

La programación funcional se centra en el uso de funciones puras, la inmutabilidad y la composición de funciones, lo que contribuye a escribir software más claro, predecible y fácil de mantener.
