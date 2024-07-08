🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 07**](../Readme.md) ➡️ / ⚡`Reto 02: Encuestas de satisfacción del cliente`

## 🎯 Objetivo

⚒️ Explorar y manipular un dataframe que contiene datos de encuestas de satisfacción de clientes en comercio electrónico, utilizando pandas para realizar un análisis básico y extraer información relevante.

---

## 📝 Instrucciones

👥 Este reto se puede resolver en equipos o de manera individual.

Contamos con un dataframe que representa las respuestas de una encuesta de satisfacción de clientes. 

```python
import pandas as pd
import numpy as np

# Simular datos de una encuesta de satisfacción de clientes de comercio electrónico
data = {
    'ID_Cliente': [101, 102, 103, 104, 105, 106],
    'Fecha_Encuesta': ['2023-01-01', '2023-01-02', np.nan, '2023-01-04', '2023-01-05', '2023-01-06'],
    'Puntuacion_Satisfaccion': [5, 4, 3, np.nan, 5, 4],  # Escala de 1 a 5
    'Comentarios': ['Todo excelente', np.nan, 'Buen servicio', 'Regular', np.nan, 'Muy bueno']
}

df = pd.DataFrame(data)
df.head(10)
```

Realiza los siguientes pasos para explorar y manipular los datos:

1. 📊 **Imprime el numero de NaNs, para filas y columnas**:
   ```plaintext
   Conteo de valores NaN por columna:
   ...
   --------------------
   Conteo de valores NaN por renglon:
   ...
   ```
   
2. 🗑️ **Eliminar filas Iincompletas**:
   - Eliminar filas donde 'Fecha_Encuesta'o 'Puntuacion_Satisfaccion' contienen por lo menos u nvalor nulo.
   - Usa el método `.copy()` para manipulaciones seguras.

3. 📝 **Manejo de comentarios faltantes**:
   - Reemplaza los valores nulos en la columna 'Comentarios' con 'Sin comentarios' usando `fillna()`.

4. 🔄 **Reindexar el dataframe**:
   - Reorganiza los índices después de eliminar filas.

5. ✏️ **Estandarización de nombres de columnas**:
   - Convierte todos los nombres de columnas a minúsculas y reemplaza los espacios por guiones bajos para una manipulación más fácil.

6. 🔤 **Renombrar columnas específicas**:
   - Cambia el nombre de la columna 'puntuacion_satisfaccion' a 'calificacion' para reflejar mejor los datos.

7. 🖨️ **Mostrar el DataFrame Actualizado**:
   - Imprime el `DataFrame` final para verificar los cambios realizados.

---

🏆 Nos vemos en el siguiente reto, ¡mucho éxito!.

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../../Sesion-08/Readme.md) ➡️