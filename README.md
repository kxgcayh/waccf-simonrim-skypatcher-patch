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

Holds no data from other mods except form references and item names. Permissions not checked; check them before any release.

## License

MIT, see [LICENSE](LICENSE).
