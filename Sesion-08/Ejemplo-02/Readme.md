🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 08**](../Readme.md) ➡️ / 📝 `Ejemplo 02: Técnicas avanzadas de filtrado en dataframes`

## 🎯 Objetivo

Desarrollar habilidades para aplicar técnicas avanzadas de filtrado en dataframes de pandas, permitiendo seleccionar y manipular datos para análisis específicos y extracción de información relevante.

---

## 🚀 Comencemos

El filtrado avanzado es esencial en el análisis de datos, permitiendo extraer subconjuntos de datos basados en condiciones específicas, se puede realizar, por ejemplo, para seleccionar columnas específicas, filtrar datos de texto o aplicar filtros booleanos para extraer datos que cumplen con ciertas condiciones.

---

## 🛠️ **Técnicas avanzadas de filtrado en dataframes** 🛠️

### 🧠 **Creación del dataframe general:**


```python
import pandas as pd

# Crear un DataFrame de ejemplo
df = pd.DataFrame({
    'Nombre': ['Ana', 'Luis', 'Carmen', 'José', 'Elena', 'Juan'],
    'Edad': [25, 30, 22, 27, 31, 19],
    'Ciudad': ['Tokio', 'Moscú', 'Londres', 'París', 'Sídney', 'Ciudad de México'],
    'Puntuación': [85, 88, 90, 95, 82, 78],
    'Ocupación': ['Estudiante', 'Ingeniero', 'Estudiante', 'Doctor', 'Arquitecto', 'Estudiante']
})
df.head(10)
```

### 📅 **Uso del método `filter()`:**

Pandas permite filtrar datos usando el método `filter()`, que puede ser útil para seleccionar **`columnas específicas`** de un DataFrame basado en etiquetas o condiciones de contenido.

```python
# Filtrar columnas por nombres que contienen ciertas letras
df_filtrado = df.filter(like='Nombre')
df_filtrado.head(10)
```
```python
# Filtrar columnas por nombres específicos
df_filtrado = df.filter(items=['Nombre', 'Edad', 'Ciudad'])
df_filtrado.head(10)
```

---

### 📝 **Aplicación de filtros de texto:**

Pandas permite filtrar datos de texto en columnas de un DataFrame, utilizando métodos específicos como `str.contains()` para seleccionar filas que contienen una cadena de texto en particular.

```python
# Filtrar filas por ciudad que contienen la letra 'a'
df_filtrado = df[df['Ciudad'].str.contains('T')]
df_filtrado.head(10)
```

---

### 🧮 **Aplicación de filtros booleanos:**

Los filtros booleanos son expresiones que resultan en `True` o `False` para cada fila del DataFrame, permitiendo extraer datos que cumplen con una condición específica.

```python
# Aplicar filtro booleano para seleccionar personas mayores de 25 años
df_filtrado = df[df['Edad'] > 25]
df_filtrado.head(10)
```

```python
# Aplicar filtro booleano para seleccionar personas con puntuación mayor o igual a 85
df_filtrado = df[df['Puntuación'] >= 85]
df_filtrado.head(10)
```

---

### 🚨 **Filtros complejos con múltiples condiciones:**

En Pandas, al aplicar filtros en DataFrames, se requiere el uso de operadores lógicos específicos para realizar operaciones element-wise sobre matrices de NumPy. En lugar de los operadores estándar de Python (and, or, not), se utilizan:

- **`&`** para **AND**
- **`|`** para **OR**
- **`~`** para **NOT**

```python
# Seleccionar filas donde (Edad < 31) y (Ocupación es 'Estudiante')
df_filtrado_and = df[(df['Edad'] < 31) & (df['Ocupación'] == 'Estudiante')]
df_filtrado_and.head()

# Seleccionar filas donde (Edad < 30) o (Puntuación es igual a 85)
df_filtrado_or = df[(df['Edad'] < 30) | (df['Puntuación'] == 85)]
df_filtrado_or.head()

# Seleccionar filas donde (Ocupación no es 'Estudiante')
df_filtrado_not = df[~(df['Ocupación'] == 'Estudiante')]
df_filtrado_not.head()
```

---

### 💡 **¿Sabías que...?**

1. **Usa filtros booleanos para condiciones simples**: Para condiciones básicas, los filtros booleanos son una forma eficiente de seleccionar datos.

2. **Usa filter() para seleccionar columnas**: Si necesitas seleccionar columnas específicas, el método filter() es una opción rápida y sencilla.

3. **Usa operadores lógicos para múltiples condiciones**: Al combinar condiciones, recuerda usar los operadores lógicos adecuados para obtener los resultados esperados.

4. **Agrupa condiciones con paréntesis**: Para evitar errores de precedencia, agrupa las condiciones con paréntesis para asegurar que las operaciones se realicen en el orden correcto.

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Reto-01/Readme.md) ➡️