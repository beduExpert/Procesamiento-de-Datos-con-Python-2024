🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 04**](../Readme.md) ➡️ / 📝 `Ejemplo 01: Definición de funciones`

## 🎯 Objetivo

Explorar y aplicar los diferentes tipos de declaración de funciones en Python, así como la forma de retornar valores y el uso de argumentos.

---

## 🚀 Introducción

Las funciones en Python nos ayudan a organizar y reutilizar código. Son bloques de código que realizan una tarea específica y pueden ser llamados en cualquier parte del programa después de haberlas declarado. Las funciones se definen con la palabra reservada `def`, seguida del nombre de la función y los parámetros entre paréntesis. 

---

### 🔦 **Sintaxis básica de una función:**

```python
def nombre_funcion(parametro1, parametro2, ...):
    # Cuerpo de la función
    # Código a ejecutar
    return valor
```

### 🛠️ **Estructura de una función:**

1. **Nombre de la función:** Identificador que se utiliza para llamar a la función.
2. **Parámetros:** Son las `variables` que recibe la función al ser llamada, pueden ser opcionales, Ej: `def funcion(texto, fecha):`.
3. **Cuerpo de la función:** Bloque de código que realiza las operaciones necesarias, todo lo que está indentado después de los dos puntos `:`.
4. **Retorno:** Valor que la función devuelve al ser llamada, puede ser opcional.
5. **Llamada a la función:** Ejecución de la función con los argumentos necesarios.
6. **Argumentos:** Son los `valores` que se pasan a la función al ser llamada, Ej: `funcion("Hola", 2024)`, donde `"Hola"` y `2024` son argumentos.

---

### 🔦 **Tipos de funciones:**

#### 1. Funciones sin argumentos
Ideal para acciones simples y mensajes de bienvenida.

```python
def saludo():
    print("¡Hola desde una función sin argumentos!")

# Llamada a la función
saludo() # salida: ¡Hola desde una función sin argumentos!
```

#### 2. Funciones con argumentos fijos
Utilizadas para operaciones que requieren entradas específicas.

```python
def suma(a, b):
    return a + b

# Llamada a la función, pasando los argumentos requeridos.
print(suma(5, 3))  # salida: 8
```

#### 3. Funciones con argumentos variables `*args`
Permiten flexibilidad con un número indefinido de argumentos no nombrados.

```python
def lista_argumentos(*args):
    for arg in args:
        print(arg)

# Llamada a la función con diferentes cantidades de argumentos.
lista_argumentos(1, 2, 3, 4, 5)
```

#### 4. Funciones con argumentos de llave-valor `**kwargs`
Adecuadas para cuando los argumentos pueden ser nombrados.

```python
def lista_kwargs(**kwargs):
    for clave, valor in kwargs.items():
        print(f"{clave}: {valor}")

# Llamada a la función con argumentos llave-valor.
lista_kwargs(nombre="Juan", edad=25, ciudad="CDMX")
```

#### 5. Funciones con argumentos predeterminados
Facilitan la configuración de parámetros con valores por defecto.

```python
def saludo(nombre="Invitado"):
    print(f"¡Hola {nombre}!"

# Llamada a la función sin argumentos.
saludo()  # salida: ¡Hola Invitado!
# Llamada a la función con argumento.
saludo("Mario")  # salida: ¡Hola Mario!
```

---

### 💡 **Sabías que...**

Es importante mencionar que las variables definidas dentro de una función son locales, es decir, que solo existen dentro de la función y no pueden ser accedidas desde fuera de ella, si lo intentamos obtendremos un error.

```python
def funcion():
    variable_local = "Soy una variable local"
    print(variable_local)

funcion() # salida: Soy una variable local
print(variable_local)  # NameError: name 'variable_local' is not defined
```

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Ejemplo-02/Readme.md) ➡️