🏠 [**Inicio**](../../Readme.md) ➡️ / 📖 [**Sesión 02**](../Readme.md) ➡️ / ⚡`Reto 02: Pedido a domicilio`


## 🎯 Objetivo

⚒️ Resolver una actividad, con el fin de practicar el uso de ciclos de repetición, para obtener el valor total sobre una orden de comida a domicilio, así como las peticiones necesarias por consola.

---

## 📝 Instrucciones

👥 Este reto se puede realizar tanto individualmente como en equipos.

1. 🗣️ Inicializa una variable `pedido_total`, que servirá para acumular el costo total del pedido.

2. ⌨️ Implementa un bucle `while` que muestre un menú de opciones de comida y permita al usuario hacer un pedido. Las opciones son:
   - 1. Pizza - $10
   - 2. Hamburguesa - $8
   - 3. Ensalada - $7
   - 0. Finalizar pedido

3. 🔄 Dentro del bucle, solicita al usuario que ingrese el número de la opción deseada y realiza las siguientes acciones según la elección:
   - Si el usuario selecciona '0', muestra el total del pedido, agradece y termina el bucle.
   - Utiliza una estructura `match` para asignar el precio correcto según la opción elegida y añadirlo al `pedido_total`.

4. ❓ Si el usuario introduce una opción no válida, muestra un mensaje de error y permite intentar nuevamente sin salir del bucle.

5. 🧮 Después de añadir cada producto al pedido, muestra un mensaje indicando el producto añadido y el total acumulado. Luego, pregunta al usuario si desea continuar añadiendo productos. Si responde "no", muestra el total del pedido, agradece y finaliza el bucle.

---

✅ **Desafío adicional**: Implementa una opción en el menú que le permita al usuario ver el total de su pedido en cualquier momento antes de finalizar.

---

🏆 Nos vemos en el siguiente reto, ¡mucho éxito!.

---

⬅️ [`Anterior`](../Readme.md) | [`Siguiente`](../../Sesion-03/Readme.md) ➡️