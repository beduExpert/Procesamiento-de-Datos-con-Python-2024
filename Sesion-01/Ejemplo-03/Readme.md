🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 01**](../Readme.md) ➡️ / 📝 `Ejemplo 03: Interpolación de Strings y lectura por teclado`

## 🎯 **Objetivo**

Aplicar la interpolación de strings, así como la captura de datos por consola del usuario para crear interfaces interactivas en Python.

---

## 🚀 **Comencemos**

En el ambiente de programación, la interacción con el usuario es una parte esencial de la creación de aplicaciones. Python proporciona herramientas para facilitar la creación de aplicaciones interactivas, como la interpolación de strings y la lectura por teclado, un ejemplo podría ser un menú interactivo en consola que permita al usuario seleccionar una opción y realizar una acción.

---

## 🔠 **Interpolación de strings**

El formateo de cadenas de caracteres o strings es una técnica común en la programación con el fin de presentar datos de manera legible, al usuario. Python ofrece varias formas de interpolación de strings, cada una con sus propias ventajas y desventajas.

### 📝 **Método de formato `%`**

Este es uno de los métodos más antiguos en Python, similar al estilo de formateo de strings en C.

```python
nombre = "Alice"
print("Hola, %s!" % nombre)
```

### 📝 **Método `str.format()`**

Introducido en Python 2.6, este método es más versátil y legible que el formateo con `%`.

```python
nombre = "Bob"
edad = 25
print("Hola, {}. Tienes {} años.".format(nombre, edad))
```

### 📝 **F-Strings (Literal string interpolation)**

Introducido en Python 3.6, los f-strings ofrecen una manera más legible y eficiente de hacer interpolación de strings, así mismo es considerada la forma más moderna de hacer interpolación de strings.

```python
nombre = "Carol"
edad = 30
print(f"Hola, {nombre}. Tienes {edad} años.")
```

---

## ⌨️ **Lectura por teclado**

La lectura por teclado permite a los usuarios interactuar con el programa durante su ejecución. Python utiliza la función `input()` para capturar la entrada del usuario.

### 📝 **Ejemplo básico de `input()`**

```python
nombre = input("Introduce tu nombre: ")
print(f"¡Hola, {nombre}!")
```

### 🔄 **Convertir tipos de datos**

A menudo necesitas convertir la entrada del usuario a un tipo de dato específico, como un entero o un flotante, considera que al leer datos por teclado, estos se almacenan como cadenas de texto, por lo que será necesario convertirlos a un tipo de dato específico. A este proceso se le conoce como *casting*.

```python
edad = input("Introduce tu edad: ")
edad = int(edad)  # Convierte la entrada a entero
print(f"Tienes {edad} años.")

# Otra forma de hacerlo en una sola línea
edad = int(input("Introduce tu edad: "))
print(f"Tienes {edad} años.")
```

### 📝 **Lectura de múltiples valores**

Puedes leer múltiples valores en una sola línea separándolos por espacios.

```python
nombre, edad = input("Introduce tu nombre y edad: ").split()
print(f"¡Hola, {nombre}! Tienes {edad} años.")
```

### 🧩 **Ejemplo complejo**

Combina la lectura por teclado con interpolación de strings para una aplicación práctica, como un cuestionario simple.

```python
nombre = input("Introduce tu nombre: ")
hobby = input("¿Cuál es tu hobby favorito? ")
print(f"¡Hola, {nombre}! Veo que te gusta {hobby}.")
```

---

### 💡 **¿Sabías que?...**

El formateo de texto es una técnica común en la programación para presentar datos de manera legible al usuario.

Algunos ejemplos de formateo de texto son:

```python
# 9 dígitos: 4 enteros, 1 punto y 4 decimales
print(f"{3.1415926:09.4f}") # Salida: 0003.1416
print(f"{153.21:09.4f}")   # Salida: 0153.2100
print(f"*{'Python':^10}*") # Salida: *  Python  *
```

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Reto-03/Readme.md)➡️