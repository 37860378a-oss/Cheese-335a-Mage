# Auditoría técnica — archivo original de Cheese

Esta auditoría describe el archivo proporcionado para el proyecto. No significa que el addon haya sido probado dentro del juego.

## Hallazgos

- Carpeta del addon: `Cheese/`
- Archivo TOC: `Cheese.toc`
- Declaración de interfaz en el TOC: `30300`
- Notas del TOC: `Cataclysm Visual Alerts`
- Archivo principal de datos: `Data.lua`
- Lógica de activación de hechizos: `APISpellActivationOverlay.lua`
- Gestión de alertas y botones de acción: `SpellActivationOverlay.lua`, `ActionButton.lua`
- El archivo incluye texturas BLP para las alertas, entre ellas Arcane Missiles, Brain Freeze, Fingers of Frost y Hot Streak.
- El mapa de hechizos es amplio y contempla varias clases; no es un conjunto de datos exclusivo para Mago en 3.3.5a.

## Qué significa esto

Cambiar únicamente el número de interfaz del TOC no garantiza compatibilidad. Es necesario comprobar los IDs de hechizos, los IDs de auras de proc, la detección de las barras de acción, el manejo de eventos y las referencias a texturas contra el cliente 3.3.5a.

## Próximos pasos de implementación

- Verificar los IDs exactos de hechizos y auras de cada proc de Mago en 3.3.5a.
- Mantener en la adaptación de Mago únicamente los mapas de procs válidos para la época de Wrath.
- Verificar el manejo de rangos y la detección del libro de hechizos y de los espacios de acción en niveles bajos.
- Revisar todas las llamadas a la API contra el cliente 3.3.5a.
- Realizar pruebas dentro del juego en niveles representativos del leveo y con los tres árboles de talentos.

## Créditos de esta auditoría

Preparación y adaptación del proyecto: **Charls**.
