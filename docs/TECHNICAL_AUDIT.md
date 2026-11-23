# Auditoría técnica y cambios — Cheese 3.3.5a

## Datos observados en el archivo original

- El TOC declara `Interface: 30300`, valor correspondiente a WoW 3.3.5.
- El texto `Cataclysm Visual Alerts` era una descripción; por sí solo no demuestra que el addon necesite Cataclysm.
- `Data.lua` contiene mapas de hechizos y procs de varias clases.
- `APISpellActivationOverlay.lua` relaciona hechizos colocados en la barra de acción con auras activas del jugador.
- El código original utiliza el cuarto retorno de `GetActionInfo` como ID global del hechizo, comportamiento previo a los cambios de API de 4.0.1.
- `UnitBuff` incluye el ID del aura como retorno 11 desde el parche 3.3.0; el ID debe seguir siendo la referencia principal.

## Cambios experimentales aplicados

- Se agregó una tabla de respaldo por nombre localizado, construida a partir de los IDs ya declarados en los mapas originales mediante `GetSpellInfo`.
- Para los botones de acción, primero se utiliza el ID global si está disponible y corresponde al mapa. Si no, se intenta resolver el nombre con `GetSpellBookItemName` y se busca el ID interno asociado.
- Para las auras, primero se utiliza el ID devuelto por `UnitBuff`; solo si no es utilizable se intenta resolver por nombre.
- Se agregó un escaneo completo de la barra de acción ante `SPELLS_CHANGED`, `PLAYER_LEVEL_UP`, `ACTIONBAR_PAGE_CHANGED` y `UPDATE_BONUS_ACTIONBAR`, además del evento original `ACTIONBAR_SLOT_CHANGED`.
- `ActionButton.lua` utiliza el mismo resolvedor que el escaneo de la barra, evitando que cada parte del addon identifique el hechizo de forma diferente.

## Limitaciones y pruebas pendientes

- La búsqueda por nombre depende del idioma del cliente y puede encontrar colisiones entre rangos con el mismo nombre. Por eso es un respaldo, no un reemplazo de los IDs.
- Los mapas originales pueden contener IDs que no correspondan a 3.3.5a o procs que no estén cubiertos.
- La build necesita pruebas reales con varias clases, niveles y especializaciones. No se debe considerar estable hasta completar esas pruebas.
- No se pudo ejecutar el cliente WoW desde este entorno; el paquete se entrega como build experimental para prueba manual.

## Créditos

Auditoría, adaptación experimental y mantenimiento: **Charls**.
