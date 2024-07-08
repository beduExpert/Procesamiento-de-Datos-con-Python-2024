🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 07**](../Readme.md) ➡️ / 📝 `Ejemplo 02: Operaciones aritméticas con DataFrames`

## 🎯 Objetivo

Implementar operaciones aritméticas y de agregación utilizando dataframes en pandas, transformando grandes conjuntos de datos de manera rapida y efectiva.

---

## 🚀 Introducción

Al igual que las series, los DataFrames en Pandas permiten una amplia gama de operaciones aritméticas y funciones de agregación. Estas operaciones pueden aplicarse tanto a columnas individuales como a todo el DataFrame, facilitando el cálculo de estadísticas y la transformación de datos a gran escala.

---

## 📊 **Operaciones aritméticas con dataframes** 📈

### 🛠️ **Operaciones básicas**

Podemos aplicar las mismas operaciones matemáticas básicas directamente a dataframes, lo que afecta a cada elemento de la estructura:

```python
import pandas as pd
import numpy as np

# Crear un DataFrame de ejemplo, con valores aleatorios
df = pd.DataFrame({
    'A': np.random.randint(1, 10, 5),
    'B': np.random.randint(1, 10, 5)
})

# Sumar un número a cada elemento del DataFrame
print(df + 10)

# Multiplicar cada elemento por un escalar
print(df * 10)
```

---

### 🛠️ **Funciones vectorizadas en dataframes**

Utilizando funciones vectorizadas de pandas y numpy para realizar operaciones más complejas y personalizadas:

```python
# Sumar dos DataFrames
print(df + df)

# Elevar al cuadrado cada elemento
print(df.pow(2))
```

---

### 🛠️ **Funciones de agregación en dataframes**

Estas funciones resumen los datos de un DataFrame en valores únicos, proporcionando estadísticas claves como sumas totales y promedios por columna:

```python
# Sumar todos los elementos de cada columna
print(df.sum())

# Calcular el promedio de cada columna
print(df.mean())

# Obtener el valor mínimo y máximo de cada columna
print(df.min())
print(df.max())
```

---

### 💡 **¿Sabías que...?**

- **Capacidades avanzadas**: Pandas no solo soporta tipos de datos heterogéneos en un dataframe, sino que también ofrece funciones avanzadas para manejar fechas, textos, y datos categóricos.

- **Análisis ampliado**: Con la ayuda de numpy, pandas puede realizar cálculos matemáticos complejos, desde transformaciones simples hasta algoritmos estadísticos avanzados.

#### 📊 **Funciones destacadas de NumPy utilizadas en dataframes**

| Función | Descripción |
|---------|-------------|
| `np.sum()` | Suma los elementos de una o más columnas. |
| `np.mean()` | Calcula el promedio de una o más columnas. |
| `np.max()` | Determina el valor máximo dentro de cada columna. |
| `np.min()` | Determina el valor mínimo dentro de cada columna. |
| `np.std()` | Estima la desviación estándar de cada columna. |

Estas funciones pueden ser especialmente útiles para realizar análisis detallados y rapidos en grandes conjuntos de datos.

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Reto-01/Readme.md) ➡️
