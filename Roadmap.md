# Roadmap & Build Order

The guiding principle: **get it alive and playable first, then layer complexity onto a working skeleton.** A janky-but-running mod you can iterate on beats a half-built masterpiece. Build in vertical slices — finish one thing before going wide.

## Phase order

| Phase | Work | Difficulty | Notes |
|-------|------|-----------|-------|
| **0** | Tooling + repo setup | — | ← current. D2RLAN, repo in `Mods\CinderVeins\`, modinfo.json + Logo.png |
| **1** | Easy-win identity pass | Easy | Attribute system, level-up system, bigger cube/inventory, drop tuning. Single-table edits — instantly makes it "yours." |
| **2** | First class fully (Sorceress) | Medium | One class end-to-end. Learn the skill pipeline once. See [Class: Sorceress](Class-Sorceress.md). |
| **3** | Follower system | Medium | Merc skills, auras, scaling, gear slots, better follower gearing. |
| **4** | Item content — foundation | Hard (front-loaded) | Custom gems/runes, custom base items, custom properties/stats. Build once; everything sits on it. |
| **5** | Item content — the grind | Easy but long | Uniques, sets, runewords, gemwords. Mostly data entry once the foundation exists. |
| **6** | Cube recipes | Medium | Crafting, upgrading, key-forging. The "glue" that touches everything. |
| **7** | Difficulty tuning pass | Ongoing | "Brutal from level 1" — monster stat scaling. Revisited constantly via playtest. |
| **8** | **GR Portals + custom maps + keys** | Hardest | The capstone. Built **last** because custom maps are the only non-table pillar. See [Endgame](Endgame-GR-Portals.md). |

## Why this order

- **Foundation before content.** The hard, brain-bending work (custom stats/properties machinery) is small and front-loaded. The huge-looking work (hundreds of items) is repetitive data entry that goes fast once the machinery exists.
- **Classes before monster tuning.** You can't sanely tune monster difficulty/immunity until you know how all your classes deal damage.
- **Maps last.** Custom maps (`.ds1` editing, Unity D2R Scene Editor) are the single hardest pillar and the only one that leaves the comfortable "edit a table" world. Isolating it last means every other system is already built and tested — the map is just the container you pour them into.

## The morale curve

This project is **not** "long and hard the whole way." It's **a hard foundation, then a long-but-easy content grind.** Know which part you're in.
