🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 02**](../Readme.md) ➡️ / 📝 `Ejemplo 01: Sentencia If`

## 🎯 Objetivo

Aplicar los principios básicos sobre el control del flujo de un programa, usando la sentencia IF.

## 🚀 Comencemos

La sentencia if en programación se utiliza para ejecutar un bloque de código solo si se cumple una condición específica. Es una forma de tomar decisiones dentro de un programa basado en condiciones.

`Nota:` La tabulación o indentación es crucial en Python, ya que se utiliza para definir bloques de código. Es decir, un espacio en blanco al principio de una línea de código, generalmente equivalente a 4 espacios o un tabulador, indica que el código pertenece a un bloque específico.

Ejemplo:

```python
if condición:
    # Bloque de código
    # Todo el código dentro de este bloque pertenece a la sentencia if.
```

## Sentencia `if`

Esta sentencia es como un guardián que decide si un bloque de código se ejecuta o no en tu programa. Funciona de manera muy sencilla:

- Primero, revisa si una condición específica es `verdadera`.
- Si la condición es `verdadera`, entonces se ejecuta el código que sigue inmediatamente después de `if`.
- Si la condición es `falsa`, ese bloque de código se salta y no se ejecuta nada de lo que está dentro.

Piensa en `if` como un interruptor que activa ciertas partes de tu programa solo cuando las condiciones son las adecuadas. Si las condiciones no se cumplen, simplemente sigue adelante sin activar ese bloque de código.

### Sintaxis

```python
if condición:
    # Bloque de código a ejecutar si la condición es verdadera
```

### Ejemplo

```python
# Ejemplo de uso de la sentencia if
edad = 20

# Verificar si la persona es mayor de edad
if edad >= 18:
    print("Eres mayor de edad.")
```

## Sentencia `if-else`

La sentencia `if-else` te ayuda a decidir qué camino tomar en tu programa dependiendo de si una condición es verdadera o no, por ejemplo:

1. **if**: Primero se verifica una condición. Si esta condición es `verdadera`, se ejecuta el bloque de código justo después de `if`.
2. **else**: Si la condición de `if` es `falsa`, entonces el programa salta al código que está después de `else`.

Piensa en esto como, cual de los dos caminos tomar en una bifurcación, dependiendo de la cantidad de combustible que tengas en tu auto, y la distancia que debes recorrer.

### Sintaxis

```python
if condición:
    # Bloque de código a ejecutar si la condición es verdadera
else:
    # Bloque de código a ejecutar si la condición es falsa
```

### Ejemplo

```python
# Ejemplo de uso de la sentencia if-else
edad = 16

# Verificar si la persona es mayor o menor de edad
if edad >= 18:
    print("Eres mayor de edad.")
else:
    print("Eres menor de edad.")
```

## Sentencia `if-elif-else`


La estructura `if-elif-else` te ayuda a manejar decisiones múltiples en tus programas. De esta manera: 

1. **if**: Comienza con una condición inicial. Si esta es verdadera, se ejecuta el bloque de código que le sigue y se ignoran las demás condiciones.
2. **elif**: Significa "else if", y se usa para probar condiciones adicionales si la condición del `if` es falsa. Puedes tener tantos `elif` como necesites, y se verificarán en orden hasta que uno sea verdadero.
3. **else**: Es el último recurso. Si ninguna de las condiciones anteriores es verdadera, entonces el código dentro de `else` se ejecuta.

### Sintaxis

```python
if condición1:
    # Bloque de código a ejecutar si la condición1 es verdadera
elif condición2:
    # Bloque de código a ejecutar si la condición2 es verdadera
else:
    # Bloque de código a ejecutar si ninguna condición anterior es verdadera
```

### Ejemplo

```python
# Ejemplo de uso de la sentencia if-elif-else
nota = 85

# Determinar la calificación basada en la nota
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

### Ejemplo

```python
# Ejemplo de uso de sentencias if anidadas
edad = 20
tiene_identificación = True

# Verificar si la persona puede entrar a un club nocturno
if edad >= 18:
    if tiene_identificación:
        print("Puedes entrar al club.")
    else:
        print("Necesitas una identificación para entrar al club.")
else:
    print("No puedes entrar al club porque eres menor de edad.")
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