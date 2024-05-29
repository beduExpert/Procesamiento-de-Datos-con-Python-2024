🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 01**](../Readme.md) ➡️ / 📝 `Ejemplo 01: Variables y Tipos de Datos`

## 🎯 Objetivo

🔍 Entender y aplicar los principios básicos de declaración de variables y tipos de datos en Python, asegurando buenas prácticas de nomenclatura y una comprensión profunda de las estructuras de datos fundamentales.

---

<!-- ## 🚀 Comencemos -->

### 📌 Variables en Python

<!-- ### 📌 Uso de variables y buenas prácticas de nomenclatura -->

Las variables son objetos en memoria utilizados para almacenar información que puede ser referenciada o manipulada en un programa. En Python, gracias al tipado dinámico, el tipo de la variable se determina automáticamente al asignarle un valor.

**Ejemplo de declaración de variables:**

```python
numero = 10
mensaje = "Hola, Python!"
nombre = "Mario"
edad = 30
altura = 1.75
es_estudiante = False

print(numero)        # Salida: 10
print(mensaje)       # Salida: Hola, Python!
print(nombre)        # Salida: Mario
print(edad)          # Salida: 30
print(altura)        # Salida: 1.75
print(es_estudiante) # Salida: False
```

**🔑 Recomendaciones para nombrar variables:**

- **📝Claridad**: Utilizar nombres explicativos como `edad` en lugar de abreviaturas como `e`.
- **🚫 Evitar nombres genéricos**: Como `x` o `y` a menos que sea necesario.
- **🐍 snake_case**: Es el estilo recomendado en Python, por ejemplo, `contador_de_usuarios`.
- **⚠️ Evitar nombres reservados**: Como `list` o `str`.
- **🔄 Consistencia**: Utilizar un estilo uniforme como `snake_case` a lo largo del código.

---

### 🧩 Tipos de datos en Python

Python ofrece tipos de datos variados para diferentes necesidades:

1. **Números**: `int`, `float`, y `complex`.
2. **Cadenas de caracteres (Strings)**: `str`, ejemplos incluyen "Ana" y "Python es divertido".
3. **Booleanos**: `bool`, que solo pueden ser `True` o `False`.

**Ejemplo de tipos de datos:**

```python
numero = 10
flotante = 10.5
complejo = 1 + 2j
cadena = "Hola, Python!"
booleano = True

print(type(numero))    # Salida: <class 'int'>
print(type(flotante))  # Salida: <class 'float'>
print(type(complejo))  # Salida: <class 'complex'>
print(type(cadena))    # Salida: <class 'str'>
print(type(booleano))  # Salida: <class 'bool'>
```

---

### 💡 **¿Sabías que?...**

- **👆 Python ejecuta el código de arriba hacia abajo**, lo que significa que usar una variable antes de declararla provocará un error.
- **🔍 La función `type()`** nos permite conocer el tipo de dato de una variable, por ejemplo, `type(numero)` devolverá `<class 'int'>`.

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Reto-01/Readme.md)➡️
