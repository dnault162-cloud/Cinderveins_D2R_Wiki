# Toolchain & Dev Setup

## Loader

**D2RLAN** — the base loader (multiplayer/TCP-capable fork; the same foundation ESR uses). Lives outside Program Files (e.g. `Documents\D2RLAN\`). Downloads its own D2R 2.4 file base; mods live in `D2RLAN\D2R\Mods\`.

- Launcher branding for the mod is driven by **`modinfo.json`** (`name`, `savepath`) + a **`Logo.png`** (~200×200) in the mod folder.
- `D2RLaunch` is the single-player-only sibling; we use D2RLAN for multiplayer capability (fits the Cinder Veins co-op DNA).

## Repo / mod folder

```
Documents\D2RLAN\D2R\Mods\
  CinderVeins\                     <- the Git repo root (CinderVeins_D2R)
    .gitignore
    modinfo.json
    Logo.png
    CinderVeins.mpq\
      data\
        global\excel\...           <- the .txt tables
        hd\global\ui\...           <- sprites / UI / art
```

- Repo is **private** while building. Mods release via Nexus (with its permission system), not public GitHub — the repo may never need to go public.
- **No license file** — you can't license Blizzard-derived data. Permissions handled the Nexus way at release.
- The full CASC extraction is kept in a **separate scratch folder** (reference library), never committed. The mod folder only holds files you actually changed.

## Tools

| Tool | Job | Source |
|------|-----|--------|
| **D2RLAN** | Loader / launcher | d2rmodding.com |
| **CascView** (Ladik's) | Extract base game data (.txt/.json/sprites) | zezula.net |
| **AFJ Sheet Edit** | Safe `.txt` table editing (**not** Excel — it corrupts files) | Phrozen Keep (d2mods.info) |
| **VS Code** | JSON editing + Git repo | code.visualstudio.com |
| **SpriteEdit** | `.sprite` editing (icons, stash tabs, UI, art) | Phrozen Keep |
| **MPQ Editor** | Packaging (optional — folder-named `.mpq` also works) | zezula.net (MPQ section) |
| **HxD** | Hex editor (e.g. bigger shared-stash `.d2i`) | mh-nexus.de |
| **D2CE** | D2R save / test-character editor (spin up test chars) | d2rcharactereditor.com |
| **D2RMM** | TypeScript value-tweak mods + merging premade QoL mods | nexusmods.com (mod #169) |

*Tier 3 (only when needed): Noesis + texture scripts (3D/textures), Unity D2R Scene Editor (maps — Phase 8), CV5 / DC6 Creator (animations).*

> Many of these are old, unsigned community tools — Windows Defender will false-flag several. Allow them / add exceptions.

## Key data files (cheat-sheet)

| File | Controls |
|------|----------|
| `skills.txt` | Skill behavior, damage, mana, synergies |
| `missiles.txt` | Projectile/FX behavior |
| `itemstatcost.txt` / `properties.txt` | Custom stats/affixes (the property machinery) |
| `uniqueitems.txt` | Unique items |
| `sets.txt` / `setitems.txt` | Sets |
| `runes.txt` | Runewords |
| `cubemain.txt` | Cube recipes (crafting, upgrades, key-forging) |
| `treasureclassex.txt` | Monster drop tables |
| `monstats.txt` / `monlvl.txt` | Monster stats & level scaling (difficulty) |
| `levels.txt` | Level/area definitions |

## Wiki hosting

Currently **GitHub Wiki** on the `CinderVeins_D2R` repo (markdown, version-controlled, zero setup). If it ever goes big and public, graduate to an ad-free host like wiki.gg — not a custom Next.js site (distraction).

### Getting these pages into the wiki

1. On GitHub, open the repo → **Wiki** tab → **Create the first page** (this initializes the wiki's hidden git repo).
2. Either paste each `.md` file's contents into a new page via the web UI (page name = filename without `.md`, e.g. `Class-Sorceress`), **or** clone the wiki repo (`CinderVeins_D2R.wiki.git`) in GitHub Desktop, drop all these `.md` files in, and push.
3. `Home.md` becomes the landing page; `_Sidebar.md` becomes the navigation sidebar automatically.
