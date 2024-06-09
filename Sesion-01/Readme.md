🏠 [**Inicio**](../Readme.md) ➡️ / 📖 `Sesión 01`

<div align="center">
    <img src="Imagenes/S01_Bedu.png" alt="Sesion_01">
</div>

## 🎯 Objetivo

⚒️ Identificar y comprender los conceptos básicos de Python, incluyendo variables, tipos de datos y operadores, para aplicarlos en la creación de programas sencillos.

---

📘 Material del prework:
Antes de comenzar con los ejercicios de esta sesión, recordemos que en el material de prework hemos cubierto los fundamentos teóricos que aplicaremos hoy. A lo largo de esta sesión, pondremos en práctica estos conceptos mediante una serie de ejercicios y retos diseñados para reforzar y validar nuestro entendimiento. 
🔥¡Vamos a comenzar!🔥

---

## 📂 Temas de la sesión...

### 📖 Variables en Python
Recordemos que una variable se utiliza para almacenar información que puede ser referenciada y manipulada en un programa. Las variables son fundamentales en cualquier lenguaje de programación y permiten a los programadores guardar datos, como números, cadenas de texto o estructuras de datos más complejas, para su uso en operaciones computacionales, una de las mejores prácticas para nombrar variables es usando `snake_case` como convención.

---

### 📖 Tipos de datos en Python

Los tipos de datos son fundamentales porque determinan qué tipo de valor puede contener una variable y qué operaciones se pueden realizar con ella. 

- **Números (`int`, `float`)**: Enteros para valores sin decimales y flotantes para números reales.
- **Cadenas de Texto (`str`)**: Secuencias de caracteres para almacenar texto.
- **Listas (`list`)**: Colecciones mutables de elementos de diversos tipos.
- **Tuplas (`tuple`)**: Colecciones inmutables similares a las listas.
- **Diccionarios (`dict`)**: Conjuntos de pares clave-valor para almacenamiento y búsqueda eficiente.
- **Booleanos (`bool`)**: Valores de verdad (`True`, `False`) para controlar el flujo del programa.

#### 📜 **[Ejemplo 01: Variables y Tipos de Datos](Ejemplo-01/Readme.md)**
#### 🔥 **[Reto 01: Recomendación de cursos](Reto-01/Readme.md)**
---

### 📖 Operadores aritméticos

Los operadores aritméticos se utilizan para cálculos básicos, permitiendo manipular valores numéricos y realizar operaciones matemáticas comunes directamente en el código.

- **Suma (`+`)**: Suma dos números.
- **Resta (`-`)**: Resta el segundo número del primero.
- **Multiplicación (`*`)**: Multiplica dos números.
- **División (`/`)**: Divide el primer número por el segundo, resultando en un número flotante.
- **Módulo (`%`)**: Devuelve el resto de la división entre dos números.
- **Exponenciación (`**`)**: Eleva un número a la potencia del segundo número.
- **División Entera (`//`)**: Divide el primer número por el segundo y devuelve la parte entera del resultado, descartando cualquier resto.

---

### 📖 Operadores relacionales

Los operadores relacionales son utilizados para comparar dos valores y determinar si una relación es `verdadera` o`falsa`. En Python, los operadores relacionales más comunes son:

- **Igual (`==`)**: Evalúa si dos valores son iguales. Por ejemplo, `5 == 5` devuelve `True`.
- **No igual (`!=`)**: Verifica si dos valores son diferentes. Por ejemplo, `5 != 4` devuelve `True`.
- **Mayor que (`>`)**: Comprueba si el valor de la izquierda es mayor que el de la derecha. Por ejemplo, `10 > 5` devuelve `True`.
- **Menor que (`<`)**: Comprueba si el valor de la izquierda es menor que el de la derecha. Por ejemplo, `5 < 10` devuelve `True`.
- **Mayor o igual que (`>=`)**: Evalúa si el valor de la izquierda es mayor o igual al de la derecha. Por ejemplo, `10 >= 10` devuelve `True`.
- **Menor o igual que (`<=`)**: Evalúa si el valor de la izquierda es menor o igual al de la derecha. Por ejemplo, `5 <= 5` devuelve `True`.

---

### 📖 Operadores lógicos

Los operadores lógicos permiten combinar expresiones condicionales y son esenciales para controlar el flujo de un programa mediante decisiones más complejas. Los principales operadores lógicos son:

- **AND (`and`)**: Evalúa como `True` si todas las condiciones que conecta son verdaderas. Por ejemplo, `True and False` devuelve `False` porque no todas las condiciones son verdaderas.

- **OR (`or`)**: Devuelve `True` si al menos una de las condiciones que conecta es verdadera. Por ejemplo, `True or False` devuelve `True` porque al menos una condición es verdadera.

- **NOT (`not`)**: Invierte el resultado de la condición que precede. Si la condición es `True`, `not` la convierte en `False`, y viceversa. Por ejemplo, `not False` devuelve `True`.

---

### 📖 Operadores de asignación

Los operadores de asignación son utilizados para asignar valores a variables de una forma más corta y directa. Estos operadores combinan operaciones aritméticas o lógicas con la asignación, lo que simplifica la sintaxis del código.

- **Asignación (`=`)**: Asigna un valor a una variable. Ejemplo: `x = 5`.

- **Asignación con suma (`+=`)**: Suma el valor del lado derecho al valor de la variable y asigna el resultado a la misma variable. Ejemplo: `x += 3` es equivalente a `x = x + 3`.

- **Asignación con resta (`-=`)**: Resta el valor del lado derecho del valor de la variable y asigna el resultado a la misma variable. Ejemplo: `x -= 2` es equivalente a `x = x - 2`.

- **Asignación con multiplicación (`*=`)**: Multiplica el valor de la variable por el valor del lado derecho y asigna el resultado a la misma variable. Ejemplo: `x *= 4` es equivalente a `x = x * 4`.

- **Asignación con división (`/=`)**: Divide el valor de la variable por el valor del lado derecho y asigna el resultado a la misma variable. Ejemplo: `x /= 2` es equivalente a `x = x / 2`.

- **Asignación con módulo (`%=`)**: Calcula el módulo utilizando el valor de la variable y el valor del lado derecho y asigna el resultado a la misma variable. Ejemplo: `x %= 3` es equivalente a `x = x % 3`.

#### 📜 **[Ejemplo 02: Operadores en Python](Ejemplo-02/Readme.md)**


#### 🔥 **[Reto 02: Simulador de compra de artículos](Reto-02/Readme.md)**

---

### 📖 Interpolación de Strings y lectura por teclado

La interpolación de strings y la lectura por teclado son herramientas esenciales que mejoran la interactividad y flexibilidad de los programas. Permiten crear aplicaciones que se adaptan dinámicamente a las necesidades y entradas de los usuarios, desde simples scripts hasta interfaces de usuario complejas.


- **Formato con `%`**:
   Antes de la introducción de los f-strings, la interpolación se realizaba con el operador `%`, similar a printf en otros lenguajes de programación.
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
   Introducido en Python 3.6, los f-strings ofrecen una manera más limpia y legible de formatear strings, permitiendo la interacción directa con variables.
   ```python
   nombre = "Mundo"
   print(f"Hola, {nombre}")
   ```

**Lectura por teclado:**

Recordemos que la función `input()` se utiliza para capturar la entrada del teclado en Python, permitiendo a los usuarios introducir datos directamente en un programa:

```python
nombre = input("Introduce tu nombre: ")
print(f"¡Hola, {nombre}!")
```

Esta función siempre devuelve una cadena de texto, incluso si el usuario introduce números. Para trabajar con tipos de datos específicos, debes convertir esta entrada a su tipo correspondiente, por ejemplo, usando `int()` para convertir a entero.

#### 📜 **[Ejemplo 03: Interpolación de strings y lectura por teclado](Ejemplo-03/Readme.md)**

#### 🔥 **[Reto 03: Cotizador para la compra de auto](Reto-03/Readme.md)**
---


⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Sesion-02/Readme.md)➡️
