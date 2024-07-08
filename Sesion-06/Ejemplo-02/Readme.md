🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 06**](../Readme.md) ➡️ / 📝 `Ejemplo 02: Métodos avanzados de indexación`

## 🎯 Objetivo

Aplicar las diferentes técnicas de indexación en Pandas para seleccionar y filtrar información en una Serie, utilizando métodos avanzados para operaciones complejas y específicas.

---

## 🚀 Comencemos

En Python y Pandas, la manipulación de datos de Series se puede realizar por posición, etiqueta, lo que facilita una selección precisa de datos para análisis y extracción de subconjuntos relevantes.

---

### 🔍 **Accediendo a elementos**

Explora cómo acceder a datos en una Serie de forma precisa usando `.loc` y `.iloc`:

<!-- Declaramos una serie de 10 datos -->

```python
import pandas as pd

data = pd.Series([10, 20, 30, 40, 50], index=['a', 'b', 'c', 'd', 'e'])
```

- **Por posición con `.iloc`:** Accede a elementos por su posición numérica.
  ```python
  data.iloc[0]  # Accede al primer elemento
  ```
  
- **Por etiqueta con `.loc`:** Utiliza etiquetas de índice para acceder a los elementos.
  ```python
  data.loc['a']  # Accede al elemento con índice 'a'
  ```
  
- **Por rango con ambos métodos:** Accede a rangos de datos.
  ```python
  data.iloc[1:3]  # Elementos en posiciones 1 y 2
  ```
  
- **Por conjunto de elementos:** Selecciona múltiples ítems específicos.
  ```python
  data.loc[['a', 'b', 'c']]  # Elementos con índices 'a', 'b', y 'c'
  ```

> **📝 Nota:** 
>
>Es importante diferenciar entre `.iloc` y `.loc`, ambos métodos pueden ser utilizados para acceder a elementos por posición o etiqueta. Sin embargo, `.iloc` se enfoca en la posición numérica de los elementos, mientras que `.loc` se enfoca en las etiquetas de índice.
>
>Asi mismo al involucrar dobles corchetes `[[ ]]` en la selección de elementos, se está creando una lista de elementos, lo cual es diferente a seleccionar un solo elemento.

---

### 📚 **Ejemplos prácticos**

Recuerda que es necesario importar la librería de Pandas para trabajar con Series y DataFrames:

```python
import pandas as pd
```

1. **Gestión de inventarios:**
   ```python
   inventario = pd.Series([300, 200, 150], index=['tornillos', 'tuercas', 'clavos'])

   # Selecciona inventario de tornillos y clavos
   seleccion = inventario.loc[['tornillos', 'clavos']]

   print(seleccion)
   # Salida:
   # tornillos    300
   # clavos       150
   # dtype: int64
   ```

2. **Control de calidad:**
   ```python
   mediciones = pd.Series([0.330, 0.335, 0.329], index=[1, 2, 3])

   # Acceder a la segunda medición usando .iloc
   segunda_medicion = mediciones.iloc[1]

   print(segunda_medicion)
   # Salida: 0.335
   ```

3. **Investigación científica:**
   ```python
   temperaturas = pd.Series([22.5, 23.1, 22.8], index=['9AM', '12PM', '3PM'])

   # Acceder a la temperatura a mediodía
   temp_mediodia = temperaturas.loc['12PM']

   print(temp_mediodia)
   # Salida: 23.1
   ```

4. **Seguimiento de pacientes en un hospital:**
   ```python
   niveles_glucosa = pd.Series([90, 140, 130], index=['Paciente 1', 'Paciente 2', 'Paciente 3'])

   # Obtener niveles de glucosa de Paciente 2
   glucosa_p2 = niveles_glucosa.loc['Paciente 2']

   print(glucosa_p2)
   # Salida: 140
   ```

5. **Análisis de ventas:**
   ```python
   ventas = pd.Series([1000, 1500, 1200], index=['Enero', 'Febrero', 'Marzo'])

   # Seleccionar ventas de Enero y Marzo
   ventas_em = ventas.loc[['Enero', 'Marzo']]

   print(ventas_em)
   # Salida:
   # Enero    1000
   # Marzo    1200
   # dtype: int64
   ```


<!-- Conclusión -->

De esta forma podemos extraer información específica de una Serie en Pandas, utilizando métodos de indexación para seleccionar y filtrar datos de forma precisa y personalizada.

---

### 💡 **¿Sabías que...?**

🔗 **Encadenamiento de métodos**: Pandas está promoviendo el encadenamiento de métodos, lo que permite realizar múltiples operaciones en una sola línea. Esto mejora tanto la legibilidad como la eficiencia en la ejecución de los programas.

🔄 **Eliminación de `inplace`**: Se planea eliminar el parámetro `inplace` para simplificar el código y porque no funciona dentro de cadenas de métodos. Este cambio busca hacer la interfaz más intuitiva.

🚀 **Integración con apache arrow**: Pandas podría adoptar Apache Arrow como backend, lo que permitiría un manejo más eficiente de grandes volúmenes de datos y mejoraría el rendimiento general de las operaciones.

🛠️ **Arrays de extensión**: La introducción de 'Extension Arrays' permite crear tipos de datos personalizados, facilitando la adaptación de Pandas a necesidades específicas de análisis de datos.

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Reto-01/Readme.md) ➡️