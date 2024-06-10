🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 03**](../Readme.md) ➡️ / 📝 `Ejemplo 03: Conjuntos y sus métodos`

## 🎯 Objetivo

Explorar los métodos y funciones esenciales de los conjuntos en Python para manejar colecciones de elementos únicos.

---

## 🚀 Introducción

Los conjuntos o `set()` en Python son colecciones desordenadas de datos únicos y mutables, que permiten operaciones matemáticas de conjuntos como uniones, intersecciones, diferencias, entre otras. Su naturaleza desordenada los hace ideales para la gestión de datos donde la unicidad es más importante que el orden de los elementos.

---

### 🔦 **Sintaxis básica de conjuntos:**

```python
# Declaración de conjuntos, con o sin elementos.
conjunto_vacio = set()
numeros = {1, 2, 3, 4, 5}
elementos = {1, 'hola', True, 3.1416}
# Elementos duplicados se eliminan automáticamente.
duplicados = {1, 2, 3, 1, 2, 3} # {1, 2, 3}
```

### 🔦 **Acceso a elementos:**

A diferencia de las listas y tuplas, los conjuntos no soportan el acceso indexado. Para trabajar con elementos individuales, se utilizan métodos específicos como un `for` o `in`.


### 🧰 **Métodos Comunes de Conjuntos:**

| Método                | Descripción |
|-----------------------|-------------|
| `add(x)`              | Añade el elemento `x` al conjunto si no está presente. |
| `remove(x)`           | Elimina el elemento `x` del conjunto. Lanza `KeyError` si `x` no está presente. |
| `discard(x)`          | Elimina el elemento `x` del conjunto si está presente (sin lanzar errores). |
| `clear()`             | Elimina todos los elementos del conjunto. |
| `union(other)`        | Devuelve un nuevo conjunto que es la unión de este conjunto con otro(s). |
| `intersection(other)` | Devuelve un nuevo conjunto con elementos comunes entre este conjunto y otro(s). |
| `difference(other)`   | Devuelve un nuevo conjunto con elementos que están en este conjunto pero no en otro(s). |

### 🔦 **Ejemplos de métodos comunes de conjuntos:**

1. **`add()`** - Añadir un elemento al conjunto:
   ```python
   frutas = {'manzana', 'banana'}
   frutas.add('naranja')
   print(frutas)  # {'manzana', 'banana', 'naranja'}
   ```

2. **`remove()`** - Eliminar un elemento específico:
   ```python
   frutas = {'manzana', 'banana', 'naranja'}
   frutas.remove('banana')
   print(frutas)  # {'manzana', 'naranja'}
   ```

---

### 🔄 **Iteración sobre conjuntos:**

Los conjuntos soportan la iteración directa con un ciclo `for`.

```python
frutas = {'manzana', 'banana', 'naranja'}
for fruta in frutas:
    print(fruta) # manzana, banana, naranja
```

---

### 🔦 **Operaciones con Conjuntos:**

Los conjuntos soportan varias operaciones que permiten comparar contenidos y realizar operaciones matemáticas de conjuntos.

```python
# Operaciones de conjunto para uniones e intersecciones.
a = {1, 2, 3}
b = {3, 4, 5}
union = a.union(b)
interseccion = a.intersection(b)
print(union)  # {1, 2, 3, 4, 5}
print(interseccion)  # {3}
```
---

### 💡 **Sabías que...**

Existe una diferencia clave entre utilizar `in` e `==` para comparar o buscar elementos en estructuras de datos en Python.

#### 1. Por ejemplo  **`in`**:

La palabra reservada **`in`** verifica la presencia de un elemento dentro de una colección, como listas, tuplas, conjuntos y diccionarios. En los ciclos, "in" se utiliza tanto para iterar sobre los elementos de la colección como para comprobar si un elemento está incluido en la misma, mediante condiciones en sentencias if o while.

  ```python
  numeros = [1, 2, 3, 4, 5]

  # Iterar sobre los elementos de la lista.
  for numero in numeros:
      print(numero)

  # Verificar si el número 3 está en la lista.
  while 3 in numeros:
      numeros.remove(3)
  
  if 3 in numeros:
      print("El número 3 está en la lista.")
  ```

#### 2. Mientras que **`==`**:

El operador  **`==`** verifica la igualdad entre dos valores, lo que resulta especialmente útil para comparar tipos de datos como cadenas, números y booleanos. En los ciclos, == se emplea para comparar elementos de una colección con un valor específico, utilizando este operador dentro de condiciones en bucles para determinar si se cumple una igualdad específica.


  ```python
  nombres = ["Ana", "Luis", "Carlos"]
  for nombre in nombres:
      if nombre == "Luis":
          print("Hemos encontrado a Luis!")
  ```

### Diferencia clave:
- **`in`** pregunta si un elemento está presente en una colección.
- **`==`** comprueba si dos valores son exactamente iguales.

---


⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Ejemplo-04/Readme.md) ➡️