🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 08**](../Readme.md) ➡️ / 📝 `Ejemplo 04: Combinación y agrupación de datos`

## 🎯 Objetivo

Aprender a combinar y agrupar dataframes en Pandas para unificar datos de múltiples fuentes y realizar análisis estadísticos complejos mediante técnicas de `merge` y `groupby`.

---

## 🚀 Comencemos

Combinar y agrupar son técnicas fundamentales en el análisis de datos que facilitan la integración de información de diversas fuentes y la realización de análisis detallados sobre subconjuntos específicos de datos.

---

## 🛠️ **Técnicas de combinación y agrupación en dataframes** 🛠️

### 🧠 **Creación de dataframes generales:**

```python
import pandas as pd

# DataFrame de Clientes
clientes = pd.DataFrame({
    'cliente_id': [101, 102, 103, 104],
    'nombre': ['Alice Johnson', 'Bob Smith', 'Charlie Davis', 'Diana Prince'],
    'email': ['alice@example.com', 'bob@example.com', 'charlie@example.com', 'diana@example.com'],
    'región': ['Norte', 'Sur', 'Este', 'Oeste']
})
clientes.head()
```

```python
# DataFrame de Pedidos
pedidos = pd.DataFrame({
    'pedido_id': ['P001', 'P002', 'P003', 'P004', 'P005', 'P006'],
    'cliente_id': [101, 103, 105, 104, 101, 102],  # Incluye IDs que no existen y repeticiones
    'total': [250, 150, 450, 300, 320, 110],
    'fecha': ['2021-01-10', '2021-02-15', '2021-03-20', '2021-04-22', '2021-05-25', '2021-06-15'],
    'categoría': ['Electrónica', 'Ropa', 'Electrónica', 'Libros', 'Alimentos', 'Ropa']
})
pedidos.head(10)
```
---

### 🆎 **Merge de dataframes** 🔄

La función `merge` en Pandas permite combinar dos o más DataFrames en función de una o más claves comunes, similar a un `JOIN` en SQL.

<div align="center">
    <img src="/Sesion-08/Imagenes/JOIN.jpg" alt="API" width="300" height="200">
</div>

### 🔦 **Ejemplos de uso de inner, left y right join:**

```python
# Inner Join
df_inner = pd.merge(clientes, pedidos, on='cliente_id', how='inner')
df_inner.head(10)
```

```python
# Left Join
df_left = pd.merge(clientes, pedidos, on='cliente_id', how='left')
df_left.head(10)
```

```python
# Right Join
df_right = pd.merge(clientes, pedidos, on='cliente_id', how='right')
df_right.head(10)
```

### Parámetros de `merge`

| Parámetro    | Descripción                                                                                                             |
|--------------|-------------------------------------------------------------------------------------------------------------------------|
| `on`         | Nombre de la columna o lista de nombres de columnas para unir las tablas. Las columnas deben existir en ambos DataFrames.|
| `how`        | Tipo de merge/join: 'left', 'right', 'outer', 'inner'. Por defecto es 'inner'.                                          |
| `left_on`    | Columnas del DataFrame izquierdo para hacer el join si los nombres de las columnas en ambos DataFrames no coinciden.    |
| `right_on`   | Columnas del DataFrame derecho para hacer el join si los nombres de las columnas en ambos DataFrames no coinciden.      |
| `left_index` | Si es `True`, usa el índice (filas) del DataFrame izquierdo como su clave de join. Por defecto es `False`.              |
| `right_index`| Si es `True`, usa el índice (filas) del DataFrame derecho como su clave de join. Por defecto es `False`.                |
| `suffixes`   | Una tupla de strings para añadir a los nombres de columnas duplicadas que no son claves de join. Por defecto es `('_x', '_y')`. |


---

### 📊 **Agrupación de datos con `groupby`**

La función `groupby` en Pandas permite agrupar datos en un DataFrame en función de una o más columnas, permitiendo realizar operaciones estadísticas y de agregación en los grupos resultantes.

Algunas funciones de agregación comunes incluyen `sum`, `mean`, `count`, `min`, `max`, `std`, `var`, entre otras.

<div align="center">
    <img src="/Sesion-08/Imagenes/groupby.png" alt="API" width="700" height="200">
</div>

### 🔦 **Ejemplos de uso de groupby:**

```python
# Realizamos un left join para obtener un DataFrame completo
df_merged = pd.merge(clientes, pedidos, on='cliente_id', how='left')
df_merged.head(10)
```

```python
# Ejemplo 1: Total de Pedidos por Región
total_por_región = df_merged.groupby('región')['total'].sum()
print(total_por_región)

# Ejemplo 2: Número de Pedidos por Categoría y Región
conteo_pedidos_categoría = df_merged.groupby(['región', 'categoría'])['pedido_id'].count()
print(conteo_pedidos_categoría)

# Ejemplo 3: Promedio del Total de Pedidos por Mes
# Convertir 'fecha' a datetime
df_merged['fecha'] = pd.to_datetime(df_merged['fecha'])

# Extraer el mes y año de la fecha
df_merged['mes_año'] = df_merged['fecha'].dt.to_period('M')

# Calcular el promedio de ventas por mes
promedio_ventas_mes = df_merged.groupby('mes_año')['total'].mean()
print(promedio_ventas_mes)
```


---

### 💡 **¿Sabías que...?**

- **`merge`** puede ser utilizado no solo para combinar dos DataFrames basados en claves coincidentes, sino también para realizar left, right, y outer joins, proporcionando una flexibilidad comparable a las bases de datos relacionales.
- **`groupby`** no solo es útil para sumar o promediar datos, sino que también puede ser utilizado para aplicar una multitud de funciones estadísticas, transformaciones personalizadas y filtrados complejos dentro de los grupos.

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Reto-02/Readme.md) ➡️