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

`Restore.ini` files in a `zz WACCF Simonrim Restore` folder run after WACCF's and put those fields back: {'name': 748, 'enchant': 8, 'gourmet effect': 7, 'charge': 9}. WACCF's stats, weights, values and keywords stay.

## Install

Copy `SKSE/` into its own MO2 mod. No plugin, so no LOOT step.

## Build from Source

Not standalone: `tools/overhaul-patches/restore.py` in the workspace generates the configs from the live load order.

## Verification Status

Check `SkyPatcher.log` for the configs, then read values in game. See the workspace report for the result.

## Credits and Permissions

Holds no data from other mods except form references and item names. Permissions not checked; check them before any release.

## License

MIT, see [LICENSE](LICENSE).
