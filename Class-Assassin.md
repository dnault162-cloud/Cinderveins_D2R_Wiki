# Class: Assassin

**Fifth class revamp.** The Assassin becomes an **ash-and-ember killer** — burning claws, fire traps, and a smoke-and-shadow toolkit. Original trees (Martial Arts / Traps / Shadow Disciplines) become **Ashen Blades**, **Cinder Traps**, and **Veilcraft**.

## Identity & damage

- **Theme:** smoke, soot, and volcanic glass — a precise, mobile assassin who burns from the shadows.
- **Damage:** **Physical** and **Fire** (claws), **Fire** (traps), with **utility/control** from Veilcraft.
- **Role:** high-skill striker. Charge-up combos, deployable trap fields, and escape tools. Rewards active play.

## Signature mechanic — Charge & detonate *(native fit!)*

The Assassin **already has** the build-up/finisher mechanic natively (charge-up skills + finishing moves), so the mod's "stack heat, then release" theme is a *clean fit* here — unlike the Druid/Paladin where it's a stitch-job:

- **Scorchmark Combo** — builds charges per hit; the finisher detonates the marks.
- **Furnace-style stacking** — native charge-up bones.

> **This class is the reference implementation for the charge-up mechanic.** Build it here first, then borrow it for Druid's Primal Furnace and Paladin's Furnace Zeal.

## Survivability

- **Veil of Soot / Cindercloak** — dodge and stealth (Fade / Burst of Speed / Cloak of Shadows lineage).
- **Ashstep / Ember Recall** — mobility escapes.
- **Smoke Double** — a decoy clone to pull aggro (Shadow Warrior/Master lineage).

---

## Tree 1 — Ashen Blades *(replaces Martial Arts)*

| Skill | Description |
|-------|-------------|
| **Cinder Fang** | A claw strike that adds fire damage and leaves a short burn. |
| **Sootcut** | Slashes an enemy with a smoke-darkened blade, lowering their defense. |
| **Ember Talon** | A fast dual-claw hit that deals bonus damage to burning enemies. |
| **Blackglass Slash** | Strikes with razor-sharp volcanic glass, causing bleed damage. |
| **Ashen Flurry** | Rapidly attacks nearby enemies with a storm of claw strikes. |
| **Veinpiercer** | A precise stab that deals heavy damage and ignores some armor. |
| **Scorchmark Combo** | Builds charges with each hit; finishing move detonates the marks. |
| **Widow Ember** | Poisons and burns the target with a cursed ember venom. |
| **Silent Cremation** | Executes a weakened enemy, causing an ash burst around them. |
| **Dance of Cinders** | A powerful spinning blade assault that hits multiple enemies and spreads burning wounds. |

## Tree 2 — Cinder Traps *(replaces Traps)*

| Skill | Description |
|-------|-------------|
| **Ember Mine** | Places a small mine that explodes when enemies approach. |
| **Smoke Pot** | Drops a smoke device that blinds and slows enemies in an area. |
| **Cinder Sentry** | Places a trap that fires ember bolts at nearby enemies. |
| **Ashwire Snare** | Sets a hidden wire that trips, slows, and damages enemies. |
| **Blackpowder Bloom** | Throws an explosive device that bursts into fire and ash. |
| **Molten Needle Trap** | Launches heated spikes from the ground when triggered. |
| **Sootburst Charge** | Places a delayed explosive that knocks enemies back. |
| **Glass Shard Nest** | Scatters volcanic glass shards that damage enemies walking over them. |
| **Furnace Lotus** | Deploys a rotating flame trap that burns enemies around it. |
| **Cinderweb Engine** | An ultimate trap that creates a large burning snare field and repeatedly erupts with fire blasts. |

## Tree 3 — Veilcraft *(replaces Shadow Disciplines)*

| Skill | Description |
|-------|-------------|
| **Ashstep** | Teleports a short distance, leaving a smoke puff behind. |
| **Veil of Soot** | Surrounds the Assassin in smoke, increasing dodge chance. |
| **Shadow Ember** | Sends out a dark ember that weakens enemy damage. |
| **Smoke Double** | Creates a shadow clone that distracts enemies briefly. |
| **Cindercloak** | Temporarily hides the Assassin from weaker enemies and boosts first-strike damage. |
| **Blind Ash** | Throws cursed ash into enemies' eyes, reducing accuracy. |
| **Umbral Vein** | Marks a shadow path, increasing movement speed along it. |
| **Black Veil Curse** | Weakens enemies in an area, making them take more trap and blade damage. |
| **Ember Recall** | Returns the Assassin to a previous position in a burst of smoke. |
| **Nightfall Crematorium** | Covers a large area in black smoke and emberlight, blinding enemies while empowering Assassin skills. |

---

## Implementation notes

The Assassin has the best native fit for the mod's signature mechanic, plus strong trap and shadow bones.

### Easy reskins (the bulk)

- **Ashen Blades:** Cinder Fang (Tiger Strike / Fists of Fire charge-up), Scorchmark Combo (**native** charge-up + finisher — easiest of all the "stacking" skills), Dance of Cinders (Dragon Flight / Phoenix Strike finisher), Ashen Flurry (multi-strike), Widow Ember (Venom), Sootcut (defense-lower on hit).
- **Cinder Traps:** Ember Mine (Wake of Fire), Cinder Sentry (Charged Bolt / Lightning Sentry → fire), Furnace Lotus (Wake of Inferno), Cinderweb Engine (Death Sentry-style), Glass Shard Nest (caltrop ground hazard), Molten Needle Trap (spike trap).
- **Veilcraft:** Veil of Soot (Fade / Burst of Speed), Cindercloak / Blind Ash / Black Veil Curse (Cloak of Shadows), Smoke Double (Shadow Warrior / Shadow Master), Shadow Ember (debuff missile).

### Stitch-jobs (the puzzles)

- **Ember Talon / Black Veil Curse** — conditional bonus vs *burning* / vs *trap & blade* targets (the condition check).
- **Silent Cremation** — execute on low-life target + burst (low-life condition trigger).
- **Ashstep / Ember Recall** — short blink and return-to-previous-position (Dragon Flight bones for blink; "recall" needs a stored-position trigger).
- **Umbral Vein** — a movement-speed path/zone (ground buff area).
- **Sootburst Charge** — delayed explosive with knockback (timed trigger + knockback).

**Shape of the work:** ~24 reskins + ~5 stitch-jobs, and the all-important charge-up mechanic is *native here* — making the Assassin the smart class to prototype that system on first.
