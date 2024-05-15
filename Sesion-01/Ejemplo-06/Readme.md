🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 01**](../Readme.md) ➡️ / 📝 `Ejemplo 06: Operadores de Asignación`


## 🎯 Objetivo

Implementar los principales operadores de asignación en Python para manejar y modificar valores almacenados en variables, realización de cálculos y la gestión de datos eficiente.

## 🚀 Comencemos

Los operadores de asignación facilitan la actualización de valores de una manera mucho mas limpia y concisa. Estos operadores combinan operaciones aritméticas o lógicas con la asignación tradicional, permitiendo modificar el valor de una variable sin la necesidad de repetir su nombre. Este enfoque acelera la escritura del código, lo hace más intuitivo y menos propenso a errores, contribuyendo a la claridad del programa.

### 📜 Lista de operadores de asignación

- `=`: Asignación simple.
- `+=`: Asignación con suma.
- `-=`: Asignación con resta.
- `*=`: Asignación con multiplicación.
- `/=`: Asignación con división.
- `%=`: Asignación con módulo.
- `**=`: Asignación con exponente.
- `//=`: Asignación con división entera.

### 🧠 Ejemplos de operadores  de asignación

### Asignación Simple (`=`)

Asigna un valor directo a una variable.

```python
x = 10  # x ahora es 10
```

### Asignación con Suma (`+=`)

Suma un valor al valor de la variable y actualiza la variable con el resultado.

```python
x = 5
x += 3  # x ahora es 8
```

### Asignación con Resta (`-=`)

Resta un valor del valor de la variable y actualiza la variable con el resultado.

```python
x = 5
x -= 2  # x ahora es 3
```

### Asignación con Multiplicación (`*=`)

Multiplica el valor de la variable por un valor y actualiza la variable con el resultado.

```python
x = 4
x *= 3  # x ahora es 12
```

### Asignación con División (`/=`)

Divide el valor de la variable por un valor y actualiza la variable con el resultado.

```python
x = 10
x /= 2  # x ahora es 5
```

### Asignación con Módulo (`%=`)

Aplica un módulo entre el valor de la variable y un valor y actualiza la variable con el resultado.

```python
x = 10
x %= 3  # x ahora es 1
```

### Asignación con Exponente (`**=`)

Eleva el valor de la variable a la potencia de un valor y actualiza la variable con el resultado.

```python
x = 2
x **= 3  # x ahora es 8
```

### Asignación con División Entera (`//=`)

Aplica una división entera entre el valor de la variable y un valor y actualiza la variable con el resultado.

```python
x = 10
x //= 3  # x ahora es 3
```

---

### 💡 **¿Sabias que?...**

En Python es la existencia del operador "Walrus" o ":=", introducido en Python 3.8, permite hacer asignaciones de variables dentro de expresiones, lo cual puede simplificar el código y reducir la cantidad de líneas necesarias para realizar ciertas tareas.

```python
# Ejemplo de uso del operador Walrus
x = 5
print(y := x + 2)  # Salida: 7

# La variable 'y' ahora contiene el resultado de la suma
print(y)  # Salida: 7

# La variable x no ha sido modificada
print(x)  # Salida: 5
```
---
⬅️ **[`Anterior`](../Readme.md) | [`Siguiente`](../Ejemplo-07/Readme.md)** ➡️