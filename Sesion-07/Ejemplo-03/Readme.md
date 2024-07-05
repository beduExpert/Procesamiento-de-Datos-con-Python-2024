🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 07**](../Readme.md) ➡️ / 📝 `Ejemplo 03: Limpieza de Datos`

## 🎯 Objetivo

Comprender y aplicar técnicas de limpieza de datos en Pandas para mejorar la calidad y confiabilidad de los conjuntos de datos. Usando técnicas de conteo y eliminación de valores faltantes para mejorar la calidad de la información, durante la interpretación de los análisis.

---

## 🚀 Introducción

La limpieza de datos es crucial en data science para asegurar que los análisis sean precisos y confiables. Involucra corregir errores, manejar inconsistencias y eliminar y/o sustituir valores atípicos o faltantes. Utilizaremos funciones en Pandas para identificar y tratar con valores `NaN` y `None`, y exploraremos cómo manipular estructuras de datos para una limpieza efectiva.

---

## 📊 **Técnicas de limpieza de datos** 🧹

### 🛠️ **Identificación de valores faltantes**

Los valores faltantes pueden representarse como `NaN` o `None` en Pandas, que representan Not a Number o un valor nulo. Es importante identificar estos valores para determinar su impacto en el análisis y decidir cómo manejarlos.

Utilizando la librería de numpy, podemos generar valores `NaN` en un DataFrame de Pandas.

```python
import pandas as pd
import numpy as np

# Crear un DataFrame para un restaurante con valores faltantes
data = {
    'Orden': [101, 102, 103, 104, 105, 106, 107, 108],
    'Platillo': ['Tacos', 'Burrito', np.nan, 'Enchiladas', 'Tacos', 'Quesadilla', 'Tacos', 'Burrito'],
    'Precio': [10, 12, 11, 13, 10, 9, np.nan, 12],
    'Categoría': ['Comida rápida', 'Comida rápida', 'Comida rápida', 'Comida tradicional', 'Comida rápida', 'Comida rápida', 'Comida rápida', 'Comida rápida'],
    'Mesero': ['Juan', 'Ana', 'Pedro', 'Ana', np.nan, 'Juan', 'Pedro', 'Ana'],
    'Fecha': ['2022-07-01', '2022-07-01', '2022-07-02', np.nan, '2022-07-02', '2022-07-03', '2022-07-03', '2022-07-04']
}

df = pd.DataFrame(data)

# Mostrar el DataFrame, recuerda al no usar print, se muestra de forma más amigable, esto es aplicable para todos los ejemplos.
df.head(10)
```

**Salida:**

```plaintext
    Orden    Platillo  Precio           Categoría Mesero       Fecha
0    101       Tacos    10.0       Comida rápida   Juan  2022-07-01
1    102     Burrito    12.0       Comida rápida    Ana  2022-07-01
2    103         NaN    11.0       Comida rápida  Pedro  2022-07-02
3    104  Enchiladas    13.0  Comida tradicional    Ana         NaN
4    105       Tacos    10.0       Comida rápida    NaN  2022-07-02
```

---

### 🔍 **Identificación y conteo de NaNs**

Aprender a detectar y contar los `NaNs` es importante para evaluar la calidad de los datos y decidir cómo manejarlos. Pandas ofrece funciones como `isna()`, `isnull()`, `notna()` y `notnull()` para identificar valores faltantes.

| Función | Descripción |
| --- | --- |
| `isna()` | Devuelve `True` si el valor es `NaN` |
| `isnull()` | Alias de `isna()` |
| `notna()` | Devuelve `False` si el valor es `NaN` |
| `notnull()` | Alias de `notna()` |

```python
# Contar NaNs en cada columna
nan_por_columna = df.isna().sum()
print(f"NaNs por columna:\n{nan_por_columna}\n")

print("-"*20)

# Contar NaNs en cada fila
nan_por_fila = df.isna().sum(axis=1)
print(f"NaNs por fila:\n{nan_por_fila}")
```

Para establecer el conteo ya sea por renglón o por columna, se puede utilizar el argumento `axis` con el valor `0` para columnas y `1` para renglones.

---

### 🗑️ **Eliminación de Valores Faltantes**

#### 🛡️ **Trabajar con copias para la seguridad de los datos**

Antes de proceder a la eliminación de filas o columnas, es crucial comprender el impacto de modificar directamente el `DataFrame` original. Para evitar cambios no deseados y asegurar la integridad de los datos:

```python
# Crear una copia del DataFrame para manipulaciones seguras
df_clean = df.copy()
print(df_clean.head())
```

> **📝 Nota:** Utilizar `.copy()` es altamente recomendable para probar o validar modificaciones sin alterar los datos originales. Esto es especialmente valioso en entornos de producción o cuando múltiples procesos dependen de una fuente de datos inalterada.

#### 🔄 **Uso de `dropna()` para eliminar datos nulos**

`dropna()` permite eliminar filas o columnas que contienen valores nulos, con opciones para especificar exactamente cómo y dónde aplicar estas eliminaciones.

```plaintext
| Argumento | Descripción                          |
|-----------|--------------------------------------|
| `axis`    | `0` para filas, `1` para columnas    |
| `how`     | `any` para eliminar si hay un `NaN`, `all` para eliminar solo si todos los valores son `NaN` |
```

**Evaluar el impacto antes de eliminar:**
Antes de eliminar valores nulos, considera su impacto en el análisis y la integridad de los datos. Decisiones informadas ayudan a mantener la relevancia y precisión de los resultados analíticos.

```python
# Eliminar filas donde cualquier valor es NaN
df_clean.dropna(axis=0, how='any')

# Eliminar columnas donde cualquier valor es NaN
df_clean.dropna(axis=1, how='any')
```

> **📝 Nota:** Estas operaciones muestran una vista previa de los datos. Para aplicar los cambios de forma permanente, utiliza `inplace=True`.

#### 📋 **Uso avanzado con `subset`**

Controla específicamente qué filas o columnas evaluar para la eliminación, utilizando el argumento `subset` que acepta una lista de nombres de columnas.

```python
# Eliminar filas donde las columnas 'Platillo' o 'Precio' contienen NaN
df_clean.dropna(subset=['Platillo', 'Precio'], axis=0, how='any')

# Eliminar columnas donde las columnas 'Mesero' o 'Fecha' contienen NaN
df_clean.dropna(subset=['Mesero', 'Fecha'], axis=1, how='any')
```

---

### 🛠️ **Limpieza avanzada**

Además de manejar valores faltantes, la limpieza de datos puede incluir la corrección de tipos de datos, manejo de valores atípicos y normalización de formatos.

```python
# Reemplazar NaN en 'Precio' con la mediana
df_clean['Precio'].fillna(value=df_clean['Precio'].median(), inplace=True)

# Reemplazar NaN en 'Platillo' con 'Desconocido'
df_clean['Platillo'].fillna(value='Desconocido', inplace=True)

# Reemplazar NaN en 'Mesero' con 'Desconocido'
df_clean['Mesero'].fillna(value='Desconocido', inplace=True)

# Reemplazar NaN en 'Fecha' con la fecha actual
df_clean['Fecha'].fillna(value=pd.Timestamp.now().date(), inplace=True)

# Mostrar el DataFrame actualizado
df_clean.head()
```

> **📝 Nota:** La función `pd.Timestamp.now().date()` devuelve la fecha actual en formato año-mes-día (YYYY-MM-DD).

---

### 💡 **¿Sabías que...?**

En el sector financiero, la limpieza de datos es crucial para la detección de fraudes. Un estudio de SAS revela que la precisión de los algoritmos de detección puede mejorar hasta un 25% al corregir datos faltantes y atípicos. Por ejemplo, una institución bancaria que implemente técnicas avanzadas como la imputación de valores faltantes y la eliminación de outliers puede reducir falsos positivos, optimizando recursos y mejorando la eficiencia operativa.

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Ejemplo-04/Readme.md) ➡️