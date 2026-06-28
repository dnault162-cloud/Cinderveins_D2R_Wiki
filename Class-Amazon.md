# Class: Amazon

**Seventh and final class revamp.** The Amazon becomes an **ember-hunter** — molten javelins, burning volleys, and an ash-warrior's discipline. Original trees (Javelin & Spear / Bow & Crossbow / Passive & Magic) become **Cinder Javelins**, **Ashen Archery**, and **Veinwarden Discipline**.

## Identity & damage

- **Theme:** the forge-hunter — every spear and arrow is molten or ash-touched.
- **Damage:** **Physical** and **Fire** (ranged & thrown). Mobile, precise, kite-and-burn.
- **Role:** the ranged carry. Two distinct offensive identities (throw vs bow) sharing one passive survival/utility tree — flexible build paths.

## Signature mechanic — Mark & focus

- **Widow Ash / Hunter's Mark of Ash** — mark enemies for bonus bow/ranged damage.
- **Battle Trance** — consecutive hits build focus, ramping damage (the recurring charge-up theme).
- Both offensive trees lean on **pierce + burn** for chewing through packs.

## Survivability (the evasive hunter)

An entire passive tree keeps her alive at range:

- **Ashen Reflex / Ashguard Stance** — dodge, block, resistances (the Avoid/Dodge/Evade lineage).
- **Molten Footwork** — dodging briefly boosts attack speed (rewarding evasion).
- **Burning Resolve** — fire resistance + control-effect reduction.
- **Cinderstep** — an evasive ember dash (shared flavor with the Sorc/Assassin blink).

---

## Tree 1 — Cinder Javelins *(replaces Javelin & Spear)*

| Skill | Description |
|-------|-------------|
| **Ember Javelin** | Throws a burning javelin that deals fire damage on impact. |
| **Molten Pierce** | A powerful spear throw that pierces through multiple enemies. |
| **Cinder Impale** | A close-range spear thrust that deals heavy damage to a single target. |
| **Lavafang Throw** | Hurls a jagged molten javelin that causes burning wounds. |
| **Ashsplitter Spear** | Splits on impact, sending smaller fiery shards into nearby enemies. |
| **Worldvein Skewer** | Throws a charged spear that erupts from the ground beneath the target. |
| **Crimson Volley** | Rapidly throws several ember-charged javelins in a cone. |
| **Furnace Spearwall** | Creates a short line of burning spear impacts in front of the Amazon. |
| **Cinderstorm Javelin** | Throws a javelin that bursts into a storm of sparks and ash. |
| **Heartpiercer of the Forge** | Ultimate spear throw that pierces enemies, explodes, and leaves molten ground behind. |

## Tree 2 — Ashen Archery *(replaces Bow & Crossbow)*

| Skill | Description |
|-------|-------------|
| **Cinder Arrow** | Fires a basic flaming arrow that burns the target. |
| **Sootshot** | Fires an ash-covered arrow that lowers enemy accuracy. |
| **Blackglass Arrow** | Fires a volcanic glass arrow that causes bleeding. |
| **Ember Rain** | Launches arrows into the sky, causing burning arrows to fall in an area. |
| **Ashfang Shot** | Fires a cursed arrow that deals poison and fire damage over time. |
| **Scorchline Arrow** | Shoots an arrow that leaves a burning trail through enemies. |
| **Furnace Volley** | Releases multiple fire arrows in a wide spread. |
| **Cinderburst Arrow** | Arrow explodes on impact, damaging nearby enemies. |
| **Widow Ash** | Marks an enemy with cursed ash, increasing bow damage against them. |
| **Rain of the Red Vein** | Ultimate bow skill that blankets a large area with molten arrows and ash explosions. |

## Tree 3 — Veinwarden Discipline *(replaces Passive & Magic)*

| Skill | Description |
|-------|-------------|
| **Ashen Reflex** | Passive skill that increases dodge chance and movement speed. |
| **Cinderstep** | Quick evasive dash that leaves a small burst of embers behind. |
| **Veinwarden Focus** | Temporarily increases attack rating and critical strike chance. |
| **Burning Resolve** | Grants resistance to fire and reduces control effects. |
| **Hunter's Mark of Ash** | Marks an enemy, making them easier to hit and more vulnerable to ranged attacks. |
| **Molten Footwork** | Dodging an attack briefly increases attack speed. |
| **Battle Trance** | Consecutive hits build focus, increasing damage for a short time. |
| **Ashguard Stance** | Defensive stance that improves dodge, block, and resistances. |
| **Red Vein Precision** | Passive that gives spear and bow attacks a chance to pierce or critically strike. |
| **Avatar of the Veinwarden** | Ultimate discipline skill that boosts speed, dodge, pierce chance, and adds ember explosions to bow and spear attacks. |

---

## Implementation notes

The Amazon's native kit (Fire Arrow, Multiple Shot, Strafe, Immolation Arrow, Jab, Impale, Lightning Fury, and the Dodge/Avoid/Penetrate passives) is an excellent base.

### Easy reskins (the bulk)

- **Cinder Javelins:** Ember Javelin (Power Strike / Jab + fire), Molten Pierce (Impale / pierce), Cinder Impale (Impale), Ashsplitter Spear / Cinderstorm Javelin (Lightning Fury → ember burst), Crimson Volley (Plague Javelin spread), Heartpiercer (pierce + explode finisher).
- **Ashen Archery:** Cinder Arrow (**Fire Arrow**), Furnace Volley (**Multiple Shot**), Cinderburst Arrow (**Exploding Arrow**), Ember Rain / Rain of the Red Vein (**Immolation Arrow** / mortar-style), Scorchline Arrow (Strafe/Fire Arrow trail), Sootshot/Blackglass (debuff arrows).
- **Veinwarden:** Ashen Reflex / Ashguard Stance (Dodge/Avoid/Evade passives), Veinwarden Focus (Penetrate/Critical), Red Vein Precision (Pierce/Critical Strike passive), Hunter's Mark of Ash (Inner Sight), Burning Resolve (resist buff).

### Stitch-jobs (the puzzles)

- **Cinderstep** — evasive dash (no native Amazon dash; reuse a blink behavior — same as the Sorc/Assassin Cinderstep).
- **Molten Footwork** — on-dodge → attack-speed trigger (reaction trigger).
- **Battle Trance** — consecutive-hit focus stack (charge-up system; reuse Assassin's).
- **Worldvein Skewer** — spear erupting from the ground under a target (delayed ground-trigger).
- **Widow Ash / Hunter's Mark** — conditional bonus damage marks.
- **Ember Rain / Rain of the Red Vein** — sky-falling area arrows (Immolation Arrow bones help, but the "rain from above" timing is the stitch).

**Shape of the work:** ~24 reskins + ~6 stitch-jobs. Archery is almost entirely native reskins; the Veinwarden triggers are where the work concentrates.
