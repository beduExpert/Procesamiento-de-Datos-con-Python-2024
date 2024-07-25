### Introducción al Procesamiento de Datos con Python:
#### 1.1. Variables y Tipos de Datos
```python
# Definición de variables con diferentes tipos de datos
titulo_libro = "1984"  # String
año_publicacion = 1949  # Integer
precio = 15.99  # Float
es_disponible = True  # Boolean
```

#### 1.2. Operadores y Expresiones
```python
# Uso de operadores aritméticos y lógicos
precio_descuento = precio * 0.85  # Descuento del 15%
libro_disponible_y_reciente = es_disponible and (año_publicacion > 2000)
```

#### 1.3. Interpolación de Strings y Lectura por Teclado
```python
# Interpolación de strings y entrada de datos por el usuario
autor = input("Ingrese el nombre del autor: ")
mensaje = f"El libro {titulo_libro} fue escrito por {autor}."
print(mensaje)
```

### Estructuras de Control:
#### 2.1. Sentencia if
```python
# Condicional if para verificar disponibilidad
if es_disponible:
    print("El libro está disponible para préstamo.")
else:
    print("El libro no está disponible en este momento.")
```

#### 2.2. Ciclo for
```python
# Ciclo for para imprimir todos los libros de una lista
libros = ["1984", "Animal Farm", "Fahrenheit 451"]
for libro in libros:
    print(libro)
```

#### 2.3. Sentencia match (disponible en Python 3.10 y posteriores)
```python
# Uso de match para clasificar libros por género
genero = "Novela"
match genero:
    case "Novela":
        print("Género de Ficción Narrativa.")
    case "Poesía":
        print("Género Lírico.")
    case _:
        print("Género no clasificado.")
```

#### 2.4. Ciclo while
```python
# Ciclo while para solicitar entrada hasta que sea correcta
numero = 0
while numero <= 0:
    numero = int(input("Ingrese un número positivo: "))
```

### Tipos de Colecciones y sus Métodos:
#### 3.1. Listas y sus Métodos
```python
# Métodos comunes de listas
libros.append("Brave New World")  # Añadir un elemento
libros.insert(0, "The Catcher in the Rye")  # Insertar en una posición específica
print(libros.pop())  # Eliminar y retornar el último elemento
```

#### 3.2. Tuplas y sus Métodos
```python
# Tupla de autores y método count
autores = ("Orwell", "Bradbury", "Huxley")
print(autores.count("Orwell"))  # Contar cuántas veces aparece 'Orwell'
```

#### 3.3. Conjuntos y sus Métodos
```python
# Conjuntos para eliminar duplicados y métodos útiles
generos = {"Novela", "Ciencia Ficción", "Novela"}
generos.add("Poesía")  # Añadir un elemento
print(generos)  # Mostrar el conjunto sin duplicados
```

#### 3.4. Diccionarios y sus Métodos
```python
# Diccionario de libros y uso de métodos
info_libro = {"titulo": "1984", "autor": "Orwell", "año": 1949}
print(info_libro.get("autor"))  # Obtener valor por clave
info_libro.update({"precio": 9.99})  # Actualizar el diccionario añadiendo un par clave-valor
```

### Funciones y Herramientas de Programación Funcional:
#### 4.1. Definición de Funciones
```python
# Definir una función para calcular el total de un pedido de libros
def calcular_total(precio, cantidad):
    return precio * cantidad
print(calcular_total(15.99, 3))
```

#### 4.2. Funciones Lambda
```python
# Función lambda para calcular el IVA de un producto
calcular_iva = lambda precio: precio * 0.16
print(calcular_iva(100))
```

#### 4.3. Control de Excepciones
```python
# Uso de try-except para manejar errores
try:
    resultado = 10 / 0
except ZeroDivisionError:
    print("No se puede dividir por cero.")
```

#### 4.4. Map, Filter y Reduce
```python
from functools import reduce

# Uso de map para aplicar un descuento a todos los precios
precios = [10, 20, 30]
precios_descuento = list(map(lambda p: p * 0.85, precios))

# Uso de filter para filtrar precios mayores a 15
precios_altos = list(filter(lambda p: p > 15, precios))

# Uso de reduce para sumar todos los precios
total_precios = reduce(lambda x, y: x + y, precios)
```