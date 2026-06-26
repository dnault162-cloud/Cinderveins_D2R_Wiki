# Class: Necromancer

**Third class revamp.** The Necromancer keeps his soul — curses, bone, and an undead army — but every tree is now laced with grave-fire and ash. Original trees (Curses / Poison & Bone / Summoning) become **Graveflame Hexes**, **Bone & Cinder**, and **Hollowbound Servants**.

## Identity & damage

- **Theme:** necrotic fire — cursed flame, burning bone, and ash-born undead.
- **Damage:** **Magic** and **Fire** (hexes), **Physical/Magic** (bone), plus a **summon army**. The most multi-pronged class in the roster.
- **Role:** the commander. Curse to soften, summon to swarm, detonate corpses. Survives behind his army (the most forgiving playstyle — see the Hardcore-friendly summoner pattern).

## Signature mechanic — Curse, kill, detonate

The mod's burning theme meets the Necro's classic corpse loop:

- **Cinder Malediction** — cursed enemies explode into embers on death.
- **Gravebrand** — marks enemies to take bonus damage from minions.
- **Splinter Pyre** — detonates corpses (the Corpse Explosion lineage).

## Survivability

- The **army tanks** — Hollowbound Servants soak hits while you cast from the back.
- **Charred Armor** — scorched bone plating (Bone Armor lineage).
- **Servant's Pact** — sacrifice a minion to heal yourself.

---

## Tree 1 — Graveflame Hexes *(replaces Curses)*

| Skill | Description |
|-------|-------------|
| **Black Pyre** | Curses an enemy with dark fire that burns over time. |
| **Ashen Frailty** | Weakens enemies in an area, reducing their damage and resistance. |
| **Gravebrand** | Marks enemies so they take bonus damage from undead minions. |
| **Soul Scorch** | Burns the spirit of a target, dealing magic and fire damage. |
| **Ember Rot** | Causes enemies to decay while burning, reducing life regeneration. |
| **Hex of Hollow Bones** | Reduces enemy defense and makes them more vulnerable to bone spells. |
| **Funeral Smoke** | Creates a cloud of cursed smoke that blinds and slows enemies. |
| **Cinder Malediction** | Enemies afflicted by this curse explode into embers when killed. |
| **Wraithfire Chains** | Binds enemies with ghostly fire, slowing movement and attack speed. |
| **Doom of the Black Furnace** | Places a powerful curse that causes repeated soul-fire bursts around enemies. |

## Tree 2 — Bone & Cinder *(replaces Poison & Bone)*

| Skill | Description |
|-------|-------------|
| **Cinder Spear** | Fires a sharp bone spear wrapped in burning ash. |
| **Bone Shards** | Launches a spread of jagged bone fragments. |
| **Ashrib Cage** | Traps enemies inside a cage of burning ribs. |
| **Marrow Flame** | Sends a line of pale fire through the ground. |
| **Charred Armor** | Surrounds the Necromancer with scorched bone plating. |
| **Splinter Pyre** | Causes bones to erupt from a corpse, damaging nearby enemies. |
| **Skull Lantern** | Summons a floating skull that emits fire pulses. |
| **Grave Spike** | Raises a massive blackened bone spike from beneath an enemy. |
| **Cinderwall** | Creates a wall of bone and ash that blocks enemies and burns them. |
| **Catacomb Rupture** | Tears open the earth, releasing bones, ash, and cursed flame in a wide area. |

## Tree 3 — Hollowbound Servants *(replaces Summoning)*

| Skill | Description |
|-------|-------------|
| **Raise Ashwalker** | Summons a basic undead warrior made from ash and bone. |
| **Raise Cinder Archer** | Summons a skeletal archer that fires burning arrows. |
| **Bonehound** | Summons a fast undead hound that bites and bleeds enemies. |
| **Hollow Wraith** | Summons a ghostly servant that drains enemy life. |
| **Grave Golem** | Creates a hulking golem of bone, stone, and grave ash. |
| **Cinder Imp** | Summons a small undead fire-spirit that throws ember bolts. |
| **Ashen Banner** | Plants a necrotic banner that empowers nearby minions. |
| **Servant's Pact** | Sacrifices a minion to heal the Necromancer or empower other minions. |
| **Funeral Legion** | Temporarily summons a wave of fragile ash skeletons. |
| **Hollow King's Command** | Greatly empowers all summoned servants, increasing damage, speed, and fire effects. |

---

## Implementation notes

The Necro has excellent native bones — curses, bone spells, and summons are all his by default.

### Easy reskins (the bulk)

- **Hexes:** Black Pyre / Soul Scorch / Ember Rot (curse templates), Ashen Frailty (Decrepify/Lower Resist), Hex of Hollow Bones (Amplify Damage / lower-defense), Funeral Smoke (Dim Vision), Wraithfire Chains (Decrepify slow).
- **Bone:** Cinder Spear (Bone Spear), Bone Shards (Teeth), Ashrib Cage (Bone Prison), Charred Armor (Bone Armor), Splinter Pyre (Corpse Explosion), Grave Spike (Bone Spear single), Cinderwall (Bone Wall), Catacomb Rupture (big AoE bone).
- **Summons:** Ashwalker (Raise Skeleton), Cinder Archer / Cinder Imp (Skeleton Mage), Grave Golem (Golem), Bonehound / Hollow Wraith (Revive / minion bones), Hollow King's Command (minion-empower buff).

### Stitch-jobs (the puzzles)

- **Cinder Malediction** — curse that triggers explosion on death (curse + on-death-detonate combo).
- **Doom of the Black Furnace** — repeated timed soul-fire bursts (multi-trigger curse).
- **Skull Lantern** — floating turret summon that pulses fire (stationary-summon-with-attack behavior).
- **Ashen Banner** — stationary minion-empowering totem.
- **Servant's Pact** — sacrifice a minion for heal/empower (needs a sacrifice mechanic; reuse a targeted-minion-consume trigger).
- **Funeral Legion** — temporary timed wave summon (mass summon with expiry).
- **Gravebrand** — mark that boosts *minion* damage specifically (conditional damage tag).

**Shape of the work:** ~22 reskins + ~7 stitch-jobs. The summon-trigger and curse-trigger combos are where the work concentrates.
