[`Procesamiento de datos con Python`](../../README.md) > [`Sesión 01`](../README.md) > `Ejemplo 01: Variables`



## 🎯 Objetivo

Aplicar los principios básicos y convenciones para establecer una variable en Python.

## 📂 Organización de la sesión

¡Claro! Aquí tienes un texto detallado sobre el uso de variables en Python, incluyendo buenas prácticas para nombrarlas y el uso de `snake_case` para el nombramiento:

---

### Uso de Variables en Python y Buenas Prácticas de Nomenclatura

**Definición de Variables:**

En Python, una variable es un nombre que se refiere a un objeto que reside en la memoria. Las variables se utilizan para almacenar datos, manipular valores y facilitar la legibilidad y mantenimiento del código.

**Declaración de Variables:**

Crear o declarar variables en Python es sencillo; no necesitas especificar un tipo de dato. Python utiliza tipado dinámico, lo que significa que el tipo de una variable se determina automáticamente cuando se le asigna un valor.

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



Nombrar correctamente las variables es fundamental para escribir un código limpio y mantenible. Siguiendo estas prácticas recomendadas, facilitarás la comprensión y colaboración en proyectos de Python, especialmente en entornos donde múltiples desarrolladores trabajan sobre el mismo código.



---
[`Anterior`](../Readme.md) | [`Siguiente`](../Ejemplo-02/Readme.md)