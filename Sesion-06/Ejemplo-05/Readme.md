🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 06**](../Readme.md) ➡️ / 📝 `Ejemplo 05: Análisis exploratorio y gestión de datos`

## 🎯 Objetivo

Implementar las herramientas básicas de Pandas para explorar y gestionar los datos contenidos en DataFrames, incluyendo la lectura y manipulación de archivos como `.csv` y `.json`, permitiendo realizar un primer análisis efectivo y una exploración inicial de la información disponible.

---

## 🚀 Comencemos

En Python existen diversas formas de cargar y gestionar datos. En este ejemplo, aprenderemos a cargar y explorar datos almacenados en archivos `.csv` y `.json`, utilizando Pandas para realizar un análisis exploratorio básico y comprender la estructura de los datos con los que estamos trabajando.

---

## 📂 Carga de Archivos en Google Colab

Para trabajar en el entorno de Google Colab, los archivos deben ser cargados previamente en una carpeta de Google Drive. Es necesario montar el sistema de archivos de Google Drive para acceder a los archivos desde Google Colab. Aquí te dejamos varios links que te pueden ayudar a realizar esta tarea:

- [Cargar archivos en Google Colab](https://colab.research.google.com/notebooks/io.ipynb)
- [Montar Google Drive en Google Colab](https://colab.research.google.com/notebooks/io.ipynb#scrollTo=7taylj9w6kU9)
- [Conectar Google Drive con Google Colab](https://colab.research.google.com/notebooks/io.ipynb#scrollTo=7taylj9w6kU9)

### 📥 Cargar Archivos `.csv` y `.json`

A continuación, te mostramos cómo cargar archivos `.csv` y `.json` en un DataFrame utilizando Pandas en Google Colab:

1. **Montar Google Drive:**
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```

2. **Leer un archivo `.csv`:**
   ```python
   import pandas as pd

   df_csv = pd.read_csv('/content/drive/MyDrive/PeliculasPlataformasStreaming.csv')
   df_csv.head()
   ```

3. **Leer un archivo `.json`:**
   ```python
   df_json = pd.read_json('/content/drive/MyDrive/Estados.json')
   df_json.head()
   ```

<!-- Nota -->
### 📌 **Nota**:
La ruta puede variar dependiendo de la ubicación de los archivos en tu Google Drive. Asegúrate de proporcionar la ruta correcta para acceder a los archivos `.csv` y `.json` que deseas cargar.

---

Exploraremos algunas características básicas del DataFrame para entender mejor los datos con los que estamos trabajando:

1. **Forma del DataFrame:**
   Utiliza `df.shape` para obtener el número de filas y columnas.

2. **Tipos de Datos:**
   Revisa `df.dtypes` para entender los tipos de datos de cada columna, asegurándote de que son adecuados para el análisis posterior.

3. **Información del DataFrame:**
   Con `df.info()`, puedes obtener un resumen que incluye el número de valores no nulos y el tipo de datos de cada columna, lo cual es útil para identificar columnas con valores faltantes.

4. **Visualización de Datos:**
   Utiliza `df.head()` y `df.tail()` para ver las primeras y últimas filas del DataFrame, proporcionando una vista rápida de los datos en ambos extremos.

---

### 💡 **¿Sabías que...?**

Google Colab no solo es compatible con Python, sino que también puede ejecutar código en R, lo que lo convierte en una herramienta versátil para el análisis de datos y la ciencia de datos. Para trabajar con R en Google Colab, puedes usar una celda de código mágico agregando %%R al inicio de la celda. Esto te permite aprovechar las capacidades de ambas lenguas en un solo entorno.

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../../Sesion-07/Readme.md) ➡️