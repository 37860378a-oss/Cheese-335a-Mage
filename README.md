# Cheese 3.3.5a — todas las clases, niveles 1–80

**Estado: primera adaptación experimental. Requiere pruebas dentro del juego.**

Adaptación comunitaria de Cheese para World of Warcraft 3.3.5a. El objetivo es conservar el soporte multiclase del addon original y permitir que sus alertas funcionen durante el leveo, desde nivel 1 hasta 80.

## Cambios experimentales de esta versión

- Se conserva la identificación por ID como método principal.
- Se agrega una búsqueda por nombre localizado como respaldo cuando el cliente no devuelve un ID utilizable.
- Se agrega un refresco del escaneo de la barra de acción al cambiar hechizos, subir de nivel o cambiar de página de acción.
- Se aplica el mismo resolvedor a los botones de acción para que el brillo y el escaneo utilicen la misma identificación.
- Se conserva el mapa general de clases y las texturas originales.

## Importante

Esta es una primera build experimental, no una versión certificada. No se ha probado todavía con personajes de todas las clases y niveles. El reconocimiento por nombre no sustituye los IDs: dos rangos o hechizos pueden compartir nombre, y los nombres dependen del idioma del cliente. Por eso, el código prioriza el ID válido y usa el nombre solamente como respaldo.

El TOC conserva `Interface: 30300`, que corresponde al cliente 3.3.5. La descripción original "Cataclysm Visual Alerts" era texto informativo, no prueba de que el addon requiera Cataclysm.

## Instalación para pruebas

1. Cerrá el juego.
2. Hacé una copia de tu carpeta actual `Interface/AddOns/Cheese`.
3. Extraé la carpeta `Cheese` de este ZIP en `World of Warcraft/Interface/AddOns/`.
4. Iniciá el cliente y activá Cheese en la lista de addons.
5. Probá primero un personaje de nivel bajo con un proc que esté contemplado en los mapas del addon.

Si aparece un error Lua, copiá el mensaje completo. Indicá clase, nivel, idioma del cliente y qué hechizo/proc estabas probando.

## Alcance pendiente

La actualización de detección no incorpora automáticamente todos los procs de todas las clases. Los IDs y nombres presentes en los mapas originales todavía deben contrastarse con los hechizos de Wrath 3.3.5a. La compatibilidad real del conjunto completo requiere pruebas en cliente.

## Créditos

- Addon original: Cheese. Los autores originales y la licencia deben verificarse en la distribución de origen.
- Adaptación experimental multiclase para WoW 3.3.5a: **By Charls**.
- Mantenimiento de esta adaptación: **Charls**.
