🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 03**](../Readme.md) ➡️ / 📝 `Ejemplo 01: Listas y sus métodos`

## 🎯 Objetivo

Explorar los métodos y funciones esenciales de las listas en Python para manipular datos.

---

## 🚀 Introducción

Las listas en Python son herramientas ideales para la ciencia de datos, capaces de almacenar elementos de distintos tipos y manipular datos de forma eficiente.

---

### 🔦 **Sintaxis básica de listas:**

```python
# Declaración de listas, con o sin elementos.
lista_vacia = []
lista_vacia = list()
numeros = [1, 2, 3, 4, 5]
elementos = [1, 'hola', True, 3.1416]
```
### 🔦 **Acceso a elementos:**

```python
# Acceso mediante índice, que comienza en 0
numeros = [10, 20, 30, 40, 50]
print(numeros[0])  # Salida: 10
print(numeros[2])  # Salida: 30
```
### 🧰 **Métodos Comunes de Listas:**

| Método                | Descripción |
|-----------------------|-------------|
| `append(x)`           | Agrega `x` al final de la lista. |
| `extend(iterable)`    | Agrega todos los elementos del `iterable` al final. |
| `insert(i, x)`        | Inserta `x` en la posición `i`. |
| `remove(x)`           | Elimina el primer elemento con valor `x`. |
| `pop([i])`            | Elimina y devuelve el elemento en la posición `i`, o el último si `i` no se especifica. |
| `clear()`             | Vacía la lista. |
| `index(x[, start[, end]])` | Devuelve el índice del primer `x` dentro del rango opcional `start` a `end`. |
| `count(x)`            | Cuenta las apariciones de `x`. |
| `sort(key=None, reverse=False)` | Ordena los elementos. `key` y `reverse` permiten personalizar el orden. |
| `reverse()`           | Invierte el orden de los elementos. |
| `copy()`              | Devuelve una copia de la lista. |

### 🔦 **Ejemplos de métodos comunes de listas:**

1. **`append()`** - Agregar a la lista:
   ```python
   nombres = ['Ana', 'Luis', 'Carlos']
   nombres.append('Sofía')
   print(nombres)  # ['Ana', 'Luis', 'Carlos', 'Sofía']
   ```

2. **`pop()`** - Eliminación y retorno de un elemento:
   ```python
   numeros = [10, 20, 30, 40, 50]
   ultimo = numeros.pop()
   print(ultimo)  # 50
   print(numeros)  # [10, 20, 30, 40]
   ```

3. **`sort()`** - Ordenación de la lista:
   ```python
   edades = [34, 23, 31, 18, 27]
   edades.sort()
   print(edades)  # [18, 23, 27, 31, 34]
   ```

---

### 🍰 **Slicing:**

El slicing permite acceder a subconjuntos de elementos en una lista mediante rangos.

```python
# Sublistas mediante slicing.
# Sintaxis: lista[inicio:fin:incremento], el rango es [inicio, fin).

numeros = [10, 20, 30, 40, 50, 60, 70, 80]
sublista = numeros[2:5]
print(sublista)  # [30, 40, 50]
```
### 📝 **List Comprehensions:**

Las list comprehensions son una forma concisa de crear listas en Python. Permiten crear listas a partir de iterables, aplicando una expresión a cada elemento, en una sola línea.

```python
# Crear lista de cuadrados
numeros = [1, 2, 3, 4, 5]
cuadrados = [numero ** 2 for numero in numeros]
print(cuadrados)  # [1, 4, 9, 16, 25]
```

---

### 💡 **Sabías que...**

Si intentamos acceder a un índice que no existe en una lista, Python lanzará un error de tipo IndexError. Por ejemplo, si intentamos acceder al índice 100 de una lista con solo 3 elementos, obtendremos un error.

```python
numeros = [10, 20, 30]

# Intentar acceder a un índice que no existe
print(numeros[100])  # Error: IndexError: list index out of range


# Intentar acceder a un índice negativo
print(numeros[-1])  # Salida: 30
```

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Ejemplo-02/Readme.md) ➡️