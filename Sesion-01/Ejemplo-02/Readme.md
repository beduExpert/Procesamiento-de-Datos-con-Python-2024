[`Procesamiento de datos con Python`](../../Readme.md) > [`Sesión 01`](../Readme.md) > `Ejemplo 02: Tipos de datos`


## 🎯 Objetivo

Aplicar los principales tipos de datos y su funcionamiento, así como las ventajas de cada uno.

## 📂 Organización de la sesión


### Tipos de datos en Python

En Python, los tipos de datos son una categoría que define los valores que una variable puede tomar. Los tipos de datos más comunes en Python son:

### 1. Números
Python tiene varios tipos de datos numéricos:

- **Enteros (`int`)**: Representan números enteros sin parte decimal. Ejemplo: `5`, `-3`, `42`.
- **Números de punto flotante (`float`)**: Representan números reales e incluyen una parte decimal. Ejemplo: `3.14`, `-0.001`, `2.0`.
- **Números complejos (`complex`)**: Usados para representar números complejos, tienen una parte real y una parte imaginaria. Ejemplo: `3 + 4j`.

### 2. Cadenas de caracteres (Strings)
Las cadenas (`str`) son secuencias de caracteres usadas para almacenar datos textuales. Ejemplo: `"Hola"`, `'Python es divertido'`.

```python
nombre = "Ana"
saludo = "Hola, " + nombre  # Concatenación de strings
print(saludo)  # Salida: Hola, Ana
```

### 3. Booleanos
El tipo booleano (`bool`) puede tener solo dos valores: `True` (verdadero) y `False` (falso). Son muy útiles en condiciones y bucles.

```python
a = 5
b = 10
es_mayor = a > b
print(es_mayor)  # Salida: False
```

### 4. Listas
Las listas (`list`) son estructuras de datos que pueden almacenar una colección de diferentes tipos de datos. Son mutables, lo que significa que podemos cambiar, añadir o eliminar elementos después de su creación.

```python
lista = [1, 2.5, 'Python', True]
print(lista)  # Salida: [1, 2.5, 'Python', True]
```

### 5. Tuplas
Las tuplas (`tuple`) son similares a las listas, pero son inmutables. Una vez creadas, no se pueden cambiar.

```python
tupla = (1, 2.5, 'Python', True)
print(tupla) # Salida: (1, 2.5, 'Python', True)
```

### 6. Conjuntos
Los conjuntos (`set`) son colecciones no ordenadas y sin elementos duplicados. Son útiles para realizar operaciones matemáticas como uniones, intersecciones y diferencias.

```python
conjunto = {1, 2, 3, 4, 4, 5}
print(conjunto)  # Salida: {1, 2, 3, 4, 5}
```

### 7. Diccionarios
Los diccionarios (`dict`) almacenan pares de clave-valor y son una de las estructuras de datos más útiles y frecuentemente usadas en Python.

```python
diccionario = {'nombre': 'Carlos', 'edad': 28}
print(diccionario)  # Salida: {'nombre': 'Carlos', 'edad': 28}
```

---

### Más ejemplos en el notebook

Hemos preparado un notebook para Google Colab que contiene una serie de ejercicios y demostraciones detalladas. 
Este recurso es ideal para profundizar y aplicar los conceptos vistos de manera interactiva.


### 🛠️ [Abrir Notebook](Ejemplo_02_Tipos_Datos.ipynb)


[`Anterior`](../Readme.md) | [`Siguiente`](../Ejemplo-03/Readme.md)