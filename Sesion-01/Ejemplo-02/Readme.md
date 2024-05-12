[`Procesamiento de datos con Python`](../../Readme.md) > [`Sesión 01`](../Readme.md) > `Ejemplo 02: Tipos de datos`


## 🎯 Objetivo

Aplicar los principales tipos de datos y su funcionamiento, así como las ventajas de cada uno.

## 📂 Comencemos 🚀


### Tipos de datos en Python

Los tipos de datos en Python son una categoría que define los valores que una variable puede tomar. Los tipos de datos más comunes en Python son:

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

Estos son los tipos de datos más comunes en Python, pero hay otros tipos de datos más avanzados que veremos más adelante.

---

#### 🔥Dato interesante: la funcion `type()` nos permite saber el tipo de dato de una variable.

```python
numero = 10  # Python infiere que 'numero' es de tipo int
print(type(numero))  # Salida: <class 'int'>
```

---

### Más ejemplos en el notebook

Hemos preparado un notebook para Google Colab que contiene una serie de ejercicios y demostraciones detalladas. 
Este recurso es ideal para profundizar y aplicar los conceptos vistos de manera interactiva.


### 🛠️ [Abrir Notebook](Ejemplo_02_Tipos_Datos.ipynb)


[`Anterior`](../Readme.md) | [`Siguiente`](../Ejemplo-03/Readme.md)