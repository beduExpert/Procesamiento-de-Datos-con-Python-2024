[`Procesamiento de datos con Python`](../../Readme.md) > [`Sesión 01`](../Readme.md) > `Ejemplo 01: Variables`


## 🎯 Objetivo

Aplicar los principios básicos y convenciones para establecer una variable en Python.

## 📂 Organización de la sesión



### Uso de Variables en Python y Buenas Prácticas de Nomenclatura

**Definición de Variables:**

En Python, una variable es un nombre que se refiere a un objeto que reside en la memoria. Las variables se utilizan para almacenar datos, manipular valores y facilitar la legibilidad y mantenimiento del código.

**Declaración de Variables:**

Crear o declarar variables en Python es sencillo, no necesitas especificar un tipo de dato. Python utiliza tipado dinámico, lo que significa que el tipo de una variable se determina automáticamente cuando se le asigna un valor.

```python
# Ejemplo de declaración de variables
numero = 10
mensaje = "Hola, Python!"
```

**Buenas Prácticas para Nombrar Variables:**

1. **Claridad y Descriptividad:**
   Las variables deben tener nombres descriptivos para hacer el código más entendible. Por ejemplo, `edad` es mejor que `e`, y `nombre_completo` mejor que `nc`.

2. **Uso de `snake_case`:**
   Python favorece el uso de `snake_case` para nombrar variables. Esto significa escribir nombres en minúsculas con palabras separadas por guiones bajos.
   
   ```python
   # Buen ejemplo de snake_case
   contador_de_usuarios = 50
   velocidad_maxima = 120
   ```
Este tipo de nomenclatura lo usaremos en el curso.

3. **Evitar Nombres Confusos:**
   No uses nombres que ya tengan un significado importante en Python, como `list` o `str`.

4. **Consistencia:**
   Mantén un estilo consistente a lo largo de todo tu código. Si comienzas usando `snake_case`, sigue usándolo en todo el proyecto.

**Ejemplos de Nombres de Variables Correctos e Incorrectos:**

```python
# Correctos
altura_del_edificio = 100
temperatura_actual = 22.5

# Incorrectos
alturaDelEdificio = 100  # camelCase, no recomendado en Python
Temp = 22.5              # ambiguo y empieza con mayúscula
int = 7                  # utiliza el nombre de un tipo de dato incorporado
```

En Python, existen varias convenciones de nomenclatura recomendadas y ampliamente aceptadas que ayudan a mantener el código legible, consistente y en línea con las expectativas de la comunidad. Por ejemplo algunas de las convenciones más populares según la guía de estilo PEP 8:

### 1. **Variables**
   - **snake_case**: Los nombres de las variables deben ser en minúsculas con palabras separadas por guiones bajos. Por ejemplo: `mi_variable`.

### 2. **Funciones y Métodos**
   - **snake_case**: Al igual que las variables, los nombres de funciones y métodos deben seguir el formato de minúsculas con guiones bajos. Ejemplo: `calcular_total()`.

### 3. **Clases**
   - **CamelCase**: Los nombres de las clases deben iniciar con mayúsculas y no deben tener guiones bajos entre palabras. Ejemplo: `MiClase`.

### 4. **Constantes**
   - **ALL_CAPS**: Las constantes se nombran con todas las letras en mayúsculas y palabras separadas por guiones bajos. Ejemplo: `MAX_ITERACIONES`.

### 5. **Módulos**
   - **snake_case o shortlowercase**: Los nombres de los módulos deben ser cortos y generalmente en minúsculas. En algunos casos se utilizan guiones bajos si mejora la legibilidad. Ejemplo: `mi_modulo`.

### 6. **Paquetes**
   - **shortlowercase**: Similar a los módulos, los nombres de los paquetes deben ser en minúsculas sin guiones bajos. Ejemplo: `mipaquete`.

### 7. **Instancias y Excepciones**
   - **CamelCase** para clases de excepciones (siguiendo la convención de nombres de clases).
   - **snake_case** para instancias de objetos y variables, siguiendo la convención de nombres de variables.

### 8. **Parámetros de Métodos y Funciones**
   - **snake_case**: Los nombres de parámetros deben ser en minúsculas y, si constan de varias palabras, separados por guiones bajos.

Es importante adherirse a esas normas para mantener la coherencia del código, con el fin de facilitar la lectura y el mantenimiento del mismo, asi como la colaboración con otros desarrolladores.

---
[`Anterior`](../Readme.md) | [`Siguiente`](../Ejemplo-02/Readme.md)