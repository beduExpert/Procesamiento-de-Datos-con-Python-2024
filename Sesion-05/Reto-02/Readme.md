🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 05**](../Readme.md) ➡️ / ⚡`Reto 02: Mysql_tienda y MongoDB_users`

## 🎯 Objetivo

⚒️ Desarrollar dos conexiones a bases de datos, una en MySQL y otra en MongoDB, para realizar operaciones básicas de consulta e impresión de resultados.

---

## 📝 Instrucciones

👥 Considerando la cantidad de estudiantes, es posible resolver este reto en equipos o de manera individual.

### Parte 1: MySQL

1. 🔑 Asegúrate de tener las credenciales y la información necesaria para conectarte a la base de datos MySQL de BEDU (host, usuario, contraseña, base de datos).

2. 🖥️ Crear una conexión a la base de datos **`tienda`**.

3. 🛠️ Crear un cursor para ejecutar consultas.

4. ⚙️ Ejecutar una consulta SQL para obtener la siguiente información de la tabla `Pedidos`:
    - `Obtener las columnas`: user_id y la suma de total_pedidos.
    - `Utiliza la tabla`: `Pedidos`.
    - `Agrupa por`: `user_id`.
    - `Agrega una condición`: `total_pedidos mayor que 1500`.
    - `Ordena por`: `total_pedidos` de forma `descendente`.

5. 🔄 Obtener los resultados de la consulta.

6. 📄 Mostrar los resultados, e imprime un mensaje similar:
   ```plaintext
   ✉️ Usuario ID: 6072, Total Pedido: $2,349.86.
   ✉️ Usuario ID: 9748, Total Pedido: $2,079.81.
   ```

### Parte 2: MongoDB

1. 🔑 Asegúrate de tener las credenciales y la información necesaria para conectarte a tu base de datos MongoDB (URI de conexión).

2. 🖥️ Crear una conexión a la base de datos **`sample_mflix`**.

3. 🛠️ Utiliza la coleccion de `users`, para obtener los documentos.

4. ⚙️ Realizar una consulta, para la siguientes información:
    - `Obtener los documentos`: que en el campo `email` contengan la palabra `@gameofthron.es`.
    - `Proyectar`: `name` y `email` solamente.
    - `Limitar`: a 10 documentos.

5. 🔄 Obtener los resultados de la consulta.

6. 📄 Mostrar los resultados, e imprime un mensaje similar:
   ```plaintext
   ✉️ Nombre: Petyr Baelish, Email: aidan_gillen@gameofthron.es.
   ✉️ Nombre: Theon Greyjoy, Email: alfie_allen@gameofthron.es.
   ```
---

📌 **Nota**:
   - Asegúrate de tener instalados los paquetes necesarios (`mysql-connector-python` para MySQL y `pymongo` para MongoDB).
   ```plaintext
   !pip install mysql-connector-python
   !pip install pymongo
   ```
   - Los nombres de host, usuario, contraseña, base de datos y colecciones deben ser reemplazados por la información específica que proporcione tu experto o experta.

---

🏆 Nos vemos en el siguiente reto, ¡mucho éxito!.

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Ejemplo-02/Readme.md) ➡️