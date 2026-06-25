# Endgame: Cinder Veins Rift Portals

> **Status: VISION CAPTURE.** This is the capstone — built **last** (Phase 8). Custom maps are the hardest pillar in the project, so this waits until every other system (keys, drops, items, difficulty) is built and tested. Captured here now so the vision doesn't evaporate; details are intentionally open.

## The pitch

A **Greater-Rift-style endgame** layered on top of Hell — an additional difficulty tier beyond the campaign. Players access scaling Cinder Veins rifts through **portals opened with custom keys**, and these rifts drop **exclusive gear found nowhere else**.

## The loop (intended shape)

1. **Keys drop from specific enemies.** Certain monsters (which ones = TBD) drop custom rift keys.
2. **Key is cubed into a portal.** A cube recipe turns the key into a portal item / opens the rift. (Cube recipes are the idiomatic D2R way to do this — see [Toolchain](Toolchain.md).)
3. **The rift is a custom map** with its own monster set and difficulty scaling.
4. **Exclusive drops.** The rift's monsters use a dedicated treasure class, so the best gear drops *only* here.

This mirrors how big mods do endgame zones: repurpose/build a level, gate it behind a custom item, give it its own loot table.

## Open questions (the who / where / how — TBD)

- **Which enemies** drop keys? (Bosses only? Specific elite types? Act-end uniques?)
- **Scaling model** — do rifts scale infinitely (GR-style tiers) or in fixed tiers? What drives the scaling?
- **Key tiers** — one key type, or escalating keys that open higher rifts?
- **Map source** — repurpose existing maps, or author new `.ds1` layouts in the Unity D2R Scene Editor?
- **Exclusive gear** — what defines the rift-only loot pool? New uniques? A mythical/ascended tier?
- **Entry rules** — consumed key per run? Time limit? Death rules?

## Technical pillars this depends on (all built first)

- Custom **monster drop tables** (`treasureclassex.txt`) for keys + exclusive gear.
- Custom **cube recipe** (`cubemain.txt`) to forge the portal.
- A **portal item** + **destination map** (`levels.txt`, plus map work).
- Working **item content** (the exclusive gear must exist before it can drop).

Build the dream last. Write the dream down now.
