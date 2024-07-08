🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 05**](../Readme.md) ➡️ / ⚡`Reto 01: Buscador de peliculas mas populares`

## 🎯 Objetivo

⚒️ Obtener información sobre las películas más populares usando la API de The Movie Database (TMDB), e imprimir el titulo, fecha de estreno y votación promedio de cada película.

---

## 📝 Instrucciones

👥 Considerando la cantidad de estudiantes, es posible resolver este reto en equipos o de manera individual.

1. 🔑 Solicita a tu Experto o Experta la API Key para acceder a los datos de la API The Movie Database (TMDB), en caso de no tenerla.

2. 🌐 Realiza una petición a la API de TMDB para obtener las películas populares.
   - URL base: `https://api.themoviedb.org/3/movie/popular?language=es-MX&page=1`

3. ⚙️ Configura los parámetros de la petición en un diccionario:
   - `language`: puede ser (`es-MX`).
   - `page`: puede ser 1.

4. 🔒 Configura los encabezados de la petición en un diccionario:
   - `Authorization`: usa el token de Bearer con tu API Key.
   - `accept`: especifica que esperas una respuesta en formato JSON.

5. 🔄 Obtén la respuesta e itera sobre los resultados obtenidos para cada película, imprime un mensaje similar:
   ```plaintext
   ✉️ Película 1: Título de la película, Fecha de estreno: (Fecha), Votación promedio: (Votación).
   ✉️ Película 2: Título de la película, Fecha de estreno: (Fecha), Votación promedio: (Votación).
   ...
   ```

> **📝 Nota:** Considera que las peliculas pueden cambiar con respecto a la fecha en que se realice el reto, por lo que los resultados pueden variar, sin embargo, el formato de impresión debe ser similar.

---

✅ **Desafío adicional**: Considera cómo podrías obtener la película con la mayor cantidad de votos.

---

🏆 Nos vemos en el siguiente reto, ¡mucho éxito!.

---

⬅️ [**Anterior**](../Readme.md) | [**Siguiente**](../Ejemplo-02/Readme.md) ➡️