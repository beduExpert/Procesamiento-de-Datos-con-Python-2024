🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 01**](../Readme.md) ➡️ / 📝 `Ejemplo 03: Operadores aritméticos`

## 🎯 Objetivo

Aplicar los operadores aritméticos en Python para realizar cálculos básicos.

## 🚀 Comencemos

### Operadores Aritméticos en Python

Los operadores aritméticos o arithmetic operators son los más comunes que nos podemos encontrar, y nos permiten realizar operaciones matematicas sencillas, como pueden ser la suma, resta o exponente. A continuación, se muestra en la siguiente tabla algunos ejemplos, donde x=10 y y=3.

| Operador | Nombre         | Ejemplo         |
|----------|----------------|-----------------|
| `+`      | Suma           | `x + y = 13`    |
| `-`      | Resta          | `x - y = 7`     |
| `*`      | Multiplicación | `x * y = 30`    |
| `/`      | División       | `x / y = 3.333` |
| `%`      | Módulo         | `x % y = 1`     |
| `**`     | Exponente      | `x ** y = 1000` |
| `//`     | Cociente       | `x // y = 3`    |

---

### Ejemplos

```python
x = 10; y = 3
print("Operadores aritméticos")
print("x+y =", x+y)   #13
print("x-y =", x-y)   #7
print("x*y =", x*y)   #30
print("x/y =", x/y)   #3.3333333333333335
print("x%y =", x%y)   #1
print("x**y =", x**y) #1000
print("x//y =", x//y) #3
```
---
### Suma (`+`)

Este operador suma los números presentes a la izquierda y derecha del operador. Recalcamos lo de números porque no tendría sentido sumar dos cadenas de texto, sin embargo en Python es posible hacer este tipo de cosas.

```python
print("2" + "2") # 22
print(5 + 3)  # Salida: 8
```
Es posible sumar también dos cadenas de texto, pero la suma no será aritmética, sino que se unirán ambas cadenas en una.

```python
print("Hola" + " " + "Mundo")  # Salida: Hola Mundo
```
---
### Resta (`-`)

Este operador resta los números presentes a la izquierda y derecha del operador. A diferencia el operador + en este caso no podemos restar cadenas o listas.

```python
a = 10
b = 3
resultado = a - b
print("El resultado de 10 - 3 es:", resultado)  # Salida: 7
```

---

### Multiplicación (`*`)

Como también pasaba con el operador + podemos hacer cosas “raras” con *. Por ejemplo, multiplicar una cadena de texto por un número, lo que nos devolverá la cadena de texto repetida tantas veces como el número que hemos multiplicado.

```python
minutos = 5
segundos_por_minuto = 60
total_segundos = minutos * segundos_por_minuto
print("Total de segundos en 5 minutos:", total_segundos)  # Salida: 300
```

---

### División (`/`)

El operador / divide los números presentes a la izquierda y derecha del operador. Un aspecto importante a tener en cuenta es que si se realiza una división cuyo resultado no es entero (es decimal) podríamos tener problemas. En Python 3 esto no supone un problema porque el mismo se encarga de convertir los números y el resultado que se muestra si es decimal.

```python
suma_de_calificaciones = 375
numero_de_estudiantes = 5
promedio_calificaciones = suma_de_calificaciones / numero_de_estudiantes
print("El promedio de calificaciones es:", promedio_calificaciones)  # Salida: 75.0
```

---

### Módulo (`%`)

El operador % realiza la operación módulo entre los números presentes a la izquierda y la derecha. Se trata de calcular el resto de la división entera entre ambos números. Es decir, si dividimos 10 entre 3, el cociente sería 3 y el resto 1. Ese resto es lo que calcula el módulo.

```python
# Obtener el último dígito del número 456
ultimo_digito = 456 % 10
print("El último dígito es:", ultimo_digito)  # Salida: 6
```

```python
# Verificar si 15 es divisible por 3
print(15 % 3 == 0)  # Salida: True
```
---

### Exponenciación (`**`)

El operador ** realiza el exponente del número a la izquierda elevado al número de la derecha.

```python
print(10**3) # 1000
print(2**2)  #4
print(2**10) # 1024
print(2**0)  #1
print(8**45) #35184372088832
```
---

### División Entera (`//`)

Divide el primer número por el segundo y devuelve la parte entera del resultado, descartando cualquier resto.

Por último, el operador // calcula el cociente de la división entre los números que están a su izquierda y derecha. Es decir, si dividimos 8 entre 3, el resultado sería 2.6666666666666665, pero si utilizamos el operador //, el resultado sería 2.

```python
# Calcular cuántas cajas se necesitan para 120 artículos, si cada caja puede contener 25 artículos.
total_articulos = 120
capacidad_caja = 25
cajas_necesarias = total_articulos // capacidad_caja
print("Cajas necesarias:", cajas_necesarias)  # Salida: 4
```
---

### Orden de aplicación

En los ejemplos anteriores simplemente se ha aplicado un operador a dos números sin mezclarlos entre ellos. Pero en la vida real, es muy común que se mezclen varios operadores en una misma linea de codigo. En estos casos, Python sigue un orden de aplicación de los operadores.

El termino PEMDAS es un acrónimo que se utiliza para recordar el orden en el que las operaciones matemáticas deben ser evaluadas.  

- **P**arentheses (Paréntesis)
- **E**xponents (Exponentes)
- **M**ultiplication (Multiplicación)
- **D**ivision (División)
- **A**ddition (Suma)
- **S**ubtraction (Resta)

Este acrónimo nos ayuda a recordar el orden en que Python evalúa las operaciones matemáticas. Por ejemplo, en la expresión `2 + 3 * 4`, Python primero multiplicará `3 * 4` y luego sumará `2` al resultado.

```python
print(10*(5+3)) # Con paréntesis se realiza primero la suma
print(10*5+3)   # Sin paréntesis se realiza primero la multiplicación
print(3*3+2/5+5%4) # Primero se multiplica y divide, después se suma
print(-2**4)       # Primero se hace la potencia, después se aplica el signo negativo
```

---

### 💡¿Sabias que?... 

Existe una funcionalidad adicional en Python que permite generar numeros aleatorios, para ello se debe importar la libreria `random` y utilizar la función `randint` de la siguiente manera:

```python
import random

print(random.randint(1, 10))  # Salida: un número aleatorio entre 1 y 10
```

### Veremos mas sobre esto en futuras sesiones.
---

⬅️ [`Anterior`](../Readme.md) | ➡️ [`Siguiente`](../Ejemplo-04/Readme.md)