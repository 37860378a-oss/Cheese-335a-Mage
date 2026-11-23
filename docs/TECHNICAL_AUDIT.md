# Auditoría técnica — archivo original de Cheese

Esta auditoría describe el archivo proporcionado para el proyecto. No significa que el addon haya sido probado dentro del juego.

## Hallazgos del código

- Carpeta del addon: Cheese/
- Archivo TOC: Cheese.toc
- Declaración de interfaz: 30300
- Notas del TOC: Cataclysm Visual Alerts
- Datos de hechizos y alertas: Data.lua
- Detección de procs y barra de acción: APISpellActivationOverlay.lua
- Efectos sobre botones: ActionButton.lua
- El mapa de hechizos de acción contiene entradas de varias clases; no es un addon diseñado únicamente para Mago.
- El mapa de auras que dispara las alertas es una lista fija de IDs de proc.
- La inicialización recorre los espacios de acción al iniciar sesión y luego escucha ACTIONBAR_SLOT_CHANGED.
- En la lógica revisada no aparece una comprobación directa de nivel 80 mediante UnitLevel.

## Interpretación

La revisión no demuestra que exista un bloqueo explícito para personajes menores de nivel 80. El comportamiento descrito puede deberse a que los IDs de hechizos o auras no correspondan con los del cliente 3.3.5a, a que falten rangos de bajo nivel o a que el addon no vuelva a actualizar correctamente sus referencias cuando el personaje aprende hechizos.

El mapa general de hechizos es una buena base para conservar el soporte multiclase, pero no alcanza por sí solo para afirmar que todas las alertas están cubiertas en Wrath 3.3.5a. Cambiar únicamente el número de interfaz del TOC tampoco garantiza compatibilidad.

## Próximos pasos

1. Contrastar los IDs de cada proc y sus hechizos asociados con 3.3.5a para todas las clases.
2. Verificar rangos y hechizos aprendidos en distintos niveles.
3. Revisar y, si hace falta, ampliar el refresco de la barra de acción al aprender hechizos, subir de nivel y cambiar páginas de acción.
4. Verificar las llamadas a la API contra el cliente 3.3.5a.
5. Realizar pruebas reales con personajes de distintas clases y niveles.

## Créditos

Auditoría, adaptación y mantenimiento del proyecto: **Charls**.
