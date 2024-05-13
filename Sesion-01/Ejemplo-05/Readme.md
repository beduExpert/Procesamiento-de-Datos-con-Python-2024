🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 01**](../Readme.md) ➡️ / 📝 `Ejemplo 05: Operadores Logicos`


## 🎯 Objetivo

Implementar operaciones matemáticas, acorde a diferentes operadores lógicos en Python.

## 🚀 Comencemos

Los operadores lógicos juegan un papel importante en la programación al permitir dirigir el flujo de las aplicaciones de manera inteligente y dinámica. Python ofrece tres operadores lógicos: `and`, `or`, y `not`, cada uno con un propósito específico diferente que ayuda a manejar decisiones basadas en múltiples condiciones.


### 📜 Lista de operadores lógicos

- **AND (`and`)**: Devuelve `True` solo si ambas condiciones son verdaderas.
- **OR (`or`)**: Devuelve `True` si al menos una de las condiciones es verdadera.
- **NOT (`not`)**: Invierte el resultado de la condición a la que se aplica.

### 🧠 Ejemplos de operadores lógicos

### Ejemplo de `AND`

Este operador evalúa si todas las condiciones especificadas son verdaderas. Solo devuelve `True` si todas las condiciones son verdaderas.

```python
# Ejemplo de uso del operador AND
a = True
b = False
print(a and b)  # Salida: False porque no ambas condiciones son verdaderas.

c = True
d = True
print(c and d)  # Salida: True porque ambas condiciones son verdaderas.
```

### Ejemplo de `OR`

Este operador evalúa si al menos una de las condiciones es verdadera. Devuelve `True` si al menos una de las condiciones es verdadera.

```python
# Ejemplo de uso del operador OR
a = True
b = False
print(a or b)  # Salida: True porque al menos una de las condiciones es verdadera.

c = False
d = False
print(c or d)  # Salida: False porque ninguna de las condiciones es verdadera.
```

### Ejemplo de `NOT`

Este operador representa un operador unario, es decir que invierte el valor de la condición a la que sea aplicado.

```python
# Ejemplo de uso del operador NOT
a = True
print(not a)  # Salida: False porque invierte el True.

b = False
print(not b)  # Salida: True porque invierte el False.
```

### Combinando Operadores Lógicos

Los operadores lógicos pueden combinarse para formar expresiones más complejas. Esto es útil en situaciones donde necesitas evaluar múltiples condiciones al mismo tiempo.

```python
# Combinando operadores lógicos
a = True
b = False
c = True
print(a and (b or c))  # Salida: True porque (b or c) es True y luego a and True es True.

# Utilizando NOT con AND y OR
print(not (a and b) or c)  # Salida: True porque (a and b) es False, not False es True, y True or c es True.
```

```python
email_verificado = True
telefono_verificado = False
reportado_spammer = True

# Los usuarios pueden enviar si alguno de sus datos está verificado y no han sido reportados como spammers
puede_enviar = (email_verificado or telefono_verificado) and not reportado_spammer
print(f"¿Puede enviar contenido? {puede_enviar}")  # Salida: False
```
---

### 💡¿Sabias que?...

Python permite integrar módulos escritos en otros lenguajes como C y C++, lo que permite a los desarrolladores optimizar partes del código sin sacrificar la velocidad.

---

⬅️ [`Anterior`](../Readme.md) | ➡️ [`Siguiente`](../Ejemplo-06/Readme.md)