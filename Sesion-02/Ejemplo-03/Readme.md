🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 02**](../Readme.md) ➡️ / 📝 `Ejemplo 03: Sentencia Match.`

## 🎯 Objetivo

Aplicar los principios básicos sobre el control del flujo de un programa, usando la sentencia match.

## 🚀 Comencemos

En Python, la sentencia match-case se utiliza como una estructura de control que permite realizar comparaciones de patrones más sofisticadas y legibles en comparación con las secuencias típicas de instrucciones if-elif-else. Este fue introducido en Python 3.10 como parte de lo que comúnmente se conoce como "pattern matching", inspirado en características similares de otros lenguajes de programación como Java, C#, Rust y Kotlin.


### Sintaxis

```python
match objeto:
    case patrón1:
        # acciones si el objeto coincide con el patrón1
    case patrón2:
        # acciones si el objeto coincide con el patrón2
    case _:
        # acciones si el objeto no coincide con ninguno de los patrones anteriores

```


### Ejemplo 1: Manejo de Menús
Supongamos que tienes un menú de opciones y quieres ejecutar diferentes funciones dependiendo de la elección del usuario.

```python
opcion = input("Elige una opción (1, 2, 3): ")

match opcion:
    case '1':
        print("Has elegido la opción 1.")
    case '2':
        print("Has elegido la opción 2.")
    case '3':
        print("Has elegido la opción 3.")
    case _:
        print("Opción no válida.")
```

### Ejemplo 2: Clasificación de Tipos de Datos
Puedes usar `match` para clasificar diferentes tipos de datos ingresados por un usuario.

```python
dato = input("Ingresa un dato: ")

match dato:
    case dato if dato.isdigit():
        print("Es un número.")
    case dato if dato.isalpha():
        print("Es una palabra.")
    case _:
        print("Es una mezcla de números y letras o caracteres especiales.")
```

### Ejemplo 3: Respuestas Basadas en Estado
En este ejemplo, `match` se usa para proporcionar una respuesta basada en el estado de un objeto, como el estado de un pedido.

```python
estado_pedido = "enviado"

match estado_pedido:
    case "pendiente":
        print("Tu pedido está pendiente de envío.")
    case "enviado":
        print("Tu pedido ha sido enviado.")
    case "entregado":
        print("Tu pedido ha sido entregado.")
    case _:
        print("Estado desconocido del pedido.")
```

---
### 💡¿Sabias que?...

La estructura match case en Python ofrece una capacidad avanzada de "pattern matching exhaustivo", lo que permite no solo evaluar valores, sino también descomponer y analizar estructuras de datos complejas como listas, diccionarios y objetos personalizados. A diferencia del switch en otros lenguajes, match case soporta la extracción directa de valores (destructuring), facilitando la manipulación de datos sin necesidad de acceder a ellos por índice.


```python
# Ejemplo de match case con listas
lista = [1, 2, 3]

match lista:
    case [1, 2, 3]:
        print("La lista contiene los números 1, 2 y 3.")
    case [1, 2, _]:
        print("La lista contiene los números 1 y 2.")
    case _:
        print("La lista no coincide con los patrones anteriores.")
```

Esto es solo un vistazo a las posibilidades que ofrece la sentencia match-case en Python. A medida que te familiarices con esta característica, podrás aplicarla en una variedad de situaciones para mejorar la legibilidad y la eficiencia de tu código.

---

⬅️ [`Anterior`](../Readme.md) | [`Siguiente`](../Ejemplo-04/Readme.md) ➡️