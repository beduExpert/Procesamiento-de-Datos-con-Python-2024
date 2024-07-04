🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 07**](../Readme.md) ➡️ / 📝 `Ejemplo 01: Operaciones aritméticas con series`

## 🎯 Objetivo

Explorar y aplicar operaciones aritméticas y funciones de agregación con series en Pandas, facilitando el procesamiento y análisis de datos con Python.

---

## 🚀 Comencemos

Las operaciones aritméticas y funciones de agregación son fundamentales para analizar y entender nuestros datos. Nos permiten obtener información clave como sumas, promedios, máximos y mínimos de los valores en una serie.

---

## 📊 **Operaciones aritméticas con Series** 📈

### 🛠️ **Operaciones simples**

Las operaciones simples incluyen suma, resta, multiplicación y división que se pueden realizar tanto con escalares como con otras series:

```python
import pandas as pd

# Crear una serie de ejemplo
serie_1 = pd.Series([1, 2, 3, 4, 5])

# Sumar un escalar
print(serie_1 + 10)

# Multiplicar por un escalar
print(serie_1 * 10)

# Sumar serie con serie
print(serie_1 + serie_1)

# Multiplicar serie con serie
print(serie_1 * serie_1)
```

### 🛠️ **Funciones vectorizadas**

Las funciones vectorizadas permiten realizar operaciones sobre cada elemento de la serie de manera directa y rápida:

```python
# Usar funciones vectorizadas para operaciones matemáticas
print(serie_1.add(10))  # Equivalente a serie_1 + 10
print(serie_1.mul(10))  # Equivalente a serie_1 * 10
print(serie_1.pow(2))   # Elevar al cuadrado cada elemento
```

### 🛠️ **Funciones de agregación**

Estas funciones ayudan a resumir los datos en un solo valor que describe un conjunto de datos:

```python
# Ejemplos de funciones de agregación
print(serie_1.sum())   # Suma total de los elementos de la serie
print(serie_1.mean())  # Promedio de los elementos de la serie
print(serie_1.min())   # Valor mínimo de la serie
print(serie_1.max())   # Valor máximo de la serie
print(serie_1.count()) # Cuenta los elementos no nulos en la serie
```

---

### 💡 **¿Sabías que...?**

Pandas es una librería de Python que proporciona estructuras de datos de alto nivel y herramientas de análisis de datos. Algunas de las características clave de Pandas son:

- **Optimización**: Pandas está construido sobre NumPy, aprovechando algoritmos compilados en C para operaciones vectorizadas rápidas.

- **Gestión de memoria**: Utiliza `BlockManager` para almacenar datos de forma flexible y manejar tipos heterogéneos, a diferencia del almacenamiento contiguo de NumPy.

- **Extensibilidad**: Además del análisis de datos, Pandas se expande con APIs como `GeoPandas` para análisis geoespacial y `Pandas TA` para el trading.

- **Aplicaciones industriales**: Usado en finanzas para análisis cuantitativo, en biotecnología para datos genómicos, y otros campos que gestionan datos complejos.

- **Interoperabilidad con SQL**: Permite la interacción directa con bases de datos SQL, facilitando la carga y manipulación avanzada de datos en `DataFrames`.

Numpy es una librería de python que proporciona soporte para arreglos y matrices multidimensionales, junto con una colección de funciones matemáticas de alto nivel para operar con estos arreglos. Algunas de las características clave de numpy son:


### 📊 **Funciones comunes de numpy para usar con pandas series**

| Función de NumPy   | Descripción                                 |
|--------------------|---------------------------------------------|
| `np.sum()`         | Calcula la suma de los elementos.           |
| `np.mean()`        | Calcula el promedio de los elementos.       |
| `np.max()`         | Encuentra el valor máximo.                  |
| `np.min()`         | Encuentra el valor mínimo.                  |
| `np.std()`         | Calcula la desviación estándar.             |

Estas funciones pueden ser aplicadas directamente a `pd.Series` para realizar cálculos estadísticos rápidos y eficientes, aprovechando la integración estrecha entre pandas y numpy.

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Ejemplo-02/Readme.md) ➡️
