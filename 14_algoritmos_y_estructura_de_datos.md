[← Inicio](./README.md)

------
# Algoritmos y Estructuras de Datos: Explicación y Ejemplos



## Índice
1. [Definición de Algoritmos](#definición-de-algoritmos)
2. [Definición de Estructuras de Datos](#definición-de-estructuras-de-datos)
3. [Tipos de Algoritmos](#tipos-de-algoritmos)
   - [Búsqueda Lineal](#búsqueda-lineal)
   - [Búsqueda Binaria](#búsqueda-binaria)
   - [QuickSort](#quicksort)
   - [MergeSort](#mergesort)
   - [Bubble Sort](#bubble-sort)
   - [Insertion Sort](#insertion-sort)
   - [Dijkstra's Algorithm](#dijkstras-algorithm)
4. [Tipos de Estructuras de Datos](#tipos-de-estructuras-de-datos)
   - [Listas](#listas)
   - [Pilas](#pilas)
   - [Colas](#colas)
   - [Conjuntos](#conjuntos)
   - [Diccionarios (Mapas)](#diccionarios-map)
   - [Árboles](#árboles)
   - [Grafos](#grafos)

---

## 1. Definición de Algoritmos

Los **algoritmos** son secuencias de instrucciones para resolver problemas o realizar tareas. Su eficiencia se mide en términos de tiempo y espacio.

## 2. Definición de Estructuras de Datos

Las **estructuras de datos** organizan y almacenan datos para optimizar el acceso y la modificación. Son esenciales para implementar algoritmos de manera efectiva.

---

## 3. Tipos de Algoritmos

### Búsqueda Lineal
- **Descripción**: Recorre cada elemento en una lista hasta encontrar el objetivo.
- **Usos**: Ideal para listas pequeñas o no ordenadas.
- **Complejidad**: O(n), donde n es el número de elementos.

### Búsqueda Binaria
- **Descripción**: Divide repetidamente una lista ordenada en mitades para encontrar un objetivo.
- **Usos**: Eficiente en listas grandes y ordenadas.
- **Complejidad**: O(log n).

### QuickSort
- **Descripción**: Algoritmo de ordenamiento que selecciona un "pivote" y particiona la lista en elementos menores y mayores.
- **Usos**: Muy utilizado en aplicaciones de ordenamiento general.
- **Complejidad**: O(n log n) en promedio.

### MergeSort
- **Descripción**: Divide la lista en mitades, ordena cada mitad y luego las combina.
- **Usos**: Utilizado en aplicaciones que requieren estabilidad en el ordenamiento.
- **Complejidad**: O(n log n).

### Bubble Sort
- **Descripción**: Compara elementos adyacentes y los intercambia si están en el orden incorrecto, repitiendo el proceso.
- **Usos**: Más educativo que práctico, utilizado en listas pequeñas.
- **Complejidad**: O(n²).

### Insertion Sort
- **Descripción**: Construye una lista ordenada insertando elementos uno a uno en la posición correcta.
- **Usos**: Eficiente para listas pequeñas o casi ordenadas.
- **Complejidad**: O(n²) en el peor de los casos.

### Dijkstra's Algorithm
- **Descripción**: Algoritmo para encontrar el camino más corto en un grafo con pesos no negativos.
- **Usos**: Utilizado en sistemas de navegación y redes.
- **Complejidad**: O(V²) o O(E log V), donde V es el número de vértices y E el de aristas.

---

## 4. Tipos de Estructuras de Datos

### Listas
- **Descripción**: Colección ordenada de elementos donde cada elemento tiene un índice.
- **Usos**: Almacenar colecciones de datos dinámicas.
- **Ejemplo**: Lista de estudiantes.

### Pilas
- **Descripción**: Estructura de datos que sigue el principio LIFO (Last In, First Out).
- **Usos**: Implementar funciones de retroceso, como en navegadores.
- **Ejemplo**: Historial de navegación.

### Colas
- **Descripción**: Estructura que sigue el principio FIFO (First In, First Out).
- **Usos**: Manejar tareas en orden, como impresoras.
- **Ejemplo**: Cola de atención en un banco.

### Conjuntos
- **Descripción**: Colección no ordenada de elementos únicos.
- **Usos**: Eliminar duplicados y realizar operaciones matemáticas como uniones e intersecciones.
- **Ejemplo**: Lista de etiquetas en un artículo.

### Diccionarios (Mapas)
- **Descripción**: Estructura de datos que almacena pares clave-valor.
- **Usos**: Permiten accesos rápidos y búsquedas.
- **Ejemplo**: Almacenamiento de información de usuarios donde el nombre de usuario es la clave.

### Árboles
- **Descripción**: Estructura jerárquica compuesta por nodos conectados.
- **Usos**: Almacenamiento eficiente de datos jerárquicos y búsqueda.
- **Ejemplo**: Árbol de decisiones o árbol de archivos.

### Grafos
- **Descripción**: Colección de nodos (vértices) conectados por aristas (edges).
- **Usos**: Modelar relaciones entre objetos, como redes sociales o rutas de transporte.
- **Ejemplo**: Mapa de ciudades y carreteras.

---

Este documento proporciona una visión general de los algoritmos y estructuras de datos, centrándose en tipos clave y sus aplicaciones. Comprender estos conceptos es fundamental para el desarrollo de software eficiente.
