# WACCF Simonrim SkyPatcher Patch

**Version 0.1.0**

Restores Simonrim enchantments, enchantment charges and item names, and Gourmet's drink effects, where WACCF's SkyPatcher configs overwrite them at runtime. Private: generated for the Overhaul 1.2 load order and not published.

SkyPatcher configs only: no plugin, no assets.

## Requirements

- [SkyPatcher](https://www.nexusmods.com/skyrimspecialedition/mods/106659)
- [Weapons Armor Clothing and Clutter Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/18994) 2.11.4
- [Thaumaturgy](https://www.nexusmods.com/skyrimspecialedition/mods/57138), Artificer, Mysticism, Gourmet, and kryptopyr's Patch Hub

## The Problem

WACCF 2.11.4 ships SkyPatcher configs that run after all plugins load, so they beat every plugin, including the Thaumaturgy compatibility patch. They replace Artificer's enchantment on 7 items and Mysticism's on 1, reset enchantment charges, rename Thaumaturgy items, and add a Restore Stamina effect to 7 Gourmet items.

## What the Patch Does

Config files in a `zz WACCF Simonrim Restore` folder run after WACCF's and put those fields back: 748 item names, 8 enchantments, 9 enchantment charges and 7 Gourmet effects. WACCF's stats, weights, values and keywords stay. The installer offers one option per mod.

## Install

Install the release zip from the GitHub release in Mod Organizer 2. It is the FOMOD itself, so MO2 runs the installer, which offers one option per mod. Keep the `.zip.meta` file next to the zip so MO2 shows the version and the repository link. No plugin, so no LOOT step.

## Build from Source

Not standalone: `tools/overhaul-patches/restore.py` in the workspace generates the configs from the live load order. The configs are tracked in this repository, and the release archive is built from them with the workspace `tools/mod-release/release.py`. `restore.py` also writes the FOMOD zip to `dist/WACCF Simonrim SkyPatcher Patch.zip`.

## Verification Status

Checked 2026-11-07: all 756 armor and weapon lines hold in game (`verify.py live`), and 5 of the 7 Gourmet lines were read in game with no Restore Stamina left.

## Credits and Permissions

Holds no data from other mods except form references and item names.

Checked on 2026-11-11 against each mod's Nexus permission block and author notes, not its description or readme. MIT (see LICENSE) covers this repository's scripts and documents only. The plugins are derived from the mods below and stay under their authors' terms.

| Mod | Author | What the Nexus page says | Status |
|---|---|---|---|
| [Weapons Armor Clothing and Clutter Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/18994) | kryptopyr | Compatibility patches and record edits (keywords, stats and the like) are allowed. Its assets and files may not be redistributed or sold. | allowed |
| [Thaumaturgy - An Enchanting Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/57138) | SimonMagus | Open: patches, ports and derivative work need no permission. The author asks you to consider releasing derivatives open. | allowed |
| [Artificer - An Artifact Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/99619) | SimonMagus | Upload, modification, conversion and asset use are allowed. Not in sold files. | allowed |
| [Mysticism - A Magic Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/27839) | SimonMagus | Open: patches, ports and derivative work need no permission. The author asks you to consider releasing derivatives open. | allowed |
| [Gourmet - A Cooking Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/96876) | SimonMagus | Upload, modification, conversion and asset use are allowed. Not in sold files. | allowed |
| [SkyPatcher](https://www.nexusmods.com/skyrimspecialedition/mods/106659) | Zzyxzz | No permission is granted. This patch only requires SkyPatcher and ships config files in its format, no SkyPatcher code or assets. | requirement only |

All sources allow this use. Credit the authors above, keep the patch free, and do not sell or paywall the zip.

## License

MIT, see [LICENSE](LICENSE).
