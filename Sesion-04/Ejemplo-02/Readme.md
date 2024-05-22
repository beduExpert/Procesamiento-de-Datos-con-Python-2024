🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 04**](../Readme.md) ➡️ / 📝 `Ejemplo 02: Funciones lambda`

## 🎯 Objetivo

Implementar funciones lambda en Python para simplificar la escritura de código y aumentar la eficiencia al realizar operaciones sencillas.

## 🚀 Introducción

Las funciones lambda, también conocidas como funciones anónimas, permiten definir operaciones en una sola línea sin utilizar la palabra reservada `def`. Son ideales para simplificar el código y aumentar su legibilidad, especialmente en situaciones donde se necesita una operación sencilla que se utilizará solamente una vez.

Así mismo también pueden tomar cualquier número de argumentos, pero solo puede tener una expresión. Aunque no es necesario, es común utilizar funciones lambda en combinación con funciones como `map()`, `filter()` y `reduce()`, que veremos mas adelante.

### 🔦 **Sintaxis básica de una función lambda:**

```python
lambda argumentos: expresión
```

### 🛠️ **Estructura de una función lambda:**

1. **`lambda`**: Palabra reservada que indica la definición de una función anónima.
2. **`argumentos`**: Son las `variables` que recibe la función, separados por comas.
3. **`:`**: Separador entre los argumentos y la expresión.
4. **`expresión`**: Operación que realiza la función y cuyo resultado se retorna.

---

### 🔦 **Ejemplos de funciones lambda:**

1. **Lambdas Sin Argumentos**: Son aquellas que no requieren datos de entrada.
   ```python
    # Aplicación a la función lambda
    print((lambda: "Hola Mundo")())  # salida: Hola Mundo
   ```

2. **Lambdas con Argumentos Simples**: Toman uno o más argumentos y realizan una operación simple con ellos.
   ```python
    # Aplicación a la función lambda
    print((lambda x, y: x + y)(5, 3))  # salida: 8
   ```

3. **Lambdas como asignación de variables**: Se pueden asignar a variables para su posterior uso.
   ```python
    # Asignación de la función lambda a una variable
    suma = lambda x, y: x + y
    print(suma(5, 3))  # salida: 8
   ```

4. **Lambdas para Manejo Condicional**: Usan expresiones condicionales para realizar tareas más complejas.
   ```python
    par_o_impar = lambda x: "Par" if x % 2 == 0 else "Impar"

    # Aplicación a la función lambda
    print(par_o_impar(5))  # salida: Impar
   ```

5. **Lambdas con `*args` y `**kwargs`**: Pueden aceptar un número variable de argumentos, al igual que las funciones definidas con `def`.
   ```python
   lambda *args: sum(args)  # Suma un número indefinido de argumentos
   lambda **kwargs: sum(kwargs.values())  # Suma los valores de un diccionario
   ```

---

### 💡 **Sabías que...**

Eficiencia en Procesamiento de Datos: Las funciones lambda son ampliamente utilizadas en el análisis de datos, especialmente con bibliotecas como pandas y NumPy. Permiten aplicar rápidamente operaciones sobre elementos de datos sin necesidad de definir funciones tradicionales. Por ejemplo, se pueden usar para transformar o filtrar datos directamente dentro de métodos de dataframe como `map(), filter(), y reduce()`.


---

⬅️ [`Anterior`](../Readme.md) | [`Siguiente`](../Reto-01/Readme.md) ➡️