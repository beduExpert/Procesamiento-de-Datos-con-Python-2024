🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 02**](../Readme.md) ➡️ / 📝 `Ejemplo 01: Sentencia If`

## 🎯 Objetivo

Aplicar los principios básicos sobre el control del flujo de un programa, usando la sentencia if.

## 🚀 Comencemos

Las sentencias condicionales en Python permiten ejecutar diferentes bloques de código según se cumplan o no ciertas condiciones. Las sentencias más comunes son `if`, `if-else`, y `if` anidados.

## Sentencia `if`

La sentencia `if` se utiliza para ejecutar un bloque de código solo si una condición es verdadera.

### Sintaxis

```python
if condición:
    # Bloque de código a ejecutar si la condición es verdadera
```

### Ejemplo 1: Verificar si un número es positivo

```python
# Verificar si un número es positivo
numero = 10

if numero > 0:
    print("El número es positivo.")
```

### Ejemplo 2: Verificar si una persona es mayor de edad

```python
# Verificar si una persona es mayor de edad
edad = 20

if edad >= 18:
    print("Eres mayor de edad.")
```

### Ejemplo 3: Verificar si una cadena no está vacía

```python
# Verificar si una cadena no está vacía
cadena = "Hola, mundo"

if cadena:
    print("La cadena no está vacía.")
```

### Ejemplo 4: Verificar si un número es par

```python
# Verificar si un número es par
numero = 4

if numero % 2 == 0:
    print("El número es par.")
```

### Ejemplo 5: Verificar si una variable tiene un valor específico

```python
# Verificar si una variable tiene un valor específico
color = "rojo"

if color == "rojo":
    print("El color es rojo.")
```


## Sentencia `if-else`

La sentencia `if-else` permite ejecutar un bloque de código si la condición es verdadera y otro bloque si la condición es falsa.

### Sintaxis

```python
if condición:
    # Bloque de código a ejecutar si la condición es verdadera
else:
    # Bloque de código a ejecutar si la condición es falsa
```

### Ejemplo 1: Verificar si un número es positivo o negativo

```python
# Verificar si un número es positivo o negativo
numero = -5

if numero >= 0:
    print("El número es positivo.")
else:
    print("El número es negativo.")
```

### Ejemplo 2: Verificar si una persona es mayor o menor de edad

```python
# Verificar si una persona es mayor o menor de edad
edad = 16

if edad >= 18:
    print("Eres mayor de edad.")
else:
    print("Eres menor de edad.")
```

### Ejemplo 3: Verificar si una cadena está vacía o no

```python
# Verificar si una cadena está vacía o no
cadena = ""

if cadena:
    print("La cadena no está vacía.")
else:
    print("La cadena está vacía.")
```

### Ejemplo 4: Verificar si un número es par o impar

```python
# Verificar si un número es par o impar.
# Considera este ejemplo importante, ya que lo aplican en muchas entrevistas de trabajo.
numero = 7

if numero % 2 == 0:
    print("El número es par.")
else:
    print("El número es impar.")
```

### Ejemplo 5: Verificar si una persona tiene permiso para votar

```python
# Verificar si una persona tiene permiso para votar
edad = 17
ciudadano = True

if edad >= 18 and ciudadano:
    print("Tienes permiso para votar.")
else:
    print("No tienes permiso para votar.")
```

## Sentencia `if-elif-else`

La sentencia `if-elif-else` permite manejar múltiples condiciones. Se pueden agregar tantos bloques `elif` como sean necesarios.

### Sintaxis

```python
if condición1:
    # Bloque de código a ejecutar si la condición1 es verdadera
elif condición2:
    # Bloque de código a ejecutar si la condición2 es verdadera
else:
    # Bloque de código a ejecutar si ninguna condición anterior es verdadera
```

### Ejemplo 1: Calificar una nota

```python
# Calificar una nota
nota = 85

if nota >= 90:
    print("Calificación: A")
elif nota >= 80:
    print("Calificación: B")
elif nota >= 70:
    print("Calificación: C")
elif nota >= 60:
    print("Calificación: D")
else:
    print("Calificación: F")
```

### Ejemplo 2: Clasificar la temperatura

```python
# Clasificar la temperatura
temperatura = 25  # grados Celsius

if temperatura > 30:
    print("Hace calor.")
elif temperatura >= 20:
    print("El clima es templado.")
elif temperatura >= 10:
    print("Hace fresco.")
else:
    print("Hace frío.")
```

### Ejemplo 3: Determinar la categoría de edad

```python
# Determinar la categoría de edad
edad = 45

if edad < 13:
    print("Eres un niño.")
elif edad < 20:
    print("Eres un adolescente.")
elif edad < 65:
    print("Eres un adulto.")
else:
    print("Eres un adulto mayor.")
```



## Sentencias `if` anidadas

Las sentencias `if` anidadas se utilizan cuando se necesita evaluar una condición dentro de otra condición.

### Sintaxis

```python
if condición1:
    # Bloque de código a ejecutar si la condición1 es verdadera
    if condición2:
        # Bloque de código a ejecutar si la condición2 también es verdadera
    else:
        # Bloque de código a ejecutar si la condición2 es falsa
else:
    # Bloque de código a ejecutar si la condición1 es falsa
```

### Ejemplo 1: Verificar si un número es positivo, negativo o cero y si es par o impar

```python
# Verificar si un número es positivo, negativo o cero y si es par o impar
numero = -4

if numero >= 0:
    if numero == 0:
        print("El número es cero.")
    elif numero % 2 == 0:
        print("El número es positivo y par.")
    else:
        print("El número es positivo e impar.")
else:
    if numero % 2 == 0:
        print("El número es negativo y par.")
    else:
        print("El número es negativo e impar.")
```

### Ejemplo 2: Verificar el acceso a un sitio web basado en edad y membresía

```python
# Verificar el acceso a un sitio web basado en edad y membresía
edad = 21
es_miembro = True

if edad >= 18:
    if es_miembro:
        print("Tienes acceso completo al sitio web.")
    else:
        print("Necesitas ser miembro para tener acceso completo.")
else:
    print("No tienes la edad suficiente para acceder al sitio web.")
```

### Ejemplo 3: Determinar si un estudiante aprueba, reprueba o está en recuperación basado en su nota

```python
# Determinar si un estudiante aprueba, reprueba o está en recuperación basado en su nota
nota = 68

if nota >= 60:
    if nota >= 70:
        print("El estudiante aprueba.")
    else:
        print("El estudiante está en recuperación.")
else:
    print("El estudiante reprueba.")
```

---
### 💡¿Sabias que?...

Introducido en Python 3.8, el operador de asignación "walrus" (:=) permite asignar valores dentro de expresiones, incluidas las condiciones en sentencias como if y while. Esto facilita escribir código más compacto y legible, eliminando la necesidad de líneas adicionales para asignaciones previas a la evaluación de condiciones.

Por ejemplo, antes de Python 3.8:

```python
input_text = input("Por favor, introduce algo: ")
if input_text:
    print("Gracias por introducir algo.")
```

Con el operador walrus:

```python
if (input_text := input("Por favor, introduce algo: ")):
    print("Gracias por introducir algo.")
```

El uso del operador walrus no solo reduce la cantidad de código, sino que también permite patrones de programación más eficientes y claros, especialmente en bucles o en cualquier situación donde necesites asignar y verificar un valor al mismo tiempo.

---

⬅️ [`Anterior`](../Readme.md) | ➡️ [`Siguiente`](../Ejemplo-02/Readme.md)