🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 01**](../Readme.md) ➡️ / 📝 `Ejemplo 04: Operadores Relacionales`

## 🎯 Objetivo

Aplicar el funcionamiento básico sobre los diferentes tipos de operadores relacionales que existen en Python.

## 🚀 Comencemos

Los operadores relacionales son utilizados para comparar dos valores, y el resultado de esta comparación es un valor booleano (`True` o `False`). Estos operadores son fundamentales en la toma de decisiones y en el control del flujo de programas.


### 📜 Lista de operadores relacionales

- **Igual (`==`)**:  Verifica si dos valores son iguales.
- **Diferente que (`!=`)**: Verifica si dos valores son diferentes.
- **Mayor que (`>`)**: Comprueba si el valor de la izquierda es mayor que el de la derecha.
- **Menor que (`<`)**: Comprueba si el valor de la izquierda es menor que el de la derecha.
- **Mayor o igual que (`>=`)**: Evalúa si el valor de la izquierda es mayor o igual al de la derecha.
- **Menor o igual que (`<=`)**: Evalúa si el valor de la izquierda es menor o igual al de la derecha.

---

### 🧠 Ejemplos de operadores relacionales

### Ejemplo de igual (`==`)

```python
# Comparando números
print(10 == 10)  # Salida: True

# Comparando cadenas
print('hola' == 'hola')  # Salida: True

# Comparando números y cadenas
print('1' == 1)  # Salida: False
```

### Ejemplo de diferente que (`!=`)

```python
# Comparando números
print(10 != 10)  # Salida: False

# Comparando cadenas
print('hola' != 'adios')  # Salida: True

# Comparando cadenas y números
print('1' != 1)  # Salida: True
```

### Ejemplo de mayor que (`>`)

```python
# Comparando números
print(10 > 5)  # Salida: True

# Comparando caracteres (ASCII value comparison)
print('b' > 'a')  # Salida: True

# Comparando valores flotantes
print(10.1 > 10.09)  # Salida: True
```

### Ejemplo de menor que (`<`)

```python
# Comparando números
print(5 < 10)  # Salida: True

# Comparando caracteres
print('a' < 'b')  # Salida: True

# Comparando valores flotantes
print(0.99 < 1.1)  # Salida: True
```

### Ejemplo de mayor o igual que (`>=`)

```python
# Comparando números iguales
print(10 >= 10)  # Salida: True

# Comparando números diferentes
print(15 >= 10)  # Salida: True
```

### Ejemplo de menor o igual que (`<=`)

```python
# Comparando números iguales
print(10 <= 10)  # Salida: True

# Comparando números diferentes
print(5 <= 10)  # Salida: True
```

---

### 💡 **¿Sabias que?...**

Existe una funcionalidad adicional en Python que permite generar números aleatorios, para ello se debe importar la librería `random` y utilizar la función `randint` de la siguiente manera:

```python
import random

print(random.randint(1, 10))  # Salida: un número aleatorio entre 1 y 10
```

⬅️ [`Anterior`](../Readme.md) | [`Siguiente`](../Ejemplo-05/Readme.md)➡️