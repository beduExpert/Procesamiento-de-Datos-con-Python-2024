🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 03**](../Readme.md) ➡️ / 📝 `Ejemplo 04: Diccionarios y sus métodos`

## 🎯 Objetivo

Explorar los métodos y funciones esenciales de los diccionarios en Python para manipular datos, llave-valor.


## 🚀 Introducción

Los diccionarios en Python son estructuras de datos que almacenan información en pares clave-valor, siendo ideales para accesos rápidos y eficientes a sus elementos, así mismo a partir de Python 3.7, los diccionarios conservan el orden en el se insertaron los elementos.

### 🔦 **Sintaxis básica de diccionarios:**

```python
# Declaración de diccionarios, con o sin elementos.
diccionario_vacio = {}
diccionario_vacio = dict()
datos = {'nombre': 'Mario', 'edad': 30, 'ciudad': 'Saltillo'}
```
### 🔦 **Acceso a los elementos:**

```python
# Acceso mediante la clave
datos = {'nombre': 'Mario', 'edad': 30, 'ciudad': 'Saltillo'}
print(datos['nombre'])  # Salida: Mario
print(datos['edad'])  # Salida: 30
print(datos['ciudad'])  # Salida: Saltillo
```
### 🧰 **Métodos Comunes de Diccionarios:**

| Método                | Descripción |
|-----------------------|-------------|
| `get(key, default)`   | Devuelve el valor de `key` si existe, si no, `default`. |
| `update({key: value})`| Actualiza el diccionario con los pares clave-valor proporcionados. |
| `keys()`              | Devuelve una vista de las claves del diccionario. |
| `values()`            | Devuelve una vista de los valores del diccionario. |
| `items()`             | Devuelve una vista de los pares clave-valor en el diccionario. |
| `pop(key)`            | Elimina la clave `key` y devuelve su valor. |
| `clear()`             | Elimina todos los elementos del diccionario. |

### 🔦 **Ejemplos de métodos comunes de diccionarios:**

1. **`get()`** - Obtener valor de una clave:
   ```python
   persona = {'nombre': 'Magda', 'edad': 30}
   print(persona.get('nombre', 'No encontrado'))  # Ana
   print(persona.get('profesión', 'No encontrado'))  # No encontrado
   ```

2. **`update()`** - Actualizar el diccionario:
   ```python
   persona = {'nombre': 'Magda', 'edad': 30}
   persona.update({'edad': 25, 'ciudad': 'Barcelona'})
   print(persona)  # {'nombre': 'Magda', 'edad': 25, 'ciudad': 'Barcelona'}
   ```

3. **`pop()`** - Eliminar una clave:
   ```python
   persona = {'nombre': 'Ana', 'edad': 24}
   edad = persona.pop('edad')
   print(edad)  # 24
   print(persona)  # {'nombre': 'Ana'}
   ```

---

### 🔄 **Iteración sobre diccionarios:**

Para recorrer un diccionario, puedes utilizar un ciclo `for` para iterar sobre las claves, valores o pares clave-valor del diccionario.

```python
# Iterar sobre claves y valores
datos = {'nombre': 'Carlos', 'edad': 28, 'ciudad': 'Madrid'}
for clave, valor in datos.items():
    print(f"{clave}: {valor}") 
```

### 📝 **Diccionarios y comprensión:**

Los diccionarios también pueden ser creados y manipulados mediante comprensiones de diccionarios, similar a las comprensiones de listas.

```python
# Crear un diccionario con comprensión
cuadrados = {x: x**2 for x in range(6)}
print(cuadrados)  # {0: 0, 1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
```

---

### 💡 **Sabías que...**

Los diccionarios en Python son implementados como tablas hash internamente, lo que permite que las operaciones de acceso, inserción y eliminación sean muy eficientes, generalmente en tiempo O(1).

Big-O Notation es una notación matemática que describe el comportamiento de una función cuando el argumento tiende a un valor específico o al infinito. En el caso de los diccionarios, las operaciones de acceso, inserción y eliminación son O(1), lo que significa que su tiempo de ejecución es constante, independientemente del tamaño del diccionario.

Su estructura es muy similar a un objeto JSON, que veremos más adelante en el curso.

---

⬅️ [`Anterior`](../Readme.md) | [`Siguiente`](../Reto-02/Readme.md) ➡️