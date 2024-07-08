🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 08**](../Readme.md) ➡️ / 📝 `Ejemplo 01: Manipulación de tipos de datos y strings`

## 🎯 Objetivo

Explorar y aplicar técnicas de manipulación de tipos de datos y cadenas de texto en pandas, facilitando la transformación y análisis de datos con python.

---

## 🚀 Comencemos

La manipulación de tipos de datos y strings es esencial para asegurar que tus datos estén en el formato correcto para el análisis. Pandas ofrece herramientas poderosas para transformar y manejar datos de manera eficiente.

---

## 🔄 **Manipulación de tipos de datos** 🛠️

### 🎲 **Casting básico con `astype()`**

El casting con `astype()` te permite cambiar el tipo de datos de las columnas en un DataFrame, lo cual es bastante útil para asegurar que los datos sean del tipo correcto para realizar operaciones específicas, de analítica o visualización.

```python
import pandas as pd

# Crear un DataFrame de ejemplo
df = pd.DataFrame({
    'A': ['1', '2', '3', '4'],
    'B': [1.1, 2.2, 3.3, 4.4],
    'C': ['2021-01-01', '2021-02-01', '2021-03-01', '2021-04-01'],
    'D': [1212883200000, 1296518400000, 1327881600000, 1361923200000]
})

# Convertir la columna 'A' a tipo entero
df['A'] = df['A'].astype(int)

# Convertir la columna 'C' a tipo datetime usando pd.to_datetime
df['C'] = pd.to_datetime(df['C'])

# Convertir la columna 'D' a tipo datetime en milisegundos
df = df.astype({'D': 'datetime64[ms]'})

# Mostrar los tipos de datos para verificar las conversiones
df.dtypes

# Salida esperada:
# A             int64
# B           float64
# C    datetime64[ns]
# D    datetime64[ns]
# dtype: object
```

### 🎲 **Casting de tipos numéricos con `to_numeric()`**

Para convertir columnas a tipos numéricos, puedes usar `pd.to_numeric()`, que ofrece más control sobre cómo manejar valores no convertibles, como la capacidad de convertirlos en NaN o ignorarlos.

```python
# Crear un DataFrame de ejemplo
df = pd.DataFrame({
    'A': ['1', '2', '3', '4'],
    'B': ['1.1', '2.2', '3.3', '4.4']
})

# Convertir la columna 'A' a tipo float usando to_numeric
df['A'] = pd.to_numeric(df['A'])

# Mostrar los tipos de datos para verificar las conversiones
df.dtypes
```

### 🚨 **Control de errores en el casting**

Es crucial manejar los posibles errores que puedan surgir durante el proceso de casting. Tanto `pd.to_numeric()` como `pd.to_datetime()` permiten especificar el parámetro `errors` para controlar cómo se manejan los errores, lo cual no está disponible en `astype()`.

```python
# Crear un DataFrame de ejemplo con datos no convertibles
df = pd.DataFrame({
    'A': ['1', '2', 'three', '4'],
    'B': ['1.1', 'two.point.two', '3.3', '4.4']
})

# Intentar convertir la columna 'A' a tipo entero, con manejo de errores
df['A'] = pd.to_numeric(df['A'], errors='coerce')

# Intentar convertir la columna 'B' a tipo float, con manejo de errores
df['B'] = pd.to_numeric(df['B'], errors='coerce')

# Nostrar el dataframe resultante
df.head()
```

| Tipo de Error   | Descripción                                                                 |
|-----------------|-----------------------------------------------------------------------------|
| `errors='raise'`  | Genera una excepción si se encuentra un valor no convertible (comportamiento predeterminado). |
| `errors='coerce'` | Convierte los valores no convertibles en NaN (valores faltantes).           |
| `errors='ignore'` | Deja los valores no convertibles tal como están, sin realizar el casting.   |

---

## 🔤 **Manipulación de cadenas de texto** 🛠️

La manipulación de cadenas de texto puede incluir tareas como cambiar a minúsculas, eliminar espacios, reemplazar caracteres, y más. Aquí hay algunos métodos comunes para trabajar con strings en Pandas.

### 🎲 **Manipulación de strings**

Pandas proporciona una propiedad especial `.str` que te permite acceder a métodos de manipulación de strings, como `lower()`, `upper()`, `strip()`, `replace()`, y `split()`, entre otros. Estos métodos son vectorizados, lo que significa que se aplican a todos los elementos de una columna de manera eficiente.

```python
# Crear un DataFrame de ejemplo
df = pd.DataFrame({
    'Nombres': ['John Doe', 'Jane Smith', 'Alice Johnson'],
    'Emails': ['john.doe@example.com', 'jane.smith@example.com', 'alice.johnson@example.com']
})

# Convertir a minúsculas
df['Nombres'] = df['Nombres'].str.lower()

# Dividir la columna 'Nombres' en dos columnas
df[['Nombre', 'Apellido']] = df['Nombres'].str.split(' ', expand=True)

# Extraer el dominio de los correos electrónicos
df['Dominio'] = df['Emails'].str.split('@').str[1]

print(df)
```

### 📊 **Métodos populares para manipulación de strings**

| Método              | Descripción                                         |
|---------------------|-----------------------------------------------------|
| `str.lower()`       | Convierte todas las cadenas a minúsculas            |
| `str.upper()`       | Convierte todas las cadenas a mayúsculas            |
| `str.strip()`       | Elimina los espacios en blanco al inicio y al final |
| `str.replace(a, b)` | Reemplaza todas las apariciones de `a` por `b`      |
| `str.split(sep)`    | Divide la cadena en una lista utilizando `sep` como separador |

Estos métodos son muy útiles para transformar y limpiar datos textuales en tus DataFrames.

---

### 💡 **¿Sabías que...?**

Pandas proporciona estructuras de datos de alto nivel y herramientas de análisis de datos. Algunas de las características clave de Pandas son:

- **Optimización**: Pandas está construido sobre NumPy, aprovechando algoritmos compilados en C para operaciones vectorizadas rápidas.

- **Gestión de memoria**: Utiliza `BlockManager` para almacenar datos de forma flexible y manejar tipos heterogéneos, a diferencia del almacenamiento contiguo de NumPy.

- **Extensibilidad**: Además del análisis de datos, Pandas se expande con APIs como `GeoPandas` para análisis geoespacial y `Pandas TA` para el trading.

- **Aplicaciones industriales**: Usado en finanzas para análisis cuantitativo, en biotecnología para datos genómicos, y otros campos que gestionan datos complejos.

- **Interoperabilidad con SQL**: Permite la interacción directa con bases de datos SQL, facilitando la carga y manipulación avanzada de datos en `DataFrames`.

NumPy es una librería de Python que proporciona soporte para arreglos y matrices multidimensionales, junto con una colección de funciones matemáticas de alto nivel para operar con estos arreglos.

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Ejemplo-02/Readme.md) ➡️