🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 07**](../Readme.md) ➡️ / ⚡`Reto 01: Evaluación de rendimiento academico`

## 🎯 Objetivo

⚒️ Explorar y manipular un dataframe que contiene las calificaciones de diferentes estudiantes en diversas materias, utilizando pandas para realizar un análisis básico y extraer información relevante.

---

## 📝 Instrucciones

👥 Este reto se puede resolver en equipos o de manera individual.

Contamos con un dataframe que representa las calificaciones de tres estudiantes en distintas materias. Aquí se muestra cómo se ha creado y visualizado el dataframe:

```python
import pandas as pd

# Ejemplo de dataframe con calificaciones
data = {
    'Estudiante': ['Ana', 'Ana', 'Ana', 'Luis', 'Luis', 'Luis', 'María', 'María', 'María'],
    'Materia': ['Matemáticas', 'Historia', 'Ciencias', 'Matemáticas', 'Historia', 'Ciencias', 'Matemáticas', 'Historia', 'Ciencias'],
    'Calificación': [85, 90, 78, 88, 85, 92, 90, 88, 85]
}

df = pd.DataFrame(data)
df.head()
```

Realiza los siguientes pasos para explorar y manipular los datos:

1. 📊 **Calcular la suma total de las calificaciones de cada estudiante**.
   - Puedes usar un filtro para obtener las calificaciones de cada estudiante: `df[df['Estudiante'] == 'NOMBRE']['Calificación'].FUNCION()`
   - Este proceso lo veremos mas a detalle en la siguiente sesión.
2. 🔢 **Calcular el promedio de las calificaciones de cada estudiante**.
3. 📏 **Determinar la calificación más alta y más baja registrada en el DataFrame**.

4. 📄 **Mostrar los resultados, e imprime un mensaje similar:**
   ```plaintext
   ✉️ Suma y promedio de calificaciones de Ana: 253 y 84.33
   ✉️ Suma y promedio de calificaciones de Luis: 265 y 88.33
   ✉️ Suma y promedio de calificaciones de María: 263 y 87.67
   ✉️ Calificación más alta en el DataFrame: 92
   ✉️ Calificación más baja en el DataFrame: 78
   ```

---

🏆 Nos vemos en el siguiente reto, ¡mucho éxito!.

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Ejemplo-03/Readme.md) ➡️