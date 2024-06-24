🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 05**](../Readme.md) ➡️ / ⭕ `Círculo de estudio`

## 🎯 Objetivo

Implementar los conceptos básicos de Python, así como ciclos, condiciones y funciones en un mini proyecto, con el objetivo de aclarar y comprender los temas vistos en sesiones anteriores 1 a 4.

Esta sección es específicamente para preguntas y respuestas de los temas vistos en las sesiones previas, así como el avance de los proyectos.


---

## 🚀 Introducción

El experto o experta explicará brevemente los temas vistos en las sesiones anteriores, aplicados a un proyecto de ejemplo. Posteriormente, se abrirá un espacio para preguntas y respuestas, así como para compartir los avances de los proyectos de los estudiantes.

---


### 🛒 Proyecto: sistema de gestión de inventario para una tienda

#### 🎯 Objetivo del Proyecto:
Desarrollar un sistema de gestión de inventario para una tienda utilizando Python. Este sistema permitirá al usuario agregar, actualizar y eliminar productos del inventario, así como consultar la información del inventario utilizando diversas estructuras de datos y técnicas de programación.

---

### 📚 Módulo 1: Fundamentos de programación

#### 📝 1.1 Variables y tipos de datos
- **Objetivo**: Definir y utilizar variables de diferentes tipos (enteros, flotantes, cadenas, booleanos).
- **Actividad**: Crear variables para almacenar la información básica de un producto (nombre, precio, cantidad, categoría).

    ```python
    nombre_producto = "Laptop"
    precio_producto = 1200.50
    cantidad_producto = 10
    categoria_producto = "Electrónica"
    ```

#### ➕ 1.2 Operadores en python
- **Objetivo**: Implementar operadores aritméticos, de comparación y lógicos para realizar operaciones con datos.
- **Actividad**: Calcular el valor total del inventario y determinar si hay suficiente stock.

    ```python
    valor_total = precio_producto * cantidad_producto
    hay_stock = cantidad_producto > 0
    ```

#### 🗣️ 1.3 Interpolación de strings y lectura por teclado
- **Objetivo**: Utilizar la interpolación de strings, para generar mensajes y leer datos ingresados por el usuario.
- **Actividad**: Pedir al usuario que ingrese la información de un nuevo producto y mostrar un mensaje de confirmación.

    ```python
    nombre_producto = input("Ingrese el nombre del producto: ")
    precio_producto = float(input("Ingrese el precio del producto: "))
    cantidad_producto = int(input("Ingrese la cantidad del producto: "))
    categoria_producto = input("Ingrese la categoría del producto: ")

    print(f"Producto agregado: {nombre_producto}, Precio: {precio_producto}, Cantidad: {cantidad_producto}, Categoría: {categoria_producto}")
    ```

---

### 🔄 Módulo 2: Control de flujo

#### 🔀 2.1 Sentencia if
- **Objetivo**: Implementar la sentencia if para tomar decisiones en el código.
- **Actividad**: Verificar si un producto está en stock y mostrar un mensaje adecuado.

    ```python
    if cantidad_producto > 0:
        print("El producto está en stock.")
    else:
        print("El producto no está en stock.")
    ```

#### 🔁 2.2 Ciclo for
- **Objetivo**: Implementar el ciclo for para iterar sobre una lista de productos.
- **Actividad**: Iterar sobre una lista de productos y mostrar sus nombres.

    ```python
    productos = ["Laptop", "Mouse", "Teclado"]
    for producto in productos:
        print(producto) # Mostrar el nombre del producto
    ```

#### 🔍 2.3 Sentencia match
- **Objetivo**: Implementar la sentencia match (Python 3.10+) para manejar múltiples condiciones.
- **Actividad**: Determinar la categoría de un producto y mostrar un mensaje correspondiente.

    ```python
    match categoria_producto:
        case "Electrónica":
            print("El producto es de la categoría Electrónica.")
        case "Ropa":
            print("El producto es de la categoría Ropa.")
        case _:
            print("Categoría desconocida.")
    ```

#### 🔄 2.4 Ciclo while
- **Objetivo**: Implementar el ciclo while para realizar iteraciones basadas en una condición.
- **Actividad**: Permitir al usuario continuar agregando productos hasta que decida detenerse.

    ```python
    continuar = True
    while continuar:
        nombre_producto = input("Ingrese el nombre del producto: ")
        # (lectura de otros datos del producto)
        continuar = input("¿Desea agregar otro producto? (s/n): ") == 's'
    ```

---

### 📋 Módulo 3: Estructuras de datos

#### 📄 3.1 Listas y sus métodos
- **Objetivo**: Implementar listas y sus métodos para almacenar y manipular datos.
- **Actividad**: Crear una lista de productos y agregar nuevos a la lista.

    ```python
    productos = ["Laptop", "Mouse", "Teclado"]
    productos.append("Monitor")
    print(productos) # Mostrar la lista de productos
    ```

#### 📚 3.2 Tuplas y sus métodos
- **Objetivo**: Implementar tuplas para almacenar datos que no deben cambiar.
- **Actividad**: Crear una tupla con la información de un producto.

    ```python
    producto = ("Laptop", 1200.50, 10, "Electrónica")
    print(producto) # Mostrar la información del producto
    ```

#### 🔢 3.3 Conjuntos y sus métodos
- **Objetivo**: Implementar conjuntos para almacenar colecciones de elementos únicos.
- **Actividad**: Crear un conjunto de categorías de productos.

    ```python
    categorias = {"Electrónica", "Ropa", "Hogar"}
    categorias.add("Deportes")
    print(categorias) # Mostrar las categorías disponibles
    ```

#### 🔑 3.4 Diccionarios y sus métodos
- **Objetivo**: Implementar diccionarios para almacenar datos en pares clave-valor.
- **Actividad**: Crear un diccionario para almacenar la información de varios productos.

    ```python
    inventario = {
        "Laptop": {"precio": 1200.50, "cantidad": 10, "categoría": "Electrónica"},
        "Mouse": {"precio": 20.00, "cantidad": 50, "categoría": "Electrónica"}
    }
    print(inventario) # Mostrar el inventario completo
    ```

---

### 🛠️ Módulo 4: Funciones y programación funcional

#### 🔧 4.1 Definición de funciones
- **Objetivo**: Definir y utilizar funciones para organizar el código.
- **Actividad**: Crear una función para agregar un nuevo producto al inventario.

    ```python
    def agregar_producto(inventario, nombre, precio, cantidad, categoria):
        inventario[nombre] = {"precio": precio, "cantidad": cantidad, "categoría": categoria}
        return inventario
    ```

#### ✏️ 4.2 Funciones lambda
- **Objetivo**: Implementar funciones lambda para crear funciones pequeñas y anónimas.
- **Actividad**: Crear una función lambda para calcular el impuesto sobre el precio de un producto.

    ```python
    calcular_impuesto = lambda precio: precio * 0.16
    print(calcular_impuesto(100))
    ```

#### ❗ 4.3 Control de excepciones
- **Objetivo**: Manejar errores y excepciones en el código.
- **Actividad**: Manejar posibles errores al ingresar datos de un producto.

    ```python
    try:
        precio_producto = float(input("Ingrese el precio del producto: "))
    except ValueError:
        print("Por favor, ingrese un número válido para el precio.")
    ```

#### 🔀 4.4 Map, filter y reduce
- **Objetivo**: Implementar las funciones map, filter y reduce para manipular listas y otros iterables.
- **Actividad**: Calcular el precio total de todos los productos en el inventario.

    ```python
    from functools import reduce

    precios = [1200.50, 20.00, 50.00]
    total = reduce(lambda x, y: x + y, precios)
    print(total)
    ```

---

<!-- Conclusion sobre el mini proyecto-->
## 🤔Conclusiones

En esta sección, se ha aplicado los conceptos básicos de Python, en diferentes situaciones y escenarios, con el objetivo de reforzar y comprender los temas vistos en las sesiones anteriores. A través de un mini proyecto de un sistema de gestión de inventario.

En base a tu proyecto, genera un resumen de como aplicarias los temas vistos hasta el momento.

---

🏆 Nos vemos en la siguiente sesión, ¡mucho éxito!.

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Ejemplo-06/Readme.md) ➡️
