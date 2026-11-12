# WACCF Simonrim SkyPatcher Patch

**Version 0.1.0**

Restores Simonrim enchantments, enchantment charges and item names, and Gourmet's drink effects, where WACCF's SkyPatcher configs overwrite them at runtime. Generated from one load order (Overhaul 1.2), so the item lists are what that load order needed. The installer offers an option for a mod only when WACCF and that mod are active.

SkyPatcher configs only: no plugin, no assets.

## Requirements

- [SkyPatcher](https://www.nexusmods.com/skyrimspecialedition/mods/106659)
- [Weapons Armor Clothing and Clutter Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/18994) 2.11.4
- [Thaumaturgy - An Enchanting Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/57138)
- [Artificer - An Artifact Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/99619)
- [Mysticism - A Magic Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/27839)
- [Gourmet - A Cooking Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/96876)
- [kryptopyr's Patch Hub](https://www.nexusmods.com/skyrimspecialedition/mods/19518)

## The Problem

WACCF 2.11.4 ships SkyPatcher configs that run after all plugins load, so they beat every plugin, including the Thaumaturgy compatibility patch. They replace Artificer's enchantment on 7 items and Mysticism's on 1, reset enchantment charges, rename Thaumaturgy items, and add a Restore Stamina effect to 7 Gourmet items.

## What the Patch Does

Config files in a `zz WACCF Simonrim Restore` folder run after WACCF's and put those fields back: 748 item names, 8 enchantments, 9 enchantment charges and 7 Gourmet effects. WACCF's stats, weights, values and keywords stay. The installer offers one option per mod.

## Install

Install the release zip from the GitHub release in Mod Organizer 2. It is the FOMOD itself, so MO2 runs the installer, which offers one option per mod. Keep the `.zip.meta` file next to the zip so MO2 shows the version and the repository link. No plugin, so no LOOT step.

## Build from Source

Nothing to build here: the files in this repository are the release, and the release zip is these files with `fomod/` at its root. The configs were generated from the author's own load order with scripts that are not published.

## Verification Status

Checked 2026-11-07: all 756 armor and weapon lines hold in game (checked with a script that reads the live game), and 5 of the 7 Gourmet lines were read in game with no Restore Stamina left.

## Credits and Permissions

Holds no data from other mods except form references and item names.

Credit goes to the authors of the mods below. Permission status is based on each mod's Nexus page permissions, read on 2026-11-11. MIT (see LICENSE) covers this repository's scripts and documents only.

- [Weapons Armor Clothing and Clutter Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/18994) by kryptopyr: allowed based on the Nexus page permissions
- [Thaumaturgy - An Enchanting Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/57138) by SimonMagus: allowed based on the Nexus page permissions
- [Artificer - An Artifact Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/99619) by SimonMagus: allowed based on the Nexus page permissions
- [Mysticism - A Magic Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/27839) by SimonMagus: allowed based on the Nexus page permissions
- [Gourmet - A Cooking Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/96876) by SimonMagus: allowed based on the Nexus page permissions
- [SkyPatcher](https://www.nexusmods.com/skyrimspecialedition/mods/106659) by Zzyxzz: requirement only; nothing of it is shipped

Credit the authors above, keep the patch free, and do not sell or paywall the zip.

## More mods

Other Skyrim mods by kxgcayh:

- [odin-mysticism-adamant-patch](https://github.com/kxgcayh/odin-mysticism-adamant-patch): Lets Odin - Skyrim Magic Overhaul run with Mysticism and Adamant.
- [tposc-compat-patch](https://github.com/kxgcayh/tposc-compat-patch): The People Of Skyrim Complete patch: forwards USSEP fixes and keeps its landscape and navmesh over Cutting Room Floor.
- [beasthhbb-ibeasts-jkj-patch](https://github.com/kxgcayh/beasthhbb-ibeasts-jkj-patch): Fixes headless and dark-faced Khajiit when Project ja-Kha'jay is used with BeastHHBB and iBeasts.
- [lawless-tamrielic-patch-update](https://github.com/kxgcayh/lawless-tamrielic-patch-update): Updates the Lawless Bandit War plugins for Tamrielic Distribution 2.0 and later.
- [UntarnishedUI-QuickLootIE-Patch](https://github.com/kxgcayh/UntarnishedUI-QuickLootIE-Patch): Untarnished UI skins for QuickLoot IE 4.x.
- [WhereWasI](https://github.com/kxgcayh/WhereWasI): SKSE plugin: a recap on save load after a break.

## License

MIT, see [LICENSE](LICENSE).
