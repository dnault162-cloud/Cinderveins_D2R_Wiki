# Class: Sorceress

The **first full class revamp.** The elemental trinity (Fire / Cold / Lightning) is **broken** and replaced with three fire-and-ash themed trees, giving the Sorceress a unified molten/ash identity unique to Cinder Veins.

## Identity & damage

- **Theme:** molten fire, lava veins, and choking ash. A glass-cannon caster who sets up and detonates.
- **Damage:** primarily Fire across all three trees, with Magic and debuff effects woven into Ashen Sorcery. (Because immunities are removed — see [Core Systems](Core-Systems.md) — an all-fire kit is fully viable; no tree needs a "coverage" damage type forced onto it.)

## Signature mechanic — Set up & detonate

A recurring theme across the kit: mark/burn enemies, then make them explode. Lean into this as the class's identity.

- **Molten Brand** — marked enemies explode on death.
- **Veinburst** — burning enemies erupt with shrapnel.
- **Cinder Curse** — cursed enemies release ash explosions when struck by fire spells.

## Survivability (glass-cannon answers)

A squishy caster in a brutal early game needs tools. Built-in answers:

- **Core Tap** — mana + cast-speed sustain.
- **Charred Mirror** — reflects a portion of incoming ranged damage.

---

## Tree 1 — Cinder Ash *(replaces Fire)*

| Skill | Description |
|-------|-------------|
| **Cinder Bolt** | Launches a fast ember projectile that leaves a brief burning trail. |
| **Ashflare** | A small fiery burst that blinds enemies with ash and deals fire damage. |
| **Ember Lance** | Fires a piercing spear of concentrated flame. |
| **Scorching Wake** | Sends a line of fire across the ground, burning enemies it passes through. |
| **Cinder Nova** | Releases a ring of burning ash around the Sorceress. |
| **Molten Brand** | Marks an enemy with a fiery sigil; marked enemies explode if killed. |
| **Blazing Shards** | Fires several jagged fragments of burning glass and coal. |
| **Ashstorm** | Summons a swirling storm of hot ash that damages enemies over time. |
| **Cinderstep** | Short-range teleport that leaves an ember explosion at the starting point. |
| **Heart of the Furnace** | Temporarily empowers fire spells, adding extra burn damage and ember splash. |

## Tree 2 — Veincraft *(replaces Lightning)*

| Skill | Description |
|-------|-------------|
| **Molten Vein** | Opens a glowing fissure beneath enemies, dealing fire damage over time. |
| **Searing Conduit** | Links the Sorceress to a target with a molten beam that burns continuously. |
| **Glassbone Spike** | Summons a jagged crystal spike from the ground, piercing enemies. |
| **Lava Pulse** | Sends a circular pulse through nearby ground veins, damaging enemies around you. |
| **Crimson Channel** | Converts a portion of mana spent into bonus fire damage for a short time. |
| **Veinburst** | Causes existing burning enemies to erupt with molten shrapnel. |
| **Igneous Grasp** | Molten hands rise from cracks in the earth, slowing and burning enemies. |
| **Cinderflow** | Creates a moving stream of lava that crawls forward and scorches enemies. |
| **Core Tap** | Drains heat from the earth to restore mana and briefly increase cast speed. |
| **Worldvein Rupture** | Tears open a massive molten vein, causing repeated eruptions in an area. |

## Tree 3 — Ashen Sorcery *(replaces Cold)*

The curse/debuff/DoT tree — shadowed fire and ash. Weakens enemies as much as it burns them.

| Skill | Description |
|-------|-------------|
| **Ash Bolt** | Fires a dark ash projectile that deals fire damage and slightly lowers enemy defense. |
| **Smothering Veil** | Creates a cloud of choking ash that slows enemies and reduces their accuracy. |
| **Black Ember** | Curses an enemy with shadowy ember that burns over time. |
| **Grave Smoke** | Releases haunted smoke around the Sorceress, damaging nearby enemies and weakening them. |
| **Ashen Hex** | Marks enemies in an area, making them take increased fire and magic damage. |
| **Soot Wraith** | Summons a drifting ash spirit that seeks enemies and explodes on contact. |
| **Charred Mirror** | Creates a smoke ward that reflects a portion of incoming ranged damage. |
| **Withering Flame** | Burns enemies with pale fire, reducing their damage dealt for a short time. |
| **Cinder Curse** | Afflicts enemies so they release ash explosions when struck by fire spells. |
| **Eclipse of Ash** | Darkens the battlefield with a storm of black ash, repeatedly damaging and weakening enemies in a large area. |

---

## Implementation notes

Reminder on the engine ceiling: you **recombine existing skill functions** (hardcoded behaviors), not write new logic. FX and missiles swap freely; the underlying *behavior* is what's being remapped. Most of these are clean drop-ins onto existing functions.

### Easy reskins (the bulk — fast, satisfying)

- **Bolts / projectiles:** Cinder Bolt, Ash Bolt, Ember Lance, Blazing Shards, Glassbone Spike (existing bolt / guided / pierce functions).
- **Novas / PBAoE:** Cinder Nova, Lava Pulse, Ashflare.
- **Ground DoT:** Scorching Wake, Molten Vein, Cinderflow, Ashstorm, Eclipse of Ash, Grave Smoke (Fire Wall / Inferno / Arctic Blast bones).
- **Self-buffs:** Heart of the Furnace, Crimson Channel, Core Tap (Enchant / Frozen Armor templates).
- **Curses / debuffs:** Smothering Veil, Black Ember, Ashen Hex, Withering Flame (slow / lower-defense / lower-damage templates).

### Stitch-jobs (the puzzles — where the real work concentrates)

- **Searing Conduit** — sustained beam. D2 has no true channel; fake it via rapid-repeat missile or trigger loop. *(Hardest.)*
- **Cinderstep** — Teleport + a triggered explosion at the origin point. Combining two behaviors.
- **Molten Brand / Veinburst / Cinder Curse** — kill- or on-burn-triggered detonations. Corpse-explosion / on-death-trigger behaviors exist (Necro side); wiring the trigger conditions is the work.
- **Soot Wraith** — a seeking summon that explodes on contact (homing missile / minion AI + death-detonate).
- **Worldvein Rupture** — repeated eruptions over an area (timed multi-trigger).
- **Igneous Grasp** — rising hands + slow (visual + crowd-control combo).

**Shape of the work:** ~25 reskins (fast) + ~5–6 stitch-jobs (the puzzle-solving). Very manageable for a first class.
