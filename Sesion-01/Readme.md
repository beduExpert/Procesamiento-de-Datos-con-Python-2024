[`Procesamiento de datos con Python`](../README.md) > `Sesión 01`

<div align="center">
    <img src="Imagenes/S01_Bedu.png" alt="Sesion_01">
</div>

## 🎯 Objetivo

Identificar y comprender los conceptos básicos de Python, incluyendo variables, tipos de datos y operadores, para aplicarlos en la creación de programas sencillos.

## 📂 Organización de la sesión

### 📖 Variables en Python
Una variable se utiliza para almacenar información que puede ser referenciada y manipulada en un programa. Las variables son fundamentales en cualquier lenguaje de programación y permiten a los programadores guardar datos, como números, cadenas de texto o estructuras de datos más complejas, para su uso en operaciones computacionales.

### 📜 [Ejemplo 01: Variables.](Ejemplo-01/Readme.md)

---

### 📖 Tipos de Datos en Python

Los tipos de datos en Python son fundamentales porque determinan qué tipo de valor puede contener una variable y qué operaciones se pueden realizar con ella. 

-  **Números**: Python soporta tanto enteros (`int`) como números de punto flotante (`float`). Los enteros son números sin parte decimal, mientras que los flotantes representan números reales y pueden contener decimales.

- **Cadenas de Texto (`str`)**: Las cadenas son secuencias de caracteres utilizadas para almacenar texto. Se definen encerrando los caracteres entre comillas simples o dobles.

- **Listas (`list`)**: Las listas son colecciones ordenadas y mutables que pueden contener elementos de diferentes tipos, incluyendo otras listas. Se definen usando corchetes y separando los elementos con comas (`[,,,]`).

- **Tuplas (`tuple`)**: Similar a las listas, pero inmutables. Una vez definida, no puedes modificar sus elementos. Se definen usando paréntesis (`(,,,)`).

- **Diccionarios (`dict`)**: Son colecciones no ordenadas de pares clave-valor. Permiten una rápida búsqueda, inserción y eliminación de datos basados en la clave. Se definen usando llaves, con los pares clave-valor separados por comas (`{key:value}`).

- **Booleanos (`bool`)**: Representan dos valores: `True` o `False`. Son muy utilizados para controlar el flujo de programas a través de declaraciones condicionales.

### 📜 [Ejemplo 02: Tipos de Datos.](Ejemplo-02/Readme.md)

### 💡 [Reto 01: Promedio de Edades.](Reto-01/Readme.md)

---

### 📖 Operadores Relacionales

Los operadores relacionales son utilizados para comparar dos valores y determinar si una relación es verdadera o falsa. En Python, los operadores relacionales más comunes son:

- **Igual (`==`)**: Evalúa si dos valores son iguales. Por ejemplo, `5 == 5` devuelve `True`.

- **No igual (`!=`)**: Verifica si dos valores son diferentes. Por ejemplo, `5 != 4` devuelve `True`.

- **Mayor que (`>`)**: Comprueba si el valor de la izquierda es mayor que el de la derecha. Por ejemplo, `10 > 5` devuelve `True`.

- **Menor que (`<`)**: Comprueba si el valor de la izquierda es menor que el de la derecha. Por ejemplo, `5 < 10` devuelve `True`.

- **Mayor o igual que (`>=`)**: Evalúa si el valor de la izquierda es mayor o igual al de la derecha. Por ejemplo, `10 >= 10` devuelve `True`.

- **Menor o igual que (`<=`)**: Evalúa si el valor de la izquierda es menor o igual al de la derecha. Por ejemplo, `5 <= 5` devuelve `True`.

### 📜 [Ejemplo 03: Operadores Relacionales.](Ejemplo-03/Readme.md)

---

### 📖 Operadores Logicos.

Los operadores lógicos en Python permiten combinar expresiones condicionales y son esenciales para controlar el flujo de un programa mediante decisiones más complejas. Los principales operadores lógicos son:

- **AND (`and`)**: Evalúa como `True` si todas las condiciones que conecta son verdaderas. Por ejemplo, `True and False` devuelve `False` porque no todas las condiciones son verdaderas.

- **OR (`or`)**: Devuelve `True` si al menos una de las condiciones que conecta es verdadera. Por ejemplo, `True or False` devuelve `True` porque al menos una condición es verdadera.

- **NOT (`not`)**: Invierte el resultado de la condición que precede. Si la condición es `True`, `not` la convierte en `False`, y viceversa. Por ejemplo, `not False` devuelve `True`.



### 📜 [Ejemplo 04: Operadores Lógicos.](Ejemplo-04/Readme.md)

### 💡 [Reto 02: Simulador de Compra de Articulos.](Reto-02/Readme.md)
---


### 📖 Operadores de asignación.

Los operadores de asignación en Python son utilizados para asignar valores a variables de una forma más corta y directa. Estos operadores combinan operaciones aritméticas o lógicas con la asignación, lo que simplifica la sintaxis del código.

- **Asignación (`=`)**: Asigna un valor a una variable. Ejemplo: `x = 5`.

- **Asignación con suma (`+=`)**: Suma el valor del lado derecho al valor de la variable y asigna el resultado a la misma variable. Ejemplo: `x += 3` es equivalente a `x = x + 3`.

- **Asignación con resta (`-=`)**: Resta el valor del lado derecho del valor de la variable y asigna el resultado a la misma variable. Ejemplo: `x -= 2` es equivalente a `x = x - 2`.

- **Asignación con multiplicación (`*=`)**: Multiplica el valor de la variable por el valor del lado derecho y asigna el resultado a la misma variable. Ejemplo: `x *= 4` es equivalente a `x = x * 4`.

- **Asignación con división (`/=`)**: Divide el valor de la variable por el valor del lado derecho y asigna el resultado a la misma variable. Ejemplo: `x /= 2` es equivalente a `x = x / 2`.

- **Asignación con módulo (`%=`)**: Calcula el módulo utilizando el valor de la variable y el valor del lado derecho y asigna el resultado a la misma variable. Ejemplo: `x %= 3` es equivalente a `x = x % 3`.

### 📜 [Ejemplo 05: Operadores de asignación.](Ejemplo-05/Readme.md)


---

### 📖 Interpolación de Strings y lectura por teclado.

La interpolación de strings y la lectura por teclado son herramientas esenciales en Python que mejoran la interactividad y flexibilidad de los programas. Permiten crear aplicaciones que se adaptan dinámicamente a las necesidades y entradas de los usuarios, desde simples scripts hasta interfaces de usuario complejas.


- **Formato con `%`**:
   Antes de la introducción de los f-strings, la interpolación se realizaba con el operador `%`, similar a sprintf en otros lenguajes de programación.
   ```python
   nombre = "Mundo"
   print("Hola, %s" % nombre)
   ```

- **Método `format()`**:
   Una forma más versátil y moderna es usar el método `format()`, que permite reordenar y reutilizar la información fácilmente.
   ```python
   nombre = "Mundo"
   print("Hola, {0}".format(nombre))
   ```

- **F-strings (Literal String Interpolation)**:
   Introducido en Python 3.6, los f-strings ofrecen una manera más legible y concisa de realizar la interpolación.
   ```python
   nombre = "Mundo"
   print(f"Hola, {nombre}")
   ```

**Lectura por Teclado:**

La función `input()` se utiliza para capturar la entrada del teclado en Python, permitiendo a los usuarios introducir datos directamente en un programa:

```python
nombre = input("Introduce tu nombre: ")
print(f"¡Hola, {nombre}!")
```

Esta función siempre devuelve una cadena de texto, incluso si el usuario introduce números. Para trabajar con tipos de datos específicos, debes convertir esta entrada a su tipo correspondiente, por ejemplo, usando `int()` para convertir a entero.



### 📜 [Ejemplo 06: Interpolación de Strings y lectura por teclado.](Ejemplo-06/Readme.md)


### 💡 [Reto 03: Cotizador para la compra de auto.](Reto-03/Readme.md)
---
[`Anterior`](../README.md) | [`Siguiente`](../Sesion-02/Readme.md)
