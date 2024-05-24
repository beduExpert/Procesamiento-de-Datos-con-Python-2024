🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 01**](../Readme.md) ➡️ / 📝 `Ejemplo 01: Variables y Tipos de Datos`

## 🎯 Objetivo

Entender y aplicar los principios básicos para establecer variables y tipos de datos en Python, asegurando buenas prácticas de nomenclatura y una comprensión profunda de las estructuras de datos fundamentales.

## 🚀 Comencemos

### Uso de variables y buenas prácticas de nomenclatura

**Definición y declaración de variables:**

Una variable es un nombre asignado a un objeto en memoria, utilizado para almacenar datos y facilitar la legibilidad y mantenimiento del código. En Python, declarar variables es sencillo gracias al tipado dinámico, que determina automáticamente el tipo de la variable al asignarle un valor.

```python
# Ejemplo de declaración de variables
numero = 10
mensaje = "Hola, Python!"
print(numero)  # Salida: 10
print(mensaje)  # Salida: Hola, Python!
```

**Buenas prácticas para nombrar variables:**

- **Claridad y descriptividad**: Utilizar nombres claros como `edad` en lugar de `e`.
- **snake_case**: Es el estilo preferido en Python, e.g., `contador_de_usuarios`.
- **Evitar nombres reservados**: Tales como `list` o `str`.
- **Consistencia**: Mantener un estilo uniforme, como `snake_case`, a lo largo del código.

### Tipos de datos en Python

Python ofrece varios tipos de datos, cada uno adecuado para diferentes necesidades:

1. **Números**: `int`, `float`, y `complex`.
2. **Cadenas de caracteres (Strings)**: `str`, ejemplos incluyen "Hola" y "Python es divertido".
3. **Booleanos**: `bool`, que solo pueden ser `True` o `False`.


<!-- Ejemplos -->

### 🕵 Ejemplos:

```python
nombre = "Ana"
saludo = "Hola, " + nombre  # Concatenación de strings
print(saludo)  # Salida: Hola, Ana

a = 5
es_mayor = a > 10
print(es_mayor)  # Salida: False
```


```python
# Ejemplo de tipos de datos
numero = 10
flotante = 10.5
complejo = 1 + 2j
cadena = "Hola, Python!"
booleano = True

print(type(numero))  # Salida: <class 'int'>
print(type(flotante))  # Salida: <class 'float'>
print(type(complejo))  # Salida: <class 'complex'>
print(type(cadena))  # Salida: <class 'str'>
print(type(booleano))  # Salida: <class 'bool'>
```

---

### 💡 **¿Sabias que?...**

- **Python ejecuta el código de arriba hacia abajo**, lo que significa que usar una variable antes de declararla provocará un error.
- **La función `type()`** nos permite conocer el tipo de dato de una variable, por ejemplo, `type(numero)` devolverá `<class 'int'>`.

---

⬅️ [`Anterior`](../Readme.md) | [`Siguiente`](../Ejemplo-02/Readme.md)➡️
