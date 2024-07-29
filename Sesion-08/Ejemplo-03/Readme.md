🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 08**](../Readme.md) ➡️ / 📝 `Ejemplo 03: Ordenamiento y transformación de dataframes`

## 🎯 Objetivo

Desarrollar habilidades para ordenar y transformar dataframes en Pandas, utilizando métodos como `sort`, `map`, y `apply` para organizar datos y aplicar funciones que mejoran el análisis y la presentación de información.

---

## 🚀 Comencemos

Ordenar y transformar Dataframes son técnicas esenciales en el análisis de datos, permitiendo no solo organizar la información de manera más efectiva, sino también aplicar transformaciones específicas para preparar los datos para análisis posteriores.

---

## 🛠️ **Técnicas de ordenamiento y transformación en dataframes** 🛠️

### 🧠 **Creación del dataframe general:**

```python
import pandas as pd

# Crear un DataFrame de ejemplo con datos de pacientes en un hospital
df = pd.DataFrame({
    'Paciente': ['John Smith', 'Laura Jones', 'Gary White', 'Sonia Taylor', 'Raj Patel', 'Emily Howard', 'Bruce Wayne', 'Clark Kent', 'Diana Prince', 'Peter Parker'],
    'Edad': [28, 34, 22, 45, 30, 26, 40, 35, 32, 29],
    'Diagnóstico': ['Apendicitis', 'Fractura de brazo', 'Gripe', 'Diabetes Tipo 2', 'Hipertensión', 'Alergias', 'Anemia', 'Bronquitis', 'Artritis', 'Quemaduras leves'],
    'Días Hospitalizado': [3, 5, 2, 7, 3, 1, 4, 6, 5, 2],
    'Costo del Tratamiento ($)': [1500, 3000, 200, 5000, 1000, 300, 1200, 1800, 2500, 500]
})
df.head(10)
```

---

### 📊 **Ordenamiento de dataframes**

La función `sort_values` permite ordenar un Dataframes por una o más columnas, facilitando la visualización y el análisis de datos de manera más efectiva.

```python
# Ordenar renglones por la columna 'Edad' en orden ascendente
df_ordenado = df.sort_values(by='Edad')
df_ordenado.head(10)
```

```python
# Ordenar renglones por la columna 'Costo del Tratamiento ($)' en orden descendente
df_ordenado = df.sort_values(by='Costo del Tratamiento ($)', ascending=False)
df_ordenado.head(10)
```

```python
# Ordenar renglones por las columnas 'Edad' y 'Días Hospitalizado'
df_ordenado = df.sort_values(by=['Edad', 'Días Hospitalizado'], ascending=[True, False])
df_ordenado.head(10)
```

---

### 🎲 **Transformación con `map` y `apply`**

Estas funciones son útiles para realizar transformaciones específicas en los datos, permitiendo tanto cambios simples como operaciones más complejas en todo el Dataframes.

#### 🔄 Uso de `map` en una Serie:

Recuerda que `map` es una función que se aplica a una Serie de Pandas, permitiendo mapear valores existentes a nuevos valores basados en un diccionario o función específica.

```python
# Supongamos que necesitamos codificar la columna de 'Diagnóstico' para un análisis anónimo.
diagnostico_codificado = {
    'Apendicitis': 'D01',
    'Fractura de brazo': 'D02',
    'Gripe': 'D03',
    'Diabetes Tipo 2': 'D04',
    'Hipertensión': 'D05',
    'Alergias': 'D06',
    'Anemia': 'D07',
    'Bronquitis': 'D08',
    'Artritis': 'D09',
    'Quemaduras leves': 'D10'
}
df['Diagnóstico Codificado'] = df['Diagnóstico'].map(diagnostico_codificado)
df[['Diagnóstico', 'Diagnóstico Codificado']]
```

```python
# Función para categorizar edades
def categorizar_edad(edad):
    if edad < 30:
        return '20-29 años'
    elif edad < 40:
        return '30-39 años'
    elif edad < 50:
        return '40-49 años'
    else:
        return '50+ años'

# Aplicar map con una función para transformar las edades
df['Grupo de Edad'] = df['Edad'].map(categorizar_edad)
df[['Paciente', 'Edad', 'Grupo de Edad']]
```

---

#### 🔄 Uso de `apply` en un dataframe:

La función `apply` se utiliza para aplicar una función a lo largo de los renglones o columnas de un Dataframes, permitiendo realizar operaciones más complejas y personalizadas en los datos.

- **Ejemplo de cálculo de costo por día hospitalizado:**

    ```python
    # Calcular el costo estimado del tratamiento por día hospitalizado
    df['Costo por Día'] = df.apply(lambda row: round(row['Costo del Tratamiento ($)'] / row['Días Hospitalizado'], 2), axis=1)
    df[['Paciente', 'Costo del Tratamiento ($)', 'Días Hospitalizado', 'Costo por Día']]
    ```

- **Ejemplo de ajuste de costo por días hospitalizados:**
    ```python
    # Ajustar el costo del tratamiento basado en el número de días hospitalizados
    def ajustar_costo(row):
        descuento = 100 * (row['Días Hospitalizado'] - 1)  # $100 descuento por cada día 'ADICIONAL', no por el primero.
        return row['Costo del Tratamiento ($)'] - descuento

    # Aplicar la función a lo largo de los renglones
    df['Costo Ajustado ($)'] = df.apply(ajustar_costo, axis=1)
    df[['Paciente', 'Días Hospitalizado', 'Costo del Tratamiento ($)', 'Costo Ajustado ($)']].head(10)
    ```

---

### 💡 **¿Sabías que...?**

- `apply()`:
Es notable por permitir la ejecución de funciones complejas y personalizadas en múltiples columnas de Dataframes, facilitando operaciones avanzadas como lógicas condicionales y manipulaciones de fechas, además de poder retornar múltiples valores nuevos desde una sola aplicación.

- `map()`:
Está optimizado para `Series`, siendo ideal para transformaciones eficientes utilizando diccionarios, otras Series o funciones, especialmente útil para codificaciones rápidas y conversión de datos categóricos con alineación automática de índices.

- `sort_values()`:
Permite un ordenamiento avanzado por múltiples columnas con criterios variables y la opción de aplicar transformaciones a datos antes del ordenamiento, además de manejar `NaNs`, mejorando la preparación de datos para análisis o visualización.

---

⬅️ [**Anterior**](../Readme.md)| [**Siguiente**](../Ejemplo-04/Readme.md) ➡️