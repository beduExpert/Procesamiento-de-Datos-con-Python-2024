🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 05**](../Readme.md) ➡️ / 📝 `Ejemplo 01: Interacción con APIs`

## 🎯 Objetivo

Implementar los métodos más populares para realizar peticiones HTTP, con el objetivo de manipular los recursos e información obtenidos a través de la web.

---

## 🚀 Introducción

Una **API** (*Interfaz de Programación de Aplicaciones*) es un conjunto de reglas y protocolos que permite a diferentes programas comunicarse entre sí, actuando como un mensajero que lleva solicitudes (`request`) de un cliente a un servidor y devuelve respuestas (`response`), facilitando la integración y el funcionamiento de aplicaciones y servicios web.

---



### 📲🌐 **Principio básico de una API** 🧩📲


<div align="center">
    <img src="/Sesion-05/Imagenes/api.jpg" alt="API" width="400" height="400">
    <!-- <img src="/Sesion-05/Imagenes/api2.jpg" alt="API" width="600" height="400"> -->
</div>

---


### 🧰 **Códigos de estado HTTP:**

🌐 Los códigos de estado HTTP indican el resultado de una solicitud que se realizó a un servidor.

| Código | Nombre                          | Descripción                                                                                      |
|--------|---------------------------------|--------------------------------------------------------------------------------------------------|
| **`200`**  | ✅ OK                           | La solicitud fue exitosa y el servidor devolvió la respuesta solicitada.                         |
| **`201`**  | 🆕 Created                      | La solicitud fue exitosa y se creó un nuevo recurso.                                             |
| **`400`**  | ❌ Bad Request                  | La solicitud es incorrecta o mal formada.                                                        |
| **`401`**  | 🔒 Unauthorized                 | La solicitud requiere autenticación.                                                             |
| **`403`**  | 🚫 Forbidden                    | El servidor entendió la solicitud, pero se niega a autorizarla.                                  |
| **`404`**  | 🔍 Not Found                    | El servidor no encontró el recurso solicitado.                                                   |
| **`500`**  | 💥 Internal Server Error        | El servidor encontró un error y no pudo completar la solicitud.                                  |
| **`502`**  | 🛑 Bad Gateway                  | El servidor recibió una solicitud inválida.                                                      |
| **`503`**  | ⚙️ Service Unavailable          | El servidor no está disponible temporalmente, generalmente por mantenimiento.                    |
| **`504`**  | ⏳ Gateway Timeout              | El servidor demoro demasiado en la respuesta.                                                    |

---

### 🔦 **Verbos HTTP:**

🌐 Los verbos HTTP indican las acciones que se realizarán a un determinado recurso.

| Verbo  | Nombre       | Descripción                                                                                      |
|--------|--------------|--------------------------------------------------------------------------------------------------|
| **`GET`**  | 📥 Obtener   | Solicita un recurso del servidor y devuelve datos sin alterar el estado del recurso.              |
| **`POST`** | 📤 Enviar    | Envía datos al servidor para crear un nuevo recurso.                                              |
| **`PUT`**  | 🔄 Actualizar| Envía datos al servidor para actualizar un recurso existente o crear uno nuevo si no existe.      |
| **`DELETE`**| 🗑️ Eliminar | Elimina un recurso especificado del servidor.                                                     |
| **`PATCH`**| 🛠️ Parche    | Aplica modificaciones parciales a un recurso existente.                                           |
| **`HEAD`** | 🧠 Cabeza    | Solicita las cabeceras de respuesta idénticas a una solicitud GET, pero sin el cuerpo de la respuesta.|
| **`OPTIONS`**| ❓ Opciones| Describe las opciones de comunicación para el recurso de destino.                                  |
| **`CONNECT`**| 🔌 Conectar| Establece un túnel hacia el servidor identificado por el recurso.                                  |
| **`TRACE`** | 📝 Trazar   | Realiza una prueba de bucle de retorno de mensaje a lo largo de la ruta hasta el recurso de destino.|


---

<!-- Ejemplo-->

## 🛠️ **Ejemplo: Interacción con APIs**



---

### 💡 **Sabías que...**


---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Reto-01/Readme.md) ➡️