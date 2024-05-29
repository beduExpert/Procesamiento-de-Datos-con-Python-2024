🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 04**](../Readme.md) ➡️ / 📝 `Ejemplo 04: Map, Filter y Reduce`

## 🎯 Objetivo

Implementar el manejo de las funciones`map()`, `filter()` y `reduce()` en Python para optimizar el procesamiento de datos, mejorar la eficiencia y legibilidad del código en aplicaciones prácticas.

## 🚀 Introducción

En ciencia de datos, aplicar funciones a elementos de una lista es común y puede ser tedioso. Python simplifica este proceso mediante `map()`, `filter()` y `reduce()`, que permiten manipular eficientemente grandes volúmenes de datos, aplicando, filtrando y reduciendo funciones en menos líneas de código.


### 🔦 **Sintaxis y uso básico:**

1. **`map(función, colección)`**: Aplica una 'función' a cada elemento de la 'colección'.
2. **`filter(función, colección)`**: Filtra los elementos de una 'colección' de datos que no cumplan con la condición en la 'función'.
3. **`reduce(función, colección)`**: Aplica una 'función' de forma acumulativa a los elementos de la 'colección', reduciéndolos a un único valor de salida.

---

### 🔦 **Ejemplos de uso de Map, Filter y Reduce:**

1. #### Ejemplos con `map()`

    ```python
    # Usando una función normal:
    def cuadrado(x):
        return x ** 2

    numeros = [1, 2, 3, 4, 5]
    resultados = list(map(cuadrado, numeros))
    print(resultados)  # salida: [1, 4, 9, 16, 25]

    # Usando una función lambda:
    numeros = [1, 2, 3, 4, 5]
    resultados = list(map(lambda x: x ** 2, numeros))
    print(resultados)  # salida: [1, 4, 9, 16, 25]
    ```

2. #### Ejemplos con `filter()`

    ```python
    # Usando una función normal:
    def es_par(x):
        return x % 2 == 0

    numeros = [1, 2, 3, 4, 5, 6]
    pares = list(filter(es_par, numeros))
    print(pares)  # salida: [2, 4, 6]

    # Usando una función lambda:
    numeros = [1, 2, 3, 4, 5, 6]
    pares = list(filter(lambda x: x % 2 == 0, numeros))
    print(pares)  # salida: [2, 4, 6]
    ```

3. #### Ejemplos con `reduce()`

    ```python
    from functools import reduce

    def sumar(x, y):
        return x + y

    numeros = [1, 2, 3, 4, 5]
    total = reduce(sumar, numeros)
    print(total)  # salida: 15

    # Usando una función lambda:
    numeros = [1, 2, 3, 4, 5]
    total = reduce(lambda x, y: x + y, numeros)
    print(total)  # salida: 15
    ```
---

- Cuando intentas imprimir directamente un objeto `map` o `filter` en Python, no ves los valores contenidos en ellos, sino una representación del objeto en sí, que incluye la dirección de memoria en la que está almacenado. Por ejemplo, si intentas imprimir un objeto `map` o `filter` directamente, obtendrás algo como esto:

    ```python
    resultados_map = map(lambda x: x ** 2, [1, 2, 3, 4, 5])
    print(resultados_map)  # <map object at 0x7f9d1f3b3a90>
    ```

- ¿Cómo visualizar los resultados?

- Para ver los resultados contenidos en un objeto `map` o `filter`, necesitas convertir el iterador en una estructura de datos que pueda ser visualizada completamente, como una lista. Esto se hace utilizando la función `list()` para consumir todos los elementos del iterador y almacenarlos en una lista, que luego se puede imprimir de manera legible:

---


### 💡 **Sabías que...**

Para poder utilizar reduce, es necesario importar la función desde el módulo `functools`, esto es debido a que en Python 3, `reduce()` fue movido a este módulo, ya que en versiones anteriores estaba disponible como una función global.

---

⬅️ [**Anterior**](../Ejemplo-02/Readme.md) | [**Siguiente**](../Reto-03/Readme.md) ➡️