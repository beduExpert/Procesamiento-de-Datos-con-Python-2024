🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 06**](../Readme.md) ➡️ / 📝 `Ejemplo 01: Series de Pandas`

## 🎯 Objetivo

Implementar los métodos más populares de Series en Pandas para manipular y extraer información, aplicando técnicas de procesamiento de datos con Python.

---

## 🚀 Comencemos

Una serie en Pandas representa una columna en una hoja de cálculo, con datos como números, texto o fechas. Cada elemento tiene una etiqueta llamada `índice` para acceder a él, similar a una columna de una tabla que organiza datos de manera ordenada.

---

## 📊 **Series en Pandas** 📈

Las Series son secuencias ordenadas unidimensionales que pueden contener diversos tipos de valores, similares a las listas. Cada elemento tiene un índice, que no necesariamente es numérico, y se utiliza para acceder a los datos de forma eficiente.

### 🛠️ **Creando Series**

Recuerda importar la librería de Pandas antes de crear una Serie:

```python
import pandas as pd
```

1. **A partir de listas:** Usa listas de Python para crear Series y asigna índices automáticamente.
   ```python
   serie_list = pd.Series([1, 2, 3, 4])
   ```
2. **A partir de diccionarios:** Cada clave del diccionario se convierte en un índice en la Serie.
   ```python
   serie_dict = pd.Series({'a': 1, 'b': 2, 'c': 3})
   ```

3. **Con índices personalizados:** Puedes especificar los índices manualmente.
   ```python
   serie_index = pd.Series([1, 2, 3], index=['a', 'b', 'c'])
   ```

---

### 📊 **Visualizando Series**

Puedes visualizar una Serie simplemente imprimiéndola en la consola, o usando el método `print()`.

```python
print(serie_dict)

# Salida:
# a    1
# b    2
# c    3
# dtype: int64
```

El signo `dtype: int64` indica que los datos en la Serie son de tipo numérico (`int64`), lo cual es útil para saber qué tipo de datos estás manejando, especialmente en Series grandes.

---


### 📐 **Tipos de Datos en Series**

Pandas maneja distintos tipos de datos en las Series para adecuarse a diversas necesidades de información.

| Tipo de Dato | Descripción                                              |
|--------------|----------------------------------------------------------|
| `int64`      | Números enteros, equivalente a `int` en Python.          |
| `float64`    | Números con decimales, equivalente a `float` en Python.  |
| `bool`       | Valores booleanos, `True` o `False`, como en Python.     |
| `object`     | Cadenas de texto o mezcla de tipos, similar a `str` en Python. |


Pandas se encarga de inferir el tipo de dato más apropiado cuando creas una Serie, pero también puedes especificarlo manualmente.

---


### 📐 **Propiedades comunes**

Las Series en Pandas tienen varias propiedades que puedes utilizar para obtener información sobre los datos que contienen.

| Propiedad | Descripción                                              | Ejemplo de uso             |
|-----------|----------------------------------------------------------|----------------------------|
| `shape`   | Devuelve una tupla que indica el tamaño de la Serie.     | `data.shape -> Salida: (3,)`       |
| `size`    | Devuelve el número total de elementos en la Serie.       | `data.size -> Salida: 3`           |
| `dtype`   | Devuelve el tipo de datos de la Serie.                   | `data.dtype -> Salida: int64`      |
| `index`   | Devuelve los índices de la Serie.                        | `data.index -> Salida: Index(['a', 'b', 'c'], dtype='object')` |
| `values`  | Devuelve los valores de la Serie como un array.          | `data.values -> Salida: array([1, 2, 3])` |

---

### 💡 **¿Sabías que...?**

Pandas fue desarrollado inicialmente para el manejo de datos financieros, y su nombre deriva de "Panel Data", un término de econometría que hace referencia a datos multidimensionales.

Polars es una alternativa a Pandas que está ganando popularidad por su velocidad y eficiencia en el manejo de grandes volúmenes de datos, especialmente en entornos de Big Data.

Pandas vs Polars: ¿Cuál es mejor? La respuesta depende de tus necesidades y del tamaño de tus datos. Pandas es más versátil y fácil de usar, mientras que Polars es más rápido y eficiente para grandes volúmenes de datos.

Si bien Pandas y NumPy son las bibliotecas más populares para el manejo de datos en Python, existen otras alternativas como Dask, Vaex y Modin que ofrecen funcionalidades similares y están diseñadas para trabajar con grandes volúmenes de datos.

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Ejemplo-02/Readme.md) ➡️
