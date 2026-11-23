# Cheese 3.3.5a — Mage Leveling Edition

**Project status: adaptation in progress. Not yet a tested release.**

Community project to adapt the Cheese spell-activation overlay addon for **World of Warcraft 3.3.5a**, focusing on the Mage class from level **1 to 80**.

## Goals

- Support Mage characters while leveling from 1 to 80.
- Detect the character's currently available spells and talents instead of assuming a level-80 spellbook.
- Cover Arcane, Fire, and Frost where the original addon architecture and 3.3.5a client APIs allow it.
- Preserve the original overlay behavior and textures wherever possible.
- Document changes and test reports so the community can contribute.

## Important: current state

The supplied archive is an older Cheese build. Its TOC declares interface **30300** and its notes say **Cataclysm Visual Alerts**. This is not proof of full Wrath of the Lich King 3.3.5a compatibility. The spell map also contains entries from several classes and expansions. The project must be audited and tested against an actual 3.3.5a client before claiming that it works from level 1 to 80.

No compatibility or leveling support is claimed until the relevant files are committed and tested in-game.

## Planned work

1. Audit the original spell-ID maps and overlay definitions.
2. Identify Mage proc alerts that exist in Wrath 3.3.5a.
3. Correct the interface version and API incompatibilities after verification.
4. Make spell detection independent of a level-80 action-bar layout or spellbook.
5. Test levels and talent builds across Arcane, Fire, and Frost.
6. Publish tagged releases with installation instructions and known limitations.

## Installation (when a tested build is published)

Extract the `Cheese` folder into:

```
World of Warcraft/Interface/AddOns/
```

Enable the addon on the character-selection AddOns screen. Remove or back up older Cheese folders first.

## Contributions and bug reports

Please include:
- Client version / server core if known.
- Character level and Mage specialization.
- Spell/talent setup.
- Steps to reproduce and the exact Lua error (if any).

## Credits

- Original Cheese addon authors: attribution and original license still need to be verified from the upstream distribution.
- 3.3.5a Mage adaptation: **Charls**.
