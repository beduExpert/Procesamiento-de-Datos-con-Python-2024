🏠 [**Inicio**](../../Readie.md) ➡️ / 📖 [**Sesión 07**](../Readme.md) ➡️ / 📝 `Ejemplo 03: Limpieza de Datos`

## 🎯 Objetivo

Comprender y aplicar técnicas fundamentales de limpieza de datos en Pandas para mejorar la calidad y confiabilidad de los conjuntos de datos. Usando tecnicas de conteo y eliminación de valores faltantes para mejorar la calidad de los datos, durante la interpretación de los análisis.

---

## 🚀 Introducción

La limpieza de datos es crucial en data science para asegurar que los análisis sean precisos y confiables. Involucra corregir errores, manejar inconsistencias y eliminar y/o sustituir valores atípicos o faltantes. Utilizaremos funciones en Pandas para identificar y tratar con valores `NaN` y `None`, y exploraremos cómo manipular estructuras de datos para una limpieza efectiva.

---

## 📊 **Técnicas de limpieza de datos** 🧹

### 🛠️ **Identificación de Valores Faltantes**

Los valores faltantes pueden representarse como `NaN` o `None` en Pandas que representa Not a Number o un valor nulo. Es importante identificar estos valores para determinar su impacto en el análisis y decidir cómo manejarlos.

Utilizando la libreria de numpy, podemos generar valores `NaN` en un DataFrame de Pandas.

```python
import pandas as pd
import numpy as np

# Crear un DataFrame de ejemplo
df = pd.DataFrame({
    'A': [1, np.nan, 3],
    'B': [4, 5, None],
    'C': [7, 8, 9],
    'D': [np.nan, 11, 12],
    'E': [15, 16, 17],
    'F': [18, np.nan, 20],
    'G': [21, 22, 23],
    'H': [np.nan, 25, 26]
})

# Mostrar dónde están los valores faltantes
print(df.isna())
```

### 🛠️ **Identificación y conteo de NaNs**

Aprender a detectar y contar los `NaNs` es importante para evaluar la calidad de los datos y decidir cómo manejarlos. Pandas ofrece funciones como `isna()`, `isnull()`, `notna()` y `notnull()` para identificar valores faltantes.


<!-- Tabla -->
| Función | Descripción |
| --- | --- |
| `isna()` | Devuelve `True` si el valor es `NaN` |
| `isnull()` | Alias de `isna()` |
| `notna()` | Devuelve `False` si el valor es `NaN` |
| `notnull()` | Alias de `notna()` |


```python
# Contar NaNs en cada columna
nan_por_columna = df.isna().sum()
print(nan_por_columna)

# Contar NaNs en cada fila
nan_por_fila = df.isna().sum(axis=1)
print(nan_por_fila)
```

Para establecer el conteo ya sea por renglon o por columna, se puede utilizar el argumento `axis` con el valor `0` para columnas y `1` para renglones.

### 🛠️ **Eliminación de valores faltantes**

Puedes eliminar filas o columnas que contengan valores nullos usando `dropna()`. Las opciones `axis` y `how` permiten especificar cómo y dónde aplicar la eliminación.

<!-- Tabla -->
| Argumento | Descripción |
| --- | --- |
| `axis` | `0` para filas, `1` para columnas |
| `how` | `any` para eliminar si hay al menos un `NaN`, `all` para eliminar si todos los valores son `NaN` |

```python
# Eliminar filas donde cualquier valor es NaN (axis=0)
df.dropna(axis=0, how='any')
```

```python
# Eliminar columnas donde todos los valores son NaN (axis=1)
df.dropna(axis=1, how='all')
```

### 🛠️ **Limpieza avanzada**

Además de manejar valores faltantes, la limpieza de datos puede incluir la corrección de tipos de datos, manejo de valores atípicos y normalización de formatos.

```python
# Convertir tipos de datos para uniformidad, este proceso se conoce como "casting"
df['A'] = df['A'].astype(float)
```

```python
# Reemplazar valores NaN con un valor estándar, como 0
df.fillna(value=0, inplace=True)
```

```python
# Reemplazar valores NaN con la media de la columna
df.fillna(value=df.mean(), inplace=True)
```

Castin y reemplazo de valores `NaN` son técnicas comunes para mejorar la calidad de los datos y facilitar el análisis, especialmente en la preparación de datos para modelos de machine learning.

---

### 💡 **¿Sabías que...?**

Una adecuada limpieza de datos puede reducir significativamente los errores de análisis y mejorar la interpretación de los modelos de machine learning y estadísticas descriptivas. Un conjunto de datos bien preparado es fundamental para lograr insights precisos y confiables.

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Ejemplo-04/Readme.md) ➡️
