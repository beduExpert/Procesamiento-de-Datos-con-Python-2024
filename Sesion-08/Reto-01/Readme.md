🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 08**](../Readme.md) ➡️ / ⚡`Reto 01: Limpieza y conversión de datos`

## 🎯 Objetivo

⚒️ Aplicar técnicas de limpieza y conversión de datos para transformar un dataframe con datos sucios en un formato más estructurado y manejable.

---

## 📋 Desarrollo

1. 📊 **Generar un dataframe con valores aleatorios**:

```python
import pandas as pd
import numpy as np

# Crear un DataFrame de ejemplo con datos sucios
def create_dirty_data(num_rows):
    np.random.seed(0)  # Para reproducibilidad

    # Generar datos aleatorios para cada columna
    nombres = [f'Nombre_{i}' for i in range(num_rows)]
    edades = np.random.choice(['25', '30', '22', '27', '31 años', '19', 'not available', ''], num_rows)
    ciudades = np.random.choice(['Tokio', 'Moscú', 'Londres', 'París ', 'Sídney', 'Ciudad de México', '   ', '', 'Moscú   '], num_rows)
    puntuaciones = np.random.choice(['85', '88', '90.5', '95', '82', 'setenta y ocho', '', 'NaN'], num_rows)
    ocupaciones = np.random.choice(['Estudiante', 'Ingeniero', 'Estudiante', 'Doctor', 'Arquitecto', 'Estudiante ', ''], num_rows)
    fechas = np.random.choice(['2021-01-01', '2021-02-01', 'not available', '2021-04-01', '2021-05-01', '2021/06/01', '01-07-2021'], num_rows)
    precios = np.random.choice(['100.50', '200', 'not a number', '150.75', '200.00', '250.10', '', 'NaN'], num_rows)
    cantidades = np.random.choice(['1', 'two', '3', '4', 'five', '6', '', 'NaN'], num_rows)

    df = pd.DataFrame({
        'Nombre': nombres,
        'Edad': edades,
        'Ciudad': ciudades,
        'Puntuación': puntuaciones,
        'Ocupación': ocupaciones,
        'Fecha de Compra': fechas,
        'Precio Unitario': precios,
        'Cantidad': cantidades
    })

    return df

# Crear un DataFrame con 200 datos sucios
df_dirty = create_dirty_data(250)
df_dirty.head()
```
---

## 📝 Instrucciones

👥 Este reto se puede resolver en equipos o de manera individual.

1. 📊 **Conversión de datos**: Convierte los siguientes campos a su tipo de dato correspondiente, tratando cualquier valor no convertible como `NaN`
   - `'Edad'`.
   - `'Puntuación'`.
   - `'Precio Unitario'`.
   - `'Cantidad'`.
   - `'Fecha de Compra'`.

2. 🧹 **Limpieza de espacios**:
   - Elimina espacios en blanco al inicio y al final de los valores en las columnas `'Nombre'`, `'Ciudad'`, y `'Ocupación'`.
   - Reemplaza los valores vacíos en `'Ciudad'` y `'Ocupación'` por `'Desconocida'`.

3. 🔄 **Llenado de `NaN`**:
   - Rellena los valores `NaN` en las columnas `'Edad'`, `'Puntuación'`, `'Precio Unitario'`, y `'Cantidad'` con la mediana de la columna respectiva.
   - Rellena los valores `NaN` en las columnas `'Ciudad'` y `'Ocupación'` con `'Desconocida'`.
   - Rellena los valores `NaT` en la columna `'Fecha de Compra'` con la fecha actual.

4. 🧩 **Mostrar el dataframe actualizado**:
   - Muestra el dataframe resultante después de aplicar las transformaciones.

---

🏆 Nos vemos en el siguiente reto, ¡mucho éxito!.

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Ejemplo-03/Readme.md) ➡️