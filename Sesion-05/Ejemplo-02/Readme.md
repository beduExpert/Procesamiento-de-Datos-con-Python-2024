🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 05**](../Readme.md) ➡️ / 📝 `Ejemplo 02: Base de datos MySQL y MongoDB`

## 🎯 Objetivo

Implementar métodos populares para interactuar y obtener información tanto de bases de datos relacionales como MySQL (fetchone, fetchmany, fetchall) como de bases de datos NoSQL como MongoDB (find_one, find, cursores).

---

## 🚀 Comencemos

Las bases de datos son una parte fundamental en el desarrollo de aplicaciones, ya que permiten almacenar y recuperar información de manera rapida. Existen diferentes tipos de bases de datos, entre las más populares se encuentran las bases de datos relacionales y las bases de datos NoSQL, cada una con sus propias características y ventajas.

En Python, existen librerías que permiten interactuar con diferentes tipos de bases de datos, como `mysql-connector-python` para MySQL y `pymongo` para MongoDB, con la finalidad de poder ejecutar consultas desde Python y obtener información de manera programática.

---


#### 🗃️ **MySQL**:

Para interactuar con una base de datos MySQL desde Python, es necesario instalar el conector `mysql-connector-python`. Se puede utilizar el siguiente comando:

```bash
# Si usas Google Colab, ejecuta esta celda
!pip install mysql-connector-python
```

Si requieres conocer más acerca de como interactuar con una base de datos MySQL desde Python, puedes consultar la documentación oficial de MySQL [aquí](https://dev.mysql.com/doc/connector-python/en/).

Tambien puedes consultar la documentación de `W3Schools` para obtener más información y ejemplos [aquí](https://www.w3schools.com/python/python_mysql_getstarted.asp).



📌 **Procedimiento para hacer una consulta**:


```python
import mysql.connector

# Crear una conexión a la base de datos.
mydb = mysql.connector.connect(
    host="localhost",
    user="root",
    password="password",
    database="mydatabase"
) # Pidele a tu Experto o Experta que te proporcione los datos de conexión.

# Crear un cursor para ejecutar consultas.
mycursor = mydb.cursor()

# Ejecutar una consulta.
mycursor.execute("SELECT * FROM Usuarios")

# Obtener los resultados de la consulta.
myresult = mycursor.fetchall()

# Mostrar los resultados.
for resultado in myresult:
    print(resultado)
```

---

#### 📦 **MongoDB**:

Para interactuar con una base de datos MongoDB desde Python, es necesario instalar la librería `pymongo`. Se puede utilizar el siguiente comando:

```bash
# Si usas Google Colab, ejecuta esta celda
!pip install pymongo
```

Si requieres conocer más acerca de como interactuar con una base de datos MongoDB desde Python, puedes consultar la documentación oficial de MongoDB [aquí](https://pymongo.readthedocs.io/en/stable/).

Tambien puedes consultar la documentación de `W3Schools` para obtener más información y ejemplos [aquí](https://www.w3schools.com/python/python_mongodb_getstarted.asp).

📌 **Procedimiento para hacer una consulta**:

```python
import pymongo

# Crear una conexión a la base de datos.
myclient = pymongo.MongoClient("mongodb://localhost:27017/")
mydb = myclient["mydatabase"]

# Pidele a tu Experto o Experta que te proporcione los datos de conexión.

# Obtener una colección.
mycol = mydb["Usuarios"]

# Realizar una consulta.
myquery = { "name": "John" }
mydoc = mycol.find(myquery)

# Mostrar los resultados.
for resultado in mydoc:
    print(resultado)
```
---



### 💡 **Sabías que...**


**MySQL**:
- `mysql-connector-python` es un conector oficial de MySQL para Python, lo que significa que es desarrollado y mantenido por Oracle. Una de sus ventajas es que proporciona soporte completo para las características avanzadas de MySQL, como el manejo de transacciones y la compatibilidad con los últimos estándares SQL. Además, incluye soporte para autenticación mediante plugins y conexiones SSL, lo que lo hace ideal para aplicaciones que requieren altos niveles de seguridad.

**MongoDB**:
- `pymongo` es una de las bibliotecas más utilizadas para interactuar con MongoDB desde Python. Una de sus características destacadas es el soporte para operaciones de agregación, que permiten realizar consultas complejas y análisis de datos directamente en la base de datos, utilizando el pipeline de agregación de MongoDB. Esto permite a los desarrolladores realizar transformaciones y agregaciones de datos directamente en el servidor de la base de datos, reduciendo la necesidad de procesamiento adicional en la aplicación y mejorando el rendimiento general.


---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Reto-02/Readme.md) ➡️
