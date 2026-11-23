# Technical audit — supplied Cheese archive

This audit describes the archive supplied for the project; it is not a claim that the addon has been tested in-game.

## Findings

- Addon folder: `Cheese/`
- TOC: `Cheese.toc`
- TOC interface declaration: `30300`
- TOC notes: `Cataclysm Visual Alerts`
- Main data file: `Data.lua`
- Spell activation logic: `APISpellActivationOverlay.lua`
- Overlay and action-button handling: `SpellActivationOverlay.lua`, `ActionButton.lua`
- The archive includes BLP overlay textures, including Arcane Missiles, Brain Freeze, Fingers of Frost, and Hot Streak.
- The spell map is a broad multi-class map, not a Mage-only 3.3.5a dataset.

## Consequences

Changing only the TOC interface number would not establish compatibility. The spell IDs, proc aura IDs, action-bar scanning, event handling, and texture references must be checked against the 3.3.5a client.

## Next implementation steps

- Verify the exact 3.3.5a spell and aura IDs for each Mage proc.
- Keep only valid Wrath-era Mage proc mappings in the Mage adaptation layer.
- Verify rank handling and spellbook/action-slot detection at low levels.
- Check all API calls against the 3.3.5a client.
- Run in-game tests at representative leveling milestones and for all three talent trees.
