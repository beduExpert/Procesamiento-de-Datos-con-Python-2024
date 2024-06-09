🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 02**](../Readme.md) ➡️ / 📝 `Ejemplo 04: Ciclo While`

## 🎯 Objetivo

Implementar el funcionamiento básico sobre ciclos de repetición indefinidos, y como salir de ellos.

---

## 🚀 Comencemos

Los ciclos de repetición son una estructura de control que permite ejecutar un bloque de código múltiples veces. El ciclo `while` es un tipo de ciclo que se utiliza para ejecutar un bloque de código repetidamente mientras una condición específica sea verdadera, pero hay que tener cuidado de no caer en un ciclo infinito o `infinite loop`, ya que este se ejecutará indefinidamente hasta que se detenga manualmente, o colapse el sistema.

---

### 📌 **Sintaxis**

```python
while condición:
    # Bloque de código a ejecutar mientras la condición sea verdadera
```
### Ejemplo 1: Contador con `break`
Este ejemplo usa un contador para iterar hasta un número específico, deteniéndose con `break` si se cumple una condición particular.

```python
contador = 0
while True:
    if contador == 5:
        break
    print(contador)
    contador += 1

# Salida: Imprime los números del 0 al 4.
```

### Ejemplo 2: Bucle con `continue`
En este caso, se imprimirán números del 1 al 10, saltando el número 5 usando `continue`.

```python
contador = 1
while contador <= 10:
    if contador == 5:
        contador += 1
        continue
    print(contador)
    contador += 1

# Salida: Imprime los números del 1 al 10, excepto el 5.
```

### Ejemplo 3: Uso de `while` con evaluación de múltiples condiciones
Aquí, un bucle `while` se ejecuta mientras se cumplan dos condiciones.

```python
x = 1
while x < 10 and x % 2 == 1:
    print(f"x es {x}, aún es menor que 10 y es impar")
    x += 2

# Salida: Imprime "x es 1, aún es menor que 10 y es impar" y "x es 3, aún es menor que 10 y es impar".
```

### Ejemplo 4: Bucle `while` con input del usuario
Este ejemplo solicita al usuario que ingrese un texto y el bucle continúa hasta que el usuario escribe "salir".

```python
mensaje = ""
while mensaje != "salir":
    mensaje = input("Escribe un mensaje: ")
    if mensaje == "salir":
        print("Saliendo del programa...")
        break
    print(f"Tu mensaje fue: {mensaje}")

# Salida: El programa solicita al usuario que ingrese un mensaje hasta que escriba "salir".
```

### Ejemplo 5: Bucle `while` con `match case`
Este es un ejemplo de cómo se puede usar `match case` dentro de un bucle `while` para manejar múltiples opciones.

```python
opcion = 0
while True:
    opcion = int(input("Introduce un número (1-3) o 4 para salir: "))
    match opcion:
        case 1:
            print("Elegiste la opción 1")
        case 2:
            print("Elegiste la opción 2")
        case 3:
            print("Elegiste la opción 3")
        case 4:
            print("Gracias por utilizar el programa.")
            break
        case _:
            print("Opción no válida, intenta de nuevo.")

# Salida: El programa solicita al usuario que ingrese un número y muestra un mensaje correspondiente, 
# hasta que el usuario elige la opción 4 para salir.
```

---
### 💡¿Sabias que?...

Los ciclos while tienden a usarse en situaciones que requieren una condición de parada no determinada por el número de elementos a procesar, como esperar una entrada del usuario o la convergencia de un algoritmo hasta alcanzar un cierto nivel de precisión.

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Reto-02/Readme.md) ➡️