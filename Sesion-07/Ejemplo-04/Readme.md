🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 07**](../Readie.md) ➡️ / 📝 `Ejemplo 04: Manipulación, reindexado y renombrado de columnas`

## 🎯 Objetivo

Explorar y aplicar técnicas de manipulación de columnas en dataframes de pandas para estandarizar la información, adaptarla a necesidades analíticas específicas, y optimizar la visualización y comprensión de los datos.

---

## 🚀 Introducción

La manipulación de columnas es una práctica esencial en el análisis de datos, para la preparación y limpieza de la información antes del análisis. Estas técnicas permiten a los analistas ajustar los datos a las especificaciones requeridas para una interpretación rapida y una visualización precisa.

---

### 📊 **Preparación del dataframe**

```python
import pandas as pd
import numpy as np

# Crear un DataFrame con datos y columnas más complejas
df = pd.DataFrame({
    'Nombre Completo': ['Juan Martínez', 'María Gómez', None, 'Ana Torres', 'Sofía Núñez'],
    'Edad al Cierre del Año': [28, 34, 19, np.nan, 45],
    'Ciudad de Residencia Actual': ['Madrid', 'Barcelona', 'Sevilla', 'Valencia', 'Bilbao'],
    'Ingresos Anuales Estimados': [1200, 1500, 900, 1100, np.nan],
    'Área de Vivienda (m²)': [np.nan, 45, 70, 80, 60],
    'Año de Construcción': [1990, 1985, np.nan, 2000, 2010]
})

# Convertir nombres de columnas a snake_case
df.columns = df.columns.str.lower().str.replace(' ', '_').str.replace('(', '').str.replace(')', '')
```

---

### 🛠️ **Limpieza de datos**

#### **Reemplazar NaN por un valor específico**

Reemplazar valores NaN en una columna clave para asegurar la integridad de los análisis posteriores.

```python
df['ingresos_anuales_estimados'] = df['ingresos_anuales_estimados'].fillna(1000)
print(df)
```

---

#### **Eliminar columnas innecesarias**

Eliminar las columnas que no aportan valor significativo al análisis.

```python
df.drop(columns=['área_de_vivienda_m²', 'año_de_construcción'], inplace=True)
```

---

#### **Eliminar filas con valores nulos**

Eliminar todas las filas que contienen al menos un valor NaN para limpiar el conjunto de datos.

```python
df.dropna(axis=0, how='any', inplace=True)
```

---

#### **Reindexar y renombrar**

Reiniciar el índice del DataFrame y cambiar el nombre de las columnas para mejorar la legibilidad.

```python
# Resetear índice conservando el viejo
df.reset_index(inplace=True)
print(df)

# Resetear índice eliminando el índice anterior
df.reset_index(drop=True, inplace=True)
print(df)

# Renombrar columnas
df.rename(columns={'nombre_completo': 'nombre', 'edad_al_cierre_del_año': 'edad', 'ciudad_de_residencia_actual': 'ciudad'}, inplace=True)
print(df)
```

---

### 💡 **¿Sabías que...?**

En machine learning, una correcta manipulación y preparación de columnas es crucial. Estandarizar nombres de columnas y limpiar valores atípicos y faltantes mejora significativamente la precisión y generalización de los modelos predictivos, ya que reduce el ruido y la variabilidad en los datos, facilitando el entrenamiento de algoritmos más potentes.

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Reto-02/Readme.md) ➡️