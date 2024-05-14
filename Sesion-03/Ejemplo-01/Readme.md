🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 03**](../Readme.md) ➡️ / 📝 `Ejemplo 01: Listas y sus métodos`

## 🎯 Objetivo

Aplicar y explorar los métodos y funciones esenciales de las listas en Python.

## 🚀 Comencemos

Las listas en Python son estructuras extremadamente versátiles y flexibles, capaces de almacenar elementos de distintos tipos, como números, cadenas, booleanos y listas anidadas. Estas características las convierten en herramientas ideales para manipular datos de forma eficiente. Son realmente útiles en tareas de ciencia de datos, incluyendo la limpieza y preparación de datos, como selección de columnas específicas, eliminación de valores nulos, así como generación de nuevas columnas a partir de datos ya existentes.

### Sintaxis

```python
# Sintaxis de una lista
lista = [elemento1, elemento2, elemento3, ..., elementoN]

# Existen diferentes formas validas de declarar una lista

# 1. Una lista vacía
lista_vacia = []

# 2. Declarando el tipo list
lista_vacia = list()

# 3. Lista con elementos
numeros = [1, 2, 3, 4, 5]

# 4. Lista con elementos de diferentes tipos
elementos = [1, 'hola', True, 3.1416]

# Entre otros...
```

Un objeto tipo lista en Python  cuenta con una serie de métodos y funciones que permiten realizar operaciones y modificaciones sobre sus elementos. 

Vamos a describir algunos:

1. **`append(x)`**: Agrega un elemento `x` al final de la lista.

2. **`extend(iterable)`**: Extiende la lista agregando todos los elementos del `iterable` al final.

3. **`insert(i, x)`**: Inserta un elemento `x` en la posición `i` especificada.

4. **`remove(x)`**: Elimina el primer elemento de la lista cuyo valor es `x`. Lanza un error si el elemento no está presente.

5. **`pop([i])`**: Elimina y devuelve el elemento en la posición `i`. Si no se especifica `i`, `pop()` elimina y devuelve el último elemento de la lista.

6. **`clear()`**: Elimina todos los elementos de la lista, dejándola vacía.

7. **`index(x[, start[, end]])`**: Devuelve el índice del primer elemento cuyo valor es `x`. Los argumentos `start` y `end` son opcionales y se utilizan para limitar la búsqueda a una subsección específica de la lista.

8. **`count(x)`**: Cuenta la cantidad de veces que el valor `x` aparece en la lista.
|
9. **`sort(key=None, reverse=False)`**: Ordena los elementos de la lista in situ (los elementos se modifican en la misma lista). `key` y `reverse` permiten especificar la función de ordenación y si se debe ordenar en orden ascendente o descendente, respectivamente.

10. **`reverse()`**: Invierte el orden de los elementos de la lista in situ.

11. **`copy()`**: Devuelve una copia superficial de la lista. Equivalente a `lista[:]`.


---

🖥️ Que les parece si vemos algunos ejemplos de los métodos mas utilizados en las listas.


1. **`append()`** - Agregar un elemento al final de la lista:
   ```python
   nombres = ['Ana', 'Luis', 'Carlos']
   nombres.append('Sofía')  # Agrega 'Sofía' al final de la lista
   print(nombres)  # ['Ana', 'Luis', 'Carlos', 'Sofía']
   ```

2. **`pop()`** - Eliminar un elemento por su índice y devolverlo:
   ```python
   numeros = [10, 20, 30, 40, 50]
   ultimo = numeros.pop()  # Elimina y devuelve el último elemento
   print(ultimo)  # 50
   print(numeros)  # [10, 20, 30, 40]
   ```

3. **`sort()`** - Ordenar los elementos de la lista in situ:
   ```python
   edades = [34, 23, 31, 18, 27]
   edades.sort()  # Ordena la lista de menor a mayor
   print(edades)  # [18, 23, 27, 31, 34]
   ```

4. **`count()`** - Contar la cantidad de veces que un elemento aparece en la lista:
   ```python
   colores = ['rojo', 'verde', 'azul', 'rojo', 'amarillo', 'rojo']
   cuenta_rojo = colores.count('rojo')  # Cuenta cuántas veces aparece 'rojo'
   print(cuenta_rojo)  # 3
   ```

5. **`reverse()`** - Invertir el orden de los elementos de la lista:
   ```python
    numeros = [10, 20, 30, 40, 50]
    numeros.reverse()  # Invierte el orden de los elementos en la lista
    print(numeros)  # [50, 40, 30, 20, 10]
   ```

---

## 🚀 List comprehension

Las listas por comprensión o list comprehension son una forma concisa y elegante de crear listas en Python. Permitiendo crear listas a partir de secuencias o iterables de forma más eficiente y legible, en una sola línea de código.

### Sintaxis

```python
# Sintaxis de una lista por comprensión
nueva_lista = [expresion for elemento in iterable if condicion]
```

Aqui podemos observar que la sintaxis de una lista por comprensión es muy similar a la de un ciclo `for`, con la diferencia de que se escribe en una sola línea y es más legible.

### Usando un ciclo `for` convencional:

```python
# Lista de números
numeros = [1, 2, 3, 4, 5]

# Lista vacía para almacenar los cuadrados
cuadrados = []

# Bucle for para calcular el cuadrado de cada número y agregarlo a la lista cuadrados
for numero in numeros:
    cuadrados.append(numero ** 2)

print(cuadrados)  # [1, 4, 9, 16, 25]
```

### Usando `list comprehension`:

```python
# Lista de números
numeros = [1, 2, 3, 4, 5]

# List comprehension para obtener los cuadrados
cuadrados = [numero ** 2 for numero in numeros]

print(cuadrados)  # [1, 4, 9, 16, 25]
```

Como puedes ver, la comprensión de listas no solo reduce la cantidad de código necesario, sino que también es más directa y a menudo más fácil de entender a primera vista. Este método es muy popular en Python por su eficiencia y simplicidad.

---
### 💡¿Sabias que?...

Si intentamos acceder a un índice que no existe en una lista, Python lanzará un error de tipo `IndexError`. Por ejemplo, si intentamos acceder al índice 100 de una lista con solo 3 elementos, obtendremos un error.

```python
numeros = [10, 20, 30]

# Intentar acceder a un índice que no existe
print(numeros[100])  # Error: IndexError: list index out of range


# Intentar acceder a un índice negativo
print(numeros[-1])  # Salida: 30
```

---

⬅️ [`Anterior`](../Readme.md) | [`Siguiente`](../Ejemplo-02/Readme.md) ➡️