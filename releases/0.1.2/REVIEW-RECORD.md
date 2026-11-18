# WACCF Simonrim SkyPatcher Patch 0.1.2: release review (read-only)

Baseline: release record `releases/0.1.1/` (confirmed by the author).

Review 2026-11-18 under the mod-release-review skill, read-only. Author-tested set: none (notice-only release; nothing needs in-game testing).

## Measured facts
- 0.1.1 -> 0.1.2 archive: `THIRD-PARTY-NOTICES.txt` line 4 ("The plugins and any other files" -> "The config files"; the package has no plugin), `fomod/info.xml` and `meta.ini` version 0.1.2. The 7 SkyPatcher configs, `LICENSE` and `fomod/ModuleConfig.xml` are byte-equal to 0.1.1. MEASURED.
- Uploaded zip and `.meta` downloaded back from release v0.1.2 and compared byte-equal with `dist/github/`. MEASURED.
- `.meta`: `version=0.1.2.0`, `fileCategory=1`, `category=84`. MEASURED.

## DEFINITE
None.

## SUSPECTED
None (no finding depends on runtime behaviour).

## PRE-EXISTING (not blocking)
P1. Source `fomod/info.xml` says `<Version>0.1.0</Version>`; release.py writes the release version into the archive, so players get 0.1.2. Answer: not raised for a fix.
P2. `tools/patch-generator/restore.py` README template is stale (hardcoded 0.1.0, older credits text); rerunning it would overwrite the hand-edited README. Not shipped. Answer: not raised for a fix.
