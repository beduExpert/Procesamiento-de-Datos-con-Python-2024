🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 06**](../Readme.md) ➡️ / 📝 `Ejemplo 04: Manipulación de columnas`

## 🎯 Objetivo

Implementar técnicas en Pandas para gestionar columnas en `DataFrames`, incluyendo añadir, reasignar y eliminar, facilitando análisis más detallados en Python.

---

## 🚀 Comencemos

La manipulación de columnas es crucial durante la etapa de preparación de datos, que es fundamental en cualquier proyecto de data science. Esto incluye limpiar los datos, transformarlos para análisis y asegurarse de que el formato de los datos sea el adecuado para las herramientas y técnicas de análisis posteriores.

---

## ➕🔄❌ Añadir, reasignar y eliminar columnas en un DataFrame

### Añadir una nueva columna:

Agrega una nueva columna al `DataFrame` asignando una Serie o arreglo de valores con un nombre específico.

```python
import pandas as pd

# Diccionario datos de ejemplo
datos = {
   "ID": [101, 102, 103, 104, 105], 
   "Nombre": ["Ana", "Luis", "Marta", "Juan", "Sofía"], 
   "Departamento": ["Finanzas", "Marketing", "TI", "Recursos Humanos", "Operaciones"], 
   "Salario": [45000, 38000, 62000, 41000, 36000]
   }

# Crear DataFrame
df = pd.DataFrame(datos)

# Añadir columna "Edad"
df["Edad"] = [25, 30, 28, 35, 32]
print(df)
```

### Reasignar una columna:

Modifica una columna existente asignando nuevos valores.

```python

# Reasigna nuevos valores a la columna "Salario"
df["Salario"] = [47000, 40000, 64000, 43000, 37000]
print(df)
```

### Eliminar una columna:

<!-- Creamos una columna adicional para eliminarla posteriormente. -->

```python
# Añadir columna "Tiempo"
df["Tiempo"] = [2, 3, 4, 5, 6]
print(df)
```


Utiliza `.drop()` para eliminar columnas por nombre o índice.

```python
df = df.drop(columns=["Tiempo"])
print(df)
```

Utilizando `axis` y `errors="ignore"` para manejo seguro de errores.

```python
df = df.drop("Tiempo", axis=1, errors="ignore")
print(df)
```

---

### 💡 **¿Sabías que...?**

Aunque el método `.drop()` es muy útil para eliminar columnas, Pandas también ofrece métodos poderosos para modificar `DataFrames` sin necesidad de eliminar y recrear columnas. Un ejemplo es el método `.assign()`, que permite añadir nuevas columnas a un `DataFrame` o modificar existentes de manera funcional (sin modificar el `DataFrame` original). Este método es especialmente útil para crear columnas derivadas mientras se mantiene el `DataFrame` original intacto para otras operaciones.

**Ejemplo de Uso de `.assign()`:**

Supongamos que queremos añadir una columna que represente un bono del 10% sobre el salario actual de los empleados, pero sin alterar la columna de salario original. Podemos hacerlo fácilmente con `.assign()`:

```python
import pandas as pd

# Diccionario de datos de ejemplo
datos = {
    "ID": [101, 102, 103, 104, 105],
    "Nombre": ["Ana", "Luis", "Marta", "Juan", "Sofía"],
    "Departamento": ["Finanzas", "Marketing", "TI", "Recursos Humanos", "Operaciones"],
    "Salario": [45000, 38000, 62000, 41000, 36000]
}

# Crear DataFrame
df = pd.DataFrame(datos)

# Usar .assign() para añadir una columna de "Bono"
df_con_bono = df.assign(Bono=lambda x: x['Salario'] * 0.1)
print(df_con_bono)
```

**Salida:**

```
    ID Nombre      Departamento  Salario   Bono
0  101    Ana          Finanzas    45000  4500.0
1  102   Luis         Marketing    38000  3800.0
2  103  Marta                TI    62000  6200.0
3  104   Juan  Recursos Humanos    41000  4100.0
4  105  Sofía       Operaciones    36000  3600.0
```

Este enfoque no solo es limpio y eficiente sino que también promueve la inmutabilidad de los datos, un concepto importante en muchas prácticas de programación moderna y análisis de datos.


---


⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Reto-02/Readme.md) ➡️
