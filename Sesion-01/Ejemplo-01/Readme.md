🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 01**](../Readme.md) ➡️ / 📝 `Ejemplo 01: Variables`

## 🎯 Objetivo

Aplicar los principios básicos y convenciones para establecer una variable en Python.

## 🚀 Comencemos

### Uso de variables y buenas prácticas de nomenclatura

**Definición de variables:**

Una variable es un nombre que se refiere a un objeto que reside en la memoria. Las variables se utilizan para almacenar datos, manipular valores y facilitar la legibilidad y mantenimiento del código.

**Declaración de variables:**

Crear o declarar variables es sencillo, no necesitas especificar un tipo de dato. Python utiliza tipado dinámico, lo que significa que el tipo de una variable se determina automáticamente cuando se le asigna un valor.

```python
# Ejemplo de declaración de variables
numero = 10
mensaje = "Hola, Python!"
print(numero)  # Salida: 10
print(mensaje)  # Salida: Hola, Python!
```

**Buenas prácticas para nombrar variables:**

1. **Deben ser claras y descriptivas:**
   Las variables deben tener nombres descriptivos para hacer el código más entendible. Por ejemplo, `edad` es mejor que `e`, y `nombre_completo` mejor que `nc`.

2. **Uso de `snake_case`:**
   Python favorece el uso de `snake_case` para nombrar variables. Esto significa escribir nombres en minúsculas con palabras separadas por guiones bajos.
   
   ```python
   # Buen ejemplo de snake_case
   contador_de_usuarios = 50
   velocidad_maxima = 120
   salario_mensual = 5000
   interes_anual = 0.05
   ```
Este tipo de nomenclatura lo usaremos en el curso.

3. **Evitar nombres confusos:**
   No uses nombres que ya tengan un significado importante en Python, como `list` o `str`.

4. **Consistencia:**
   Mantén un estilo consistente a lo largo de todo tu código. Si comienzas usando `snake_case`, sigue usándolo en todo el proyecto.

**Ejemplos de nombres de variables correctos e incorrectos:**

```python
# Correctos
altura_del_edificio = 100
temperatura_actual = 22.5

# Incorrectos
alturaDelEdificio = 100  # camelCase, no recomendado en Python
Temp = 22.5              # ambiguo y empieza con mayúscula
int = 7                  # utiliza el nombre de un tipo de dato incorporado
```

Existen varias convenciones de nomenclatura recomendadas y ampliamente aceptadas que ayudan a mantener el código legible, consistente y en línea con las expectativas de la comunidad. Por ejemplo algunas de las convenciones más populares según la guía de estilo PEP 8:

### 1. **Variables**
   - **snake_case**: Los nombres de las variables deben ser en minúsculas con palabras separadas por guiones bajos. Por ejemplo: `mi_variable`.

### 2. **Funciones y métodos**
   - **snake_case**: Al igual que las variables, los nombres de funciones y métodos deben seguir el formato de minúsculas con guiones bajos. Ejemplo: `calcular_total()`.

### 3. **Clases**
   - **CamelCase**: Los nombres de las clases deben iniciar con mayúsculas y no deben tener guiones bajos entre palabras. Ejemplo: `MiClase`.

### 4. **Constantes**
   - **ALL_CAPS**: Las constantes se nombran con todas las letras en mayúsculas y palabras separadas por guiones bajos. Ejemplo: `MAX_ITERACIONES`.


Es importante adherirse a esas normas para mantener la coherencia del código, con el fin de facilitar la lectura y el mantenimiento del mismo, así como la colaboración con otros desarrolladores.

---

### 💡¿Sabias que?...

Python ejecuta el código de arriba hacia abajo, por lo que si intentas usar una variable que no ha sido declarada, Python lanzará un error.

```python
# Intentar usar una variable no declarada
print(mensaje)  # Error: NameError: name 'mensaje' is not defined
```

---

⬅️ [`Anterior`](../Readme.md) | ➡️ [`Siguiente`](../Ejemplo-02/Readme.md)