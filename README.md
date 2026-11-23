# Cheese 3.3.5a — Mago del nivel 1 al 80

**Estado del proyecto: adaptación en desarrollo. Todavía no es una versión probada.**

Proyecto comunitario para adaptar el addon de alertas visuales de activación de hechizos Cheese a **World of Warcraft 3.3.5a**, con enfoque en la clase **Mago**, desde el nivel **1 hasta el 80**.

## Objetivos

- Dar soporte a personajes Mago durante todo el leveo, del nivel 1 al 80.
- Detectar los hechizos y talentos que el personaje tiene disponibles, sin asumir que posee el libro de hechizos de nivel 80.
- Cubrir las especializaciones Arcano, Fuego y Escarcha, siempre que la estructura del addon original y las API del cliente 3.3.5a lo permitan.
- Conservar, en la medida de lo posible, el comportamiento original de las alertas y sus texturas.
- Documentar los cambios y las pruebas para que la comunidad pueda colaborar.

## Estado actual: importante

El archivo original proporcionado corresponde a una versión anterior de Cheese. Su archivo TOC declara la interfaz **30300** y sus notas indican **Cataclysm Visual Alerts**. Esto no demuestra que sea totalmente compatible con Wrath of the Lich King 3.3.5a. Además, el mapa de hechizos contiene entradas de varias clases y expansiones. Antes de afirmar que funciona del nivel 1 al 80, hay que auditarlo y probarlo en un cliente real de 3.3.5a.

No se afirma compatibilidad ni soporte completo de leveo hasta que los archivos correspondientes estén adaptados y probados dentro del juego.

## Próximas tareas

1. Revisar los mapas originales de IDs de hechizos y las definiciones de alertas.
2. Identificar los procs de Mago que existen en Wrath 3.3.5a.
3. Corregir la versión de interfaz y las incompatibilidades de API después de verificarlas.
4. Hacer que la detección de hechizos no dependa de una barra de acción o un libro de hechizos de nivel 80.
5. Probar distintos niveles y configuraciones de talentos de Arcano, Fuego y Escarcha.
6. Publicar versiones etiquetadas con instrucciones de instalación y limitaciones conocidas.

## Instalación (cuando se publique una versión probada)

Extraé la carpeta `Cheese` en:

```
World of Warcraft/Interface/AddOns/
```

Activá el addon desde la pantalla de selección de personaje. Antes, eliminá o guardá una copia de cualquier carpeta anterior de Cheese.

## Reportes de errores y colaboraciones

Al informar un problema, incluí:
- Versión del cliente y núcleo del servidor, si lo conocés.
- Nivel del personaje y especialización de Mago.
- Hechizos y talentos utilizados.
- Pasos para reproducir el problema y el error Lua exacto, si aparece.

## Créditos

- **Addon original:** Cheese. Los nombres de sus autores originales y la licencia deben verificarse en la distribución de origen antes de completar la atribución.
- **Adaptación para WoW 3.3.5a — Mago nivel 1–80:** **By Charls**.
- **Proyecto y mantenimiento de esta adaptación:** Charls.

Esta adaptación busca respetar el trabajo original. Si tenés información verificable sobre los autores o la licencia de la versión de origen, podés colaborar para completar los créditos correctamente.
