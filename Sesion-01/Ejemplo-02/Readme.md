🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 01**](../Readme.md) ➡️ / 📝 `Ejemplo 02: Operadores en Python`

## 🎯 Objetivo

🔍 Familiarizarse con los diferentes tipos de operadores en Python: aritméticos, relacionales, lógicos y de asignación, y aplicarlos en diferentes contextos para manejar y modificar valores de variables.

---

<!-- ## 🚀 Comencemos -->

### ➕ Operadores Aritméticos

🧮 Los operadores aritméticos permiten realizar cálculos matemáticos básicos como suma, resta, multiplicación y división.

| Operador | Nombre         | Ejemplo         |
|----------|----------------|-----------------|
| `+`      | Suma           | `x + y = 13`    |
| `-`      | Resta          | `x - y = 7`     |
| `*`      | Multiplicación | `x * y = 30`    |
| `/`      | División       | `x / y = 3.333` |
| `%`      | Módulo         | `x % y = 1`     |
| `**`     | Exponente      | `x ** y = 1000` |
| `//`     | Cociente       | `x // y = 3`    |


##### 📝 Ejemplo de operadores aritméticos:

```python
# Definir variables 'x' y 'y'.
x, y = 10, 3
print("Suma:", x + y)   # 13
print("Resta:", x - y)  # 7
print("Multiplicación:", x * y)  # 30
print("División:", x / y)  # 3.333
print("Módulo:", x % y)  # 1
print("Exponente:", x ** y)  # 1000
print("Cociente:", x // y)  # 3
```
---

### ➖ Operadores Relacionales

🔍 Estos operadores comparan dos valores y devuelven un valor booleano basado en la comparación.

- `==`: Igual a
- `!=`: No igual a
- `>`: Mayor que
- `<`: Menor que
- `>=`: Mayor o igual que
- `<=`: Menor o igual que


##### 📝 Ejemplo de operadores relacionales:

```python
# Operadores relacionales
print("Igual a:", x == y)  # False
print("No igual a:", x != y)  # True
print("Mayor que:", x > y)  # True
```
---

### 🔄 Operadores Lógicos

🤔 Utilizados para combinar condiciones booleanas.

- `and`: Devuelve `True` si ambos operandos son verdaderos.
- `or`: Devuelve `True` si al menos uno de los operandos es verdadero.
- `not`: Invierte el valor del operando.


##### 📝 Ejemplo de operadores lógicos:

```python
print("AND lógico:", (x > y) and (x < 15))  # True
print("OR lógico:", (x > y) or (x < 5))  # True
print("NOT lógico:", not (x > y))  # False
```
---

### ⏩ Operadores de Asignación

💻 Permiten asignar y modificar el valor de una variable de manera eficiente.

- `=`: Asignación simple.
- `+=`: Suma y asigna.
- `-=`: Resta y asigna.
- `*=`: Multiplica y asigna.
- `/=`: Divide y asigna.
- `%=`: Módulo y asigna.
- `**=`: Potencia y asigna.
- `//=`: División entera y asigna.


##### 📝 Ejemplo de operadores de asignación:

```python
# Operadores de asignación
x += 5  # x ahora es 15
print("x incrementado:", x)  # 15
x -= 5  # x ahora es 10
print("x decrementado:", x)  # 10
x *= 2  # x ahora es 20
print("x multiplicado:", x)  # 20
x /= 4  # x ahora es 5.0
print("x dividido:", x)  # 5.0
x %= 3  # x ahora es 2.0
print("x módulo:", x)  # 2.0
x **= 3  # x ahora es 8.0
print("x potenciado:", x)  # 8.0
x //= 3  # x ahora es 2.0
print("x cociente:", x)  # 2.0

# Operador Walrus
x = 5
print(y := x + 2)  # Salida: 7
# 'y' ahora contiene el resultado de la suma, y 'x' sigue siendo 5

# Equivalente a:
x = 5
y = x + 2
print(y)
```

---

### 💡 **¿Sabias que?...**

- **Manejo de excepciones**: 🚨 Al realizar una división por cero en Python, se lanza una excepción `ZeroDivisionError`. Este tipo de errores es común y se puede manejar adecuadamente para evitar que el programa se detenga abruptamente, esta funcionalidad la veremos en la sesión 04. 
  
- **Generación de números aleatorios**: 🎲 Python permite generar números aleatorios utilizando la librería `random`. Por ejemplo, `random.randint(1, 10)` genera un número aleatorio entre 1 y 10. Esta funcionalidad es útil para situaciones que requieren elementos de aleatoriedad, como simulaciones o juegos.

- **Operador Walrus (`:=`)**: 🧐 Introducido en Python 3.8, el operador Walrus permite hacer asignaciones de variables dentro de expresiones. Esto simplifica el código al reducir la cantidad de líneas necesarias para realizar ciertas tareas. Por ejemplo, puedes asignar y utilizar un valor al mismo tiempo sin necesidad de dos líneas separadas:

  ```python
    x = 5
    print(y := x + 2)  # Salida: 7
    # 'y' ahora contiene el resultado de la suma, y 'x´ sigue siendo 5.

    # Equivalente a:
    x = 5
    y = x + 2
    print(y)
    ```

-  El termino **PEMDAS** es un acrónimo que se utiliza para recordar el orden en el que las operaciones matemáticas deben ser evaluadas.  

  1. **P**arentheses (Paréntesis)
  1. **E**xponents (Exponentes)
  1. **M**ultiplication (Multiplicación)
  1. **D**ivision (División)
  1. **A**ddition (Suma)
  1. **S**ubtraction (Resta)

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Reto-02/Readme.md)➡️
