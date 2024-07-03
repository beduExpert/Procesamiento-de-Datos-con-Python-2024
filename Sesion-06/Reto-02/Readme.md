
🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 06**](../Readme.md) ➡️ / ⚡`Reto 02: Gestión de proyectos y tareas`

## 🎯 Objetivo

⚒️ Gestionar información relacionada con proyectos en una empresa de software usando Pandas, desde la creación de un DataFrame con índices personalizados hasta la manipulación de sus columnas para facilitar un análisis eficaz.

---

## 📝 Instrucciones

👥 Este reto puede ser resuelto en equipos o individualmente.

Considera el siguiente conjunto de datos que representa varios proyectos en una empresa de software. 
Cada proyecto tiene:
   - Un nombre único.
   - Una fase actual.
   - Un costo estimado.
   - Una duración estimada en días.

<!-- Codigo Python -->
```python
import pandas as pd

# Datos de proyectos
datos = {
    'Fase Actual': ['Diseño', 'Desarrollo', 'Testing', 'Lanzamiento', 'Mantenimiento'],
    'Costo Estimado': [20000, 50000, 15000, 30000, 10000],
    'Duración Estimada': [30, 90, 15, 20, 60]  # Duración en días
}
```

Realiza los siguientes pasos para gestionar y analizar los datos de proyectos:

1. 📊 **Crear el DataFrame con índices personalizados:**
    - Utiliza cualquier nombre para los 5 proyectos como índices.
    - Imprime el DataFrame inicial.

2. 📊 **Añade una nueva columna al DataFrame llamada 'Riesgo de Retraso':** que evalúe la duración estimada de cada proyecto. Si la duración es superior a 50 días, asigna un riesgo de "Alto", de lo contrario, será "Bajo".

    - Puedes utilizar un list comprehension para evaluar cada fila del DataFrame y asignar el riesgo correspondiente.

        ```python
        ['Alto' if x > 50 else 'Bajo' for x in proyectos['Duración Estimada']]
        ```

3. 🔄 **Actualiza la columna 'Costo Estimado':** con nuevos valores basados en revisiones recientes del presupuesto.

4. ❌ **Elimina la columna 'Duración Estimada':** del DataFrame.

---

🏆 Nos vemos en el siguiente reto, ¡mucho éxito!.

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Ejemplo-05/Readme.md) ➡️
