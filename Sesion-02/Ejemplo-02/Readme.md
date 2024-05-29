🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 02**](../Readme.md) ➡️ / 📝 `Ejemplo 02: Ciclo for`

## 🎯 Objetivo

Aplicar las bases sobre ciclos de repetición finito de acuerdo con conjunto de elementos, y procesar la información, en cada iteración.

## 🚀 Comencemos

Los ciclos de repetición son una estructura de control que permite ejecutar un bloque de código múltiples veces. El ciclo for es un tipo de ciclo que se utiliza para recorrer una secuencia de elementos `finitos`, como una lista, tupla, rango, etc.


### Sintaxis

```python
for elemento in secuencia:
    # Bloque de código a ejecutar para cada elemento en la secuencia
```

<!-- Nota -->
**Nota:** La función `range()` es una función que genera una secuencia de números enteros. Sera utilizada en los ejemplos siguientes.


```python
range(inicio, fin, incremento)
# inicio: Número inicial de la secuencia
# fin: Número final de la secuencia (no incluido)
# incremento: Valor que se suma a cada elemento de la secuencia
```

### Ejemplo 1: Iterar sobre un rango de números

```python
# Iterar sobre un rango de números del 0 al 4
for i in range(5):
    print(i)

# Salida:
# 0
# 1
# 2
# 3
# 4
```

### Ejemplo 2: Iterar sobre un rango de números con un paso específico

```python
# Iterar sobre un rango de números del 0 al 10 con un paso de 2
for i in range(0, 11, 2):
    print(i)

# Salida:
# 0
# 2
# 4
# 6
# 8
# 10
```

### Ejemplo 3: Iterar sobre los caracteres de una cadena

```python
# Iterar sobre cada carácter de una cadena
cadena = "Hola"
for caracter in cadena:
    print(caracter)

# Salida:
# H
# o
# l
# a
```

### Ejemplo 4: Iterar sobre un rango de números en orden inverso

```python
# Iterar sobre un rango de números del 5 al 1 en orden inverso
for i in range(5, 0, -1):
    print(i)

# Salida:
# 5
# 4
# 3
# 2
# 1
```

### Ejemplo 5: Iterar sobre un rango sin usar el elemento individual

```python
# Ejecutar un bloque de código 3 veces sin usar el elemento individual
for _ in range(3):
    print("Hola, mundo")

# Salida:
# Hola, mundo
# Hola, mundo
# Hola, mundo
```

---

<!-- Hablemos sobre brake, continue, pass y else -->

Las palabras clave `break`, `continue`, `pass` y `else` se pueden utilizar dentro de un ciclo for para controlar el flujo de ejecución.

Esto es bastante útil cuando se desea detener la ejecución del ciclo, saltar a la siguiente iteración, o simplemente no hacer nada.

### Ejemplo 1: Usar `break` para detener un ciclo

```python
# Detener un ciclo cuando se encuentra el número 3
for i in range(5):
    if i == 3:
        break
    print(i)

# Salida:
# 0
# 1
# 2
```

### Ejemplo 2: Usar `continue` para saltar a la siguiente iteración

```python
# Saltar a la siguiente iteración cuando se encuentra el número 3
for i in range(5):
    if i == 3:
        continue
    print(i)

# Salida:
# 0
# 1
# 2
# 4
```


### Ejemplo 3: Usar `pass` para no hacer nada

```python
# No hacer nada cuando se encuentra el número 3
for i in range(5):
    if i == 3:
        pass
    print(i)

# Salida:
# 0
# 1
# 2
# 3
# 4
```

### Ejemplo 4: Usar `else` para ejecutar un bloque de código al final del ciclo

```python
# Ejecutar un bloque de código al final del ciclo
for i in range(5):
    print(i)
else:
    print("Fin del ciclo")

# Salida:
# 0
# 1
# 2
# 3
# 4
# Fin del ciclo
```

---
### 💡¿Sabias que?...

La librería `time` en Python proporciona varias funciones relacionadas con el manejo del tiempo y la fecha.

Es muy útil para medir el tiempo de ejecución de un bloque de código, y saber si nuestro programa está tardando demasiado en ejecutarse.

### Ejemplo 1: Medir el tiempo de ejecución de un ciclo

```python
import time

# Medir el tiempo de ejecución de un ciclo
inicio = time.time()

for i in range(1000000):
    pass

fin = time.time()

print(f"Tiempo de ejecución: {fin - inicio} segundos")

# Salida:
# Tiempo de ejecución: 0.03125 segundos
```

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Reto-01/Readme.md) ➡️