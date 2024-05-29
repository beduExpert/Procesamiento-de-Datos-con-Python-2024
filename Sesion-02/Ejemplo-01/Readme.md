🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 02**](../Readme.md) ➡️ / 📝 `Ejemplo 01: Sentencia If`

## 🎯 Objetivo

Aplicar los principios básicos sobre el control del flujo de un programa, usando la sentencia if.

---

## 🚀 Comencemos

Las sentencias condicionales en Python permiten ejecutar diferentes bloques de código según se cumplan o no ciertas condiciones. Las sentencias más comunes son `if`, `if-else`, y `if` anidados.

---

## 📝 Sentencia `if`

La sentencia `if` se utiliza para ejecutar un bloque de código solo si una condición es verdadera.

### 📌 Sintaxis

```python
if condición:
    # Bloque de código a ejecutar si la condición es verdadera
```

### Ejemplos

```python
# Verificar si un número es positivo
numero = 10
if numero > 0:
    print("El número es positivo.")

# Verificar si una persona es mayor de edad
edad = 20
if edad >= 18:
    print("Eres mayor de edad.")

# Verificar si una cadena no está vacía
cadena = "Hola, mundo"
if cadena:
    print("La cadena no está vacía.")

# Verificar si un número es par
numero = 4
if numero % 2 == 0:
    print("El número es par.")

# Verificar si una variable tiene un valor específico
color = "rojo"
if color == "rojo":
    print("El color es rojo.")
```

---

## 📝 Sentencia `if-else`

La sentencia `if-else` permite ejecutar un bloque de código si la condición es verdadera y otro bloque si la condición es falsa.

### 📌 Sintaxis

```python
if condición:
    # Bloque de código a ejecutar si la condición es verdadera
else:
    # Bloque de código a ejecutar si la condición es falsa
```

### Ejemplos

```python
# Verificar si un número es positivo o negativo
numero = -5
if numero >= 0:
    print("El número es positivo.")
else:
    print("El número es negativo.")

# Verificar si una persona es mayor o menor de edad
edad = 16
if edad >= 18:
    print("Eres mayor de edad.")
else:
    print("Eres menor de edad.")

# Verificar si una cadena está vacía o no
cadena = ""
if cadena:
    print("La cadena no está vacía.")
else:
    print("La cadena está vacía.")

# Verificar si un número es par o impar
numero = 7
if numero % 2 == 0:
    print("El número es par.")
else:
    print("El número es impar.")

# Verificar si una persona tiene permiso para votar
edad = 17
ciudadano = True
if edad >= 18 and ciudadano:
    print("Tienes permiso para votar.")
else:
    print("No tienes permiso para votar.")
```

---

## 📝 Sentencia `if-elif-else`

La sentencia `if-elif-else` permite manejar múltiples condiciones. Se pueden agregar tantos bloques `elif` como sean necesarios.

### 📌 Sintaxis

```python
if condición1:
    # Bloque de código a ejecutar si la condición1 es verdadera
elif condición2:
    # Bloque de código a ejecutar si la condición2 es verdadera
else:
    # Bloque de código a ejecutar si ninguna condición anterior es verdadera
```

### Ejemplos

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

---

## 📝 Sentencias `if` anidadas

Las sentencias `if` anidadas se utilizan cuando se necesita evaluar una condición dentro de otra condición.

### 📌 Sintaxis

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

### Ejemplos

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

### 💡 **¿Sabías que?...**

En Python, puedes usar sentencias `if-else` en una sola línea para simplificar el código en situaciones donde las acciones a realizar son cortas. Este patrón se conoce como "Ternary Conditional Operator" o "Operador Ternario".

#### 📌 Sintaxis

```python
variable = valor_if_true if condicion else valor_if_false
```

Esto es útil para asignar valores a una variable basada en una condición de manera compacta.

#### Ejemplos

```python
edad = 18
mensaje = "Eres mayor de edad." if edad >= 18 else "Eres menor de edad."
print(mensaje)  # Salida: Eres mayor de edad.

# Otro ejemplo
descuento = 20 if es_vip else 5
print(f"El descuento aplicado es: {descuento}%")
```

Este operador ternario puede mejorar la legibilidad del código cuando se trata de condiciones simples, evitando la necesidad de múltiples líneas y haciendo el código más conciso.


---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Ejemplo-02/Readme.md) ➡️