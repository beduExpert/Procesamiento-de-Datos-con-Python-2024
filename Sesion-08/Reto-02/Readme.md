🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 08**](../Readme.md) ➡️ / ⚡`Reto 02: Análisis de datos de tráfico en una ciudad`

## 🎯 Objetivo

⚒️ Aplicar técnicas de ordenamiento, transformación, combinación y agrupación en un dataframe que contiene datos de tráfico en una ciudad para identificar patrones de congestión y correlaciones con factores meteorológicos.

---

## 📋 Desarrollo

1. 📊 **Generar un dataframe con valores aleatorios**:

Contamos con dos dataframes que representan datos de tráfico y datos meteorológicos.

```python
import pandas as pd
import numpy as np

# Generar datos para el DataFrame de tráfico
np.random.seed(0)
fechas_trafico = pd.date_range(start='2024-07-01', periods=30, freq='D')
horas_trafico = ['08:00', '17:00']
zonas_trafico = ['Centro', 'Norte', 'Sur', 'Este', 'Oeste']

# Crear DataFrame de tráfico con 150 datos
df_trafico = pd.DataFrame(
    {
      'fecha': np.tile(fechas_trafico, len(horas_trafico) * len(zonas_trafico)),
      'hora': np.repeat(horas_trafico * len(fechas_trafico), len(zonas_trafico)),
      'zona': np.tile(zonas_trafico, len(fechas_trafico) * len(horas_trafico)),
      'vehiculos': np.random.randint(100, 500, size=(len(fechas_trafico) * len(horas_trafico) * len(zonas_trafico)))
  }
)

# Crear DataFrame meteorológico con 30 días de datos
df_meteorologico = pd.DataFrame(
    {
      'fecha': fechas_trafico,
      'temperatura': np.random.uniform(25, 35, size=len(fechas_trafico)),
      'precipitacion': np.random.uniform(0, 10, size=len(fechas_trafico))
  }
)
```
---

## 📝 Instrucciones

👥 Este reto se puede resolver en equipos o de manera individual.

1. **Ordenar datos de tráfico:**
   - Ordena el DataFrame de tráfico por fecha y hora en orden ascendente.

2. **Transformar datos:**
   - Incrementa la columna `vehiculos` en un formato que permita visualizar mejor la cantidad de vehículos (por ejemplo, en miles).
   - Limpia cualquier espacio en blanco en la columna `zona`.

3. **Combinar dataframes:**
   - Combina el DataFrame de tráfico con el DataFrame meteorológico usando la columna `fecha` para unir los datos.

4. **Agrupar y analizar:**
   - Agrupa los datos combinados por `zona` y `hora` para calcular el promedio de vehículos y la temperatura máxima en cada zona por hora.
   - Calcula la cantidad promedio de vehículos en función de la `precipitacion` para identificar si hay una correlación entre la precipitación y el tráfico.

5. **Mostrar resultados:**
   - Muestra los resultados obtenidos en un nuevo DataFrame.

---

🏆 ¡Buena suerte con el análisis de datos de tráfico! Asegúrate de verificar las relaciones entre el tráfico y el clima para obtener conclusiones útiles.

---

⬅️ [**Anterior**](../Readme.md) | 🏠 [**Inicio**](../../Readme.md)