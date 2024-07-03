🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 04**](../Readme.md) ➡️ / 📝 `Ejemplo 03: Control excepciones`

## 🎯 Objetivo

Implementar el manejo de excepciones en Python para escribir programas más seguros y confiables, evitando que se detengan inesperadamente.

---

## 🚀 Comencemos

En lenguajes de programación como Python, es común que los programas se detengan si se encuentra un error. Sin embargo, en muchas ocasiones, es preferible que el programa continúe ejecutándose, incluso si se presenta un error. Para manejar estos casos, Python cuenta con un sistema de excepciones que permite capturar y manejar errores de forma controlada.

---

### 🔦 **Sintaxis básica excepciones**

El manejo de excepciones en Python permite controlar el flujo del programa ante errores o situaciones inesperadas. En lugar de detenerse, el programa puede responder de forma adecuada y continuar operando o cerrar ordenadamente.


<!-- Sintaxis de una excepcion -->
```python
try:
    # Bloque de código que puede generar una excepción
    pass
except Exception as e:
    # Bloque de código que se ejecuta si se genera una excepción
    pass
else:
    # Bloque de código que se ejecuta si no se genera una excepción
    pass
finally:
    # Bloque de código que se ejecuta siempre, haya o no excepción
    pass
```

---

### 🛠️ **Excepciones mas comunes:**

| Número | Excepción             | Descripción                                                                                      |
|--------|-----------------------|--------------------------------------------------------------------------------------------------|
| 1      | `Exception`           | Clase base para todas las excepciones.                                                           |
| 2      | `ZeroDivisionError`   | Se genera cuando se intenta dividir un número por cero.                                          |
| 3      | `ValueError`          | Se genera cuando una función recibe un argumento con un valor inapropiado.                       |
| 4      | `TypeError`           | Se genera cuando se intenta realizar una operación con un tipo de dato incorrecto.               |
| 5      | `IndexError`          | Se genera cuando se intenta acceder a un índice fuera de rango en una lista o secuencia.         |
| 6      | `KeyError`            | Se genera cuando se intenta acceder a una clave que no existe en un diccionario.                 |
| 7      | `FileNotFoundError`   | Se genera cuando se intenta abrir un archivo que no existe.                                      |

Son algunas de las excepciones más comunes en Python, pero existen muchas más que se pueden consultar en la [documentación oficial](https://docs.python.org/3/library/exceptions.html).

<!-- Vamos a generar algunos errores de acuerdo a la tabla -->
---
### 🔦 **Veamos algunos ejemplos de excepciones:**

1. **Manejo de entrada de datos en un formulario**: Supongamos que un programa necesita obtener un número entero del usuario, y es importante que este dato sea válido para continuar con la operación.

   ```python
   try:
      edad = int(input("Ingrese su edad: "))
   except ValueError:
      print("La entrada no es un número entero válido.")
   else:
      print(f"Edad ingresada: {edad}")
   finally:
      print("Operación de ingreso de edad completada.")
   ```

2. **División segura**: Este código realiza una división, pero maneja el caso en que el divisor sea cero, lo cual es un error común.

   ```python
   try:
      numerador = 10
      denominador = 0
      resultado = numerador / denominador
   except ZeroDivisionError:
      print("No se puede dividir por cero.")
   else:
      print(f"El resultado de la división es {resultado}.")
   finally:
      print("Operación de división completada.")
   ```


El uso de la palabra reservada `else` y `finally` no es obligatorio, pero es una buena práctica incluirlos para asegurarse de que las operaciones se completen correctamente.

---


### 💡 **Sabías que...**

En el bloque except, puedes nombrar la excepción capturada para obtener más información sobre el error. Esto se hace especificando el tipo de excepción esperado..

```python
try:
    # Código que puede generar una excepción
    pass
except ValueError as e:
    # Código que se ejecuta si se genera una excepción de tipo ValueError
    print(f"Error de valor: {e}")
except FileNotFoundError as e:
    # Código que se ejecuta si se genera una excepción de tipo FileNotFoundError
    print(f"Error de archivo no encontrado: {e}")
```

`Raise` en Python se utiliza para lanzar intencionalmente excepciones, lo que ayuda a gestionar condiciones inesperadas en un programa.


```python
def verificar_edad(edad):
    if edad < 18:
        raise ValueError("Acceso denegado. Debes ser mayor de edad.")
    print("Acceso permitido.")

try:
    verificar_edad(16)
except ValueError as e:
    print(e)
```
---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Reto-02/Readme.md) ➡️