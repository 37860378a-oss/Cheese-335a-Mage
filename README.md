# Cheese 3.3.5a — Soporte para todas las clases, niveles 1–80

**Estado: adaptación en desarrollo. Todavía no es una versión probada.**

Proyecto comunitario para adaptar Cheese a **World of Warcraft 3.3.5a**, conservando su enfoque general para **todas las clases**. El objetivo es que las alertas funcionen durante todo el progreso del personaje, desde nivel 1 hasta 80, sin exigir ser nivel máximo ni usar perfiles separados por clase.

## Objetivos

- Mantener el soporte general para todas las clases.
- Hacer que las alertas disponibles funcionen desde nivel 1 hasta 80.
- Reconocer hechizos y rangos aprendidos por el personaje, así como los procs que realmente puede activar.
- Evitar depender de un libro de hechizos o una barra de acción propios de nivel 80.
- Conservar el diseño, los efectos visuales y las texturas originales siempre que sean compatibles.
- Probar el comportamiento en las distintas clases y especializaciones de WoW 3.3.5a.

## Estado y diagnóstico inicial

El archivo original proporcionado declara la interfaz **30300** y sus notas dicen **Cataclysm Visual Alerts**. El mapa de hechizos contempla varias clases, por lo que el objetivo no es convertir Cheese en un addon exclusivo para Mago.

La primera revisión del código no encontró una comprobación directa de nivel 80 (UnitLevel) que bloquee el addon. Sí encontró mapas fijos de hechizos y auras, además de una inicialización que escanea la barra de acción al iniciar sesión y responde a cambios de espacios de acción. Por eso, la causa puede estar en IDs de hechizos/procs que no coinciden con 3.3.5a, rangos aprendidos durante el leveo o falta de actualización al aprender hechizos; todavía hay que comprobarlo en el cliente.

Cambiar solamente el número de interfaz del TOC no garantiza compatibilidad.

## Próximas tareas

1. Verificar los IDs de hechizos y auras de proc de todas las clases en 3.3.5a.
2. Comprobar que estén contemplados los rangos de hechizos que se aprenden durante el leveo.
3. Revisar la detección de la barra de acción y actualizarla cuando se aprendan hechizos o cambie la página de acción.
4. Revisar las llamadas a la API contra el cliente 3.3.5a.
5. Probar desde niveles bajos hasta 80 con distintas clases y especializaciones.
6. Publicar builds probadas con instrucciones y limitaciones conocidas.

## Instalación (cuando se publique una versión probada)

Extraé la carpeta Cheese en:

    World of Warcraft/Interface/AddOns/

Activá el addon desde la pantalla de selección de personaje. Antes, eliminá o guardá una copia de cualquier carpeta anterior de Cheese.

## Reportes de errores y colaboraciones

Al informar un problema, incluí:
- Versión del cliente y núcleo del servidor, si lo conocés.
- Clase, nivel y especialización.
- Hechizos y talentos utilizados.
- Pasos para reproducir el problema y el error Lua exacto, si aparece.

## Créditos

- **Addon original:** Cheese. Los autores originales y la licencia deben verificarse en la distribución de origen antes de completar la atribución.
- **Adaptación para WoW 3.3.5a, todas las clases y niveles 1–80:** **By Charls**.
- **Proyecto y mantenimiento de esta adaptación:** Charls.

Esta adaptación busca respetar el trabajo original. Si tenés información verificable sobre los autores o la licencia de la versión de origen, podés colaborar para completar los créditos correctamente.
