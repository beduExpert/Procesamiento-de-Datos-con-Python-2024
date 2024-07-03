🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 04**](../Readme.md) ➡️ / 📝 `Ejemplo 02: Funciones lambda`

## 🎯 Objetivo

Implementar funciones lambda en Python para simplificar la escritura de código y aumentar la eficiencia al realizar operaciones sencillas.

---

## 🚀 Comencemos

Las funciones lambda, también conocidas como funciones anónimas, permiten definir operaciones en una sola línea sin utilizar la palabra reservada `def`. Son ideales para simplificar el código y aumentar su legibilidad, especialmente en situaciones donde se necesita una operación sencilla que se utilizará solamente una vez.

---

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

1. **Lambdas con Argumentos Simples**: Toman uno o más argumentos y realizan una operación simple con ellos.
   ```python
    # Aplicación a la función lambda
    print((lambda x, y: x + y)(5, 3))  # salida: 8
   ```

2. **Lambdas como asignación de variables**: Se pueden asignar a variables para su posterior uso.
   ```python
    # Asignación de la función lambda a una variable
    suma = lambda x, y: x + y
    print(suma(5, 3))  # salida: 8
   ```

3. **Lambdas para Manejo Condicional**: Usan expresiones condicionales para realizar tareas más complejas.
   ```python
    par_o_impar = lambda x: "Par" if x % 2 == 0 else "Impar"

    # Aplicación a la función lambda
    print(par_o_impar(5))  # salida: Impar
   ```


---

### 💡 **Sabías que...**

Eficiencia en Procesamiento de Datos: Las funciones lambda son ampliamente utilizadas en el análisis de datos, especialmente con bibliotecas como pandas y NumPy. Permiten aplicar rápidamente operaciones sobre elementos de datos sin necesidad de definir funciones tradicionales. Por ejemplo, se pueden usar para transformar o filtrar datos directamente dentro de métodos de dataframe como `map(), filter(), y reduce()`.

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Reto-01/Readme.md) ➡️