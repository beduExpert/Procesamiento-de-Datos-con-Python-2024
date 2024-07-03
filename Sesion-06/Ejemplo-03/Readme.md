🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 06**](../Readme.md) ➡️ / 📝 `Ejemplo 03: Dataframes`

## 🎯 Objetivo

Implementar técnicas avanzadas en Pandas para construir DataFrames a partir de diccionarios de listas y realizar indexación eficiente, facilitando la extracción y manipulación de subconjuntos de datos específicos en Python.

---

## 🚀 Comencemos

Un `DataFrame` en Pandas es una estructura de datos bidimensional y tabular en Python, diseñada para almacenar y manipular datos estructurados. Cada columna en un `DataFrame` puede contener tipos de datos variados y esencialmente representa una serie de `Series` alineadas verticalmente. Esta estructura proporciona herramientas avanzadas para el análisis de datos, permitiendo operaciones como slicing, indexación y selección, además de facilitar métodos para la manipulación estadística de datos.

---

<div align="center">
    <img src="/Sesion-06/Imagenes/Dataframe.png" alt="API" width="800" height="400">
</div>

---

## 📋 **DataFrame en Pandas** 📊

Existen diversas formas de crear un `DataFrame` en Pandas, veamos algunas de las más comunes:

Recuerda importar la librería de Pandas antes de crear un DataFrame:

```python
import pandas as pd
```

1. **A partir de diccionarios de listas:** Cada clave del diccionario se convierte en una columna y cada lista en los valores de esa columna.
   ```python
   data = {
       'nombre': ['Juan', 'Ana', 'Luis', 'Diana'],
       'edad': [25, 30, 35, 40],
       'ciudad': ['CDMX', 'GDL', 'MTY', 'PUE']
   }
   df = pd.DataFrame(data)

   print(df)
   
   # Salida:
   #    nombre  edad ciudad
   # 0   Juan    25   CDMX
   # 1    Ana    30    GDL
   # 2   Luis    35    MTY
   # 3  Diana    40    PUE
   ```

<!-- A partir de una Serie: -->

2. **A partir de multiples Series:** Cada Serie se convierte en una columna en el DataFrame.
   ```python
   s1 = pd.Series([1, 2, 3], index=['a', 'b', 'c'], name='Columna1')
   s2 = pd.Series([4, 5, 6], index=['a', 'b', 'c'], name='Columna2')
   df = pd.DataFrame({s1.name: s1, s2.name: s2})

   print(df)

   # Salida:
   #    Columna1  Columna2
   # a         1         4
   # b         2         5
   # c         3         6
   ```


3. **Con índices personalizados:** Puedes especificar los índices manualmente.
   ```python
   data = {
       'nombre': ['Juan', 'Ana', 'Luis', 'Diana'],
       'edad': [25, 30, 35, 40],
       'ciudad': ['CDMX', 'GDL', 'MTY', 'PUE']
   }
   df = pd.DataFrame(data, index=['renglon_1', 'renglon_2', 'renglon_3', 'renglon_4'])

   print(df)

   # Salida:
   #             nombre  edad  ciudad
   # renglon_1    Juan    25    CDMX
   # renglon_2    Ana     30    GDL
   # renglon_3    Luis    35    MTY
   # renglon_4    Diana   40    PUE
   ```

Ahora te preguntaras que significan ciertos términos utilizados dentro de los paréntesis, como `index` y `name`. Estos son argumentos opcionales que puedes utilizar para personalizar tu DataFrame, veamos qué significan:

- `index`: Especifica los índices de las filas en el DataFrame. Si no se especifica, Pandas asigna índices numéricos de forma automática.

- `name`: Especifica el nombre de la columna en el DataFrame. Si no se especifica, Pandas asigna un nombre genérico.

Existen muchos otros argumentos que puedes utilizar para personalizar tu DataFrame, aqui te dejamos algunos links para que puedas explorar más sobre ellos:

- [Documentación oficial de Pandas](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.html)

- [Tutorial de Pandas](https://aprendepython.es/pypi/datascience/pandas/#dataframes)

- [Código de ejemplo](https://www.geeksforgeeks.org/python-pandas-dataframe/)

---

<!-- Metodos de indexacion en vertical y horizontal -->

## 📌 **Métodos de indexación en DataFrames**

Una vez que has creado un DataFrame, puedes acceder a los datos de diferentes maneras utilizando métodos de indexación en Pandas. Estos métodos te permiten seleccionar subconjuntos de datos específicos en el DataFrame, ya sea en forma vertical o en horizontal.

### **Indexación en vertical**

- **Por varias columnas:** Puedes acceder a varias columnas a la vez utilizando una lista de nombres de columnas.
  ```python
  print(df[['nombre', 'ciudad']])

  # Salida:
  #    nombre ciudad
  # 0   Juan   CDMX
  # 1    Ana    GDL
  # 2   Luis    MTY
  # 3  Diana    PUE
  ```
   Tambien puedes usar rangos y slices para obtener un subconjunto de columnas.

### **Indexación en horizontal**

- **Por rango de filas:** Puedes acceder a un rango de filas utilizando la propiedad `iloc`.
  ```python
   print(df.iloc[1:3])

   # Salida:
   #    nombre  edad ciudad
   # 1    Ana    30    GDL
   # 2   Luis    35    MTY

   # Recuerda que el rango es inclusivo en el inicio y exclusivo en el final.
  ```


- **Por multiples filas y columnas:** Puedes acceder a un subconjunto de filas y columnas utilizando la propiedad `loc`.
  ```python
   print(df.loc[1:3, ['nombre', 'ciudad']])

   # Salida:
   #    nombre ciudad
   # 1    Ana    GDL
   # 2   Luis    MTY
   # 3  Diana    PUE

   # En este caso, el primer rango corresponde a las filas y el segundo rango a las columnas.
  ```


---

### 💡 **¿Sabías que...?**

La visualización de datos y el machine learning son dos campos estrechamente interconectados que se benefician enormemente de la flexibilidad y el poder de Pandas. Algunas de las bibliotecas más populares que se integran con Pandas son:

1. **Visualización con Matplotlib y Seaborn:** 
   - **Matplotlib** es ampliamente utilizada para personalizar gráficos, mientras que **Seaborn** ofrece una interfaz simplificada para gráficos estadísticos, ambos trabajando eficientemente con `DataFrames` de Pandas.

2. **Machine Learning con Scikit-learn:**
   - **Scikit-learn** facilita el análisis predictivo y se integra directamente con Pandas, simplificando la preparación de datos para modelos predictivos.

3. **Deep Learning con TensorFlow y Keras:**
   - Aunque **TensorFlow** y **Keras** manejan datos en forma de tensores, Pandas es útil para la carga y manipulación inicial antes de convertirlos, permitiendo tareas como la normalización y la codificación de variables categóricas.

Estas herramientas, en conjunto, permiten desde la visualización hasta el desarrollo de modelos avanzados de machine learning y deep learning, formando un ecosistema completo para el análisis de datos.

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Ejemplo-04/Readme.md) ➡️