🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 05**](../Readme.md) ➡️ / 📝 `Ejemplo 01: Interacción con APIs`

## 🎯 Objetivo

Implementar los métodos más populares para realizar peticiones HTTP, con el objetivo de manipular los recursos e información obtenidos a través de la web.

---

## 🚀 Comencemos

Una **API** (*Interfaz de Programación de Aplicaciones*) es un conjunto de reglas y protocolos que permite a diferentes programas comunicarse entre sí, actuando como un mensajero que lleva solicitudes (`request`) de un cliente a un servidor y devuelve respuestas (`response`), facilitando la integración y el funcionamiento de aplicaciones y servicios web.

---

### 📲🌐 **Principio básico de una API** 🧩📲

<div align="center">
    <img src="/Sesion-05/Imagenes/api2.jpg" alt="API" width="800" height="400">
</div>

---

### 🌐 **Conceptos clave:**

- **URL**: 🌍 La "dirección" a donde vamos a realizar nuestra petición.
- **Verbo HTTP**: 📋 El tipo de acción que vamos a realizar (i.e. GET, POST, PUT, PATCH, DELETE, etc.).
- **Parámetros**: 📝 Valores que agregamos a nuestra petición para enviar información relevante a la API (datos de acceso, filtros, etc.).
- **Estatus de la respuesta**: 📊 Un código que dice si nuestra petición fue realizada exitosamente o no (i.e. 200, 201, 400, 404, 500, etc.).
- **Cuerpo de la respuesta**: 📦 Los datos que fueron enviados de regreso al finalizar la petición.

---

### 🧰 **Estatus de la respuesta HTTP:**

| Código | Nombre                          | Descripción                                           |
|--------|---------------------------------|-------------------------------------------------------|
| **`200`**  | ✅ OK                           | Solicitud exitosa, servidor devolvió la respuesta.     |
| **`201`**  | 🆕 Created                      | Solicitud exitosa, nuevo recurso creado.               |
| **`400`**  | ❌ Bad Request                  | Solicitud incorrecta o mal formada.                    |
| **`401`**  | 🔒 Unauthorized                 | Autenticación requerida.                               |
| **`403`**  | 🚫 Forbidden                    | Solicitud entendida, pero no autorizada.               |
| **`404`**  | 🔍 Not Found                    | Recurso solicitado no encontrado.                      |
| **`500`**  | 💥 Internal Server Error        | Error en el servidor.                                  |
| **`502`**  | 🛑 Bad Gateway                  | Solicitud inválida recibida por el servidor.           |
| **`503`**  | ⚙️ Service Unavailable          | Servidor no disponible temporalmente.                  |
| **`504`**  | ⏳ Gateway Timeout              | El servidor demoró demasiado en responder.             |

---

### 🔦 **Verbos HTTP:**

| Verbo  | Nombre       | Descripción                                           |
|--------|--------------|-------------------------------------------------------|
| **`GET`**  | 📥 Obtener   | Solicita y devuelve datos del servidor.               |
| **`POST`** | 📤 Enviar    | Envía datos para crear un nuevo recurso.               |
| **`PUT`**  | 🔄 Actualizar| Actualiza un recurso existente o crea uno nuevo.       |
| **`DELETE`**| 🗑️ Eliminar | Elimina un recurso especificado.                      |
| **`PATCH`**| 🛠️ Parche    | Aplica modificaciones parciales a un recurso.         |
| **`HEAD`** | 🧠 Cabecera    | Solicita cabeceras sin el cuerpo de la respuesta.      |
| **`OPTIONS`**| ❓ Opciones| Describe opciones de comunicación del recurso.         |
| **`CONNECT`**| 🔌 Conectar| Establece un túnel hacia el servidor.                  |
| **`TRACE`** | 📝 Trazar   | Prueba de bucle de retorno de mensaje.                 |

---

## 🛠️ **Ejemplo: Interacción con APIs**

Para este ejercicio vamos a utilizar la API de [The Movie Data Base](https://www.themoviedb.org/), un servicio gratuito que nos permite realizar peticiones HTTP y obtener información sobre películas, series, actores, etc.

Tambien usaremos la libreria de [requests](https://docs.python-requests.org/en/master/) para realizar las peticiones HTTP.

1. **Registro en The Movie Data Base:**

    - Para poder utilizar la API de The Movie Data Base, es necesario registrarse.
    - Una vez registrado, debemos solicitar una API Key, la cual nos permitirá realizar peticiones a la API.

2. **Instalación requests:**

    - Para realizar peticiones HTTP en Python, vamos a utilizar la librería `requests`.
    - Para instalarla, ejecutamos el siguiente comando en la terminal:

        ```bash
        # Si usamos Google Colab
        !pip install requests
        ```

3. **Ejemplo de petición GET:**

    - Vamos a realizar una petición GET a la API de The Movie Data Base para obtener información sobre una película en específico.
    - Para ello, necesitamos la URL base de la API y la API Key que obtuvimos al registrarnos.

    ```python
    import requests

    # Pidele a tu Experto o Experta la API Key, en caso de no tenerla.
    api_key = "YOUR API KEY"

    # Parámetros de la petición
    query = "Ready Player One" # Película a buscar
    include_adult = False # Incluir contenido para adultos
    language = "es-MX" # Lenguaje de la respuesta
    page = 1 # Cantidad de páginas

    # URL base de la API
    base_url = "https://api.themoviedb.org/3/search/movie"

    # Parámetros
    params = {
        'query': query,
        'include_adult': str(include_adult).lower(),
        'language': language,
        'page': page
    }

    # Encabezados de la petición
    headers = {
        'Authorization': 'Bearer ' + api_key,
        'accept': 'application/json'
    }

    # Realizar la petición GET
    response = requests.get(base_url, headers=headers, params=params)

    # Imprimir la respuesta en texto plano.
    print(response.text)
    ```

    - De esta manera, podemos acceder a la información de la película y manipularla según sea necesario.

Al realizar una petición GET a la API de The Movie Data Base, obtendremos un JSON con la información de la película "Ready Player One", algo similar a lo siguiente:

<!-- Json object -->

```json
{
    "page": 1,
    "results": [
        {
            "adult": false,
            "backdrop_path": "/xFYpUmB01nswPgbzi8EOCT1ZYFu.jpg",
            "genre_ids": [12, 28, 18],
            "id": 980489,
            "original_language": "en",
            "original_title": "Gran Turismo",
            "overview": "Basada en una historia real, la película cuenta cómo cumplió su sueño un adolescente que jugaba a Gran Turismo, juego en el que ganó una serie de competiciones patrocinadas por Nissan, y que le sirvió de trampolín para acabar convirtiéndose en un piloto de carreras profesional.",
            "popularity": 135.225,
            "poster_path": "/tVj5dn15iwkMhjU2wIih1yMy5LK.jpg",
            "release_date": "2023-08-09",
            "title": "Gran Turismo: De jugador a corredor",
            "video": false,
            "vote_average": 7.842,
            "vote_count": 2405
        },
    ],
    "total_pages": 1,
    "total_results": 3
}
```

<!-- Conclusion -->

Con esto, hemos realizado una petición GET a la API de The Movie Data Base y obtenido información sobre la película "Ready Player One", puedes probar con otras películas y explorar la información que obtienes, e incluso puede usar ciclos para obtener información de varias películas a la vez.

---

### 💡 **Sabías que...**

La librería **requests** fue creada por Kenneth Reitz para simplificar las peticiones HTTP en Python y se ha convertido en un estándar, con más de mil millones de descargas. En ciencia de datos, es crucial para recolectar datos de APIs, permitiendo análisis en tiempo real y modelos predictivos que revolucionan sectores como tecnología, salud y finanzas. Por ejemplo, se utiliza en fintech para desarrollar algoritmos de trading automatizado que toman decisiones en fracciones de segundo.

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Reto-01/Readme.md) ➡️
