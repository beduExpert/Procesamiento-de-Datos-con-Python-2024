🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 07**](../Readme.md) ➡️ / 📝 `Ejemplo 04: Manipulación, reindexado y renombrado de columnas`

## 🎯 Objetivo

Explorar y aplicar técnicas de manipulación, reindexado y renombrado de columnas en dataframes de pandas para estandarizar la información, adaptarla a necesidades analíticas específicas, y optimizar la visualización y comprensión de los datos.

---

## 🚀 Introducción

La manipulación, reindexado y renombrado de columnas son prácticas esenciales en el análisis de datos, necesarias para la preparación y limpieza de la información antes del análisis. Estas técnicas permiten a los analistas ajustar los datos a las especificaciones requeridas para una interpretación rápida y una visualización precisa.

---

### 📊 **Preparación del dataframe**

```python
import pandas as pd
import numpy as np

# Crear un DataFrame con datos y columnas más complejas
df = pd.DataFrame({
    'Nombre Completo': ['Juan Martínez', 'María Gómez', np.nan, 'Ana Torres', 'Sofía Núñez', np.nan, "Lena Marie", np.nan],
    'Edad al Cierre del Año': [28, 34, 19, np.nan, 45, np.nan, 1, np.nan],
    'Ciudad de Residencia Actual': ['Madrid', 'Barcelona', 'Sevilla', 'Valencia', 'Bilbao', np.nan, "Coahuila", np.nan],
    'Ingresos Anuales Estimados': [1200, 1500, 900, 1100, np.nan, np.nan, 1200, np.nan],
    'Área de Vivienda m²': [np.nan, 45, 70, 80, 60, np.nan, 120, np.nan],
    'Año de Construcción': [1990, 1985, np.nan, 2000, 2010, np.nan, np.nan, np.nan],
    'Reseña del Cliente': [np.nan, np.nan, np.nan, np.nan, np.nan, np.nan, np.nan, np.nan]
})

# Convertir nombres de columnas a snake_case
df.columns = df.columns.str.lower().str.replace(' ', '_').str.replace('(', '').str.replace(')', '')

# Mostrar el DataFrame inicial
df.head(10)
```

---

#### 🧹 **Proceso de eliminación de filas y columnas**

En este proceso vamos a retirar del dataframe columnas que no aportan información relevante y filas que contienen valores faltantes. Esto nos permitirá limpiar y estandarizar la información para un análisis más preciso y eficiente.

```python
# Eliminar columnas que no aportan información relevante
df.drop(columns=['área_de_vivienda_m²', 'año_de_construcción', 'reseña_del_cliente'], inplace=True)
df.head(10)
```

```python
# Eliminar filas con valores faltantes
df.dropna(axis=0, how='any', inplace=True)
df.head(10)
```

---

#### 🔄 **Reindexar y renombrar**

Reiniciar el índice del DataFrame y cambiar el nombre de las columnas para mejorar la legibilidad.


```python
# Mostrar el DataFrame antes de reindexar
df.head()
```

```python
# Reindexar el DataFrame
df.reset_index(drop=False, inplace=False)  # Mostrar cómo queda el índice sin eliminar el índice anterior
```

```python
# Aplicamos el reindexado definitivo
df.reset_index(drop=True, inplace=True) # drop=True elimina la columna de índices anteriores, inplace=True modifica el DataFrame original
df.head()
```

```python
# Renombrar columnas
columnas = {
    'nombre_completo': 'nombre',
    'edad_al_cierre_del_año': 'edad',
    'ciudad_de_residencia_actual': 'ciudad',
    'ingresos_anuales_estimados': 'ingresos'
}

df.rename(columns=columnas, inplace=True)
df.head()
```

---

### 💡 **¿Sabías que...?**

En machine learning, una correcta manipulación y preparación de columnas es crucial. Estandarizar nombres de columnas y limpiar valores atípicos y faltantes mejora significativamente la precisión y generalización de los modelos predictivos, ya que reduce el ruido y la variabilidad en los datos, facilitando el entrenamiento de algoritmos más potentes. Los pasos demostrados en este ejemplo contribuyen directamente a estos beneficios.

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Reto-02/Readme.md) ➡️