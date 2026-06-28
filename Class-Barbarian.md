# Class: Barbarian

**Sixth class revamp.** The Barbarian becomes a **molten berserker** — fire-charged fury, ash-choked warcries, and forge-forged weapon techniques. Original trees (Combat Skills / Warcries / Combat Masteries) become **Cinder Rage**, **Ashen Warcries**, and **Furnace Arms**.

## Identity & damage

- **Theme:** rage as fire — the angrier he gets, the hotter he burns. Molten steel and explosive anger.
- **Damage:** **Physical** and **Fire** — the purest melee bruiser in the roster.
- **Role:** frontline destroyer + party anchor. Warcries buff allies and break enemies (strong in co-op), while Cinder Rage turns him into a self-detonating wrecking ball.

## Signature mechanic — Build heat, then erupt

The Barbarian leans hardest into the mod's "stacking heat" theme:

- **Rage Ignition** — builds heat as you fight, ramping damage after repeated hits.
- **Volcanic Wrath** — kills have a chance to trigger eruptions.
- **Cinderborn Berserk** — ultimate rage state; attacks explode with embers.

> Uses the same charge-up system as Druid's Primal Furnace and Paladin's Furnace Zeal — build it once on the [Assassin](Class-Assassin.md) (native), reuse here.

## Survivability (the bruiser)

- **Obsidian Guard** — raises weapon defense / block-style survival.
- **Gravelord's Taunt** — forces enemies onto him while reducing his incoming damage (a true tank tool).
- **Cinder Rally** — restores life/mana to himself and nearby allies.
- Warcries like **Iron Lung** extend his buffs, and **Battle Smoke** lowers enemy accuracy.

---

## Tree 1 — Cinder Rage *(replaces Combat Skills)*

| Skill | Description |
|-------|-------------|
| **Ember Cleave** | A wide melee swing that deals bonus fire damage to nearby enemies. |
| **Rage Ignition** | Builds heat as you fight, increasing damage after repeated hits. |
| **Bloodfire Frenzy** | Rapid attacks that burn enemies and increase attack speed with each strike. |
| **Cinder Leap** | Leaps into battle and creates a fiery impact on landing. |
| **Molten Rampage** | Charges forward, smashing through enemies and leaving burning ground behind. |
| **Ashbreaker Slam** | Slams the ground, sending out a short wave of fire and stone. |
| **Fury of the Pit** | Temporarily increases movement speed, attack speed, and fire damage. |
| **Scorched Wounds** | Your attacks cause enemies to bleed and burn at the same time. |
| **Volcanic Wrath** | Each kill has a chance to trigger a small eruption around you. |
| **Cinderborn Berserk** | Ultimate rage state that boosts damage, resistance, and causes attacks to explode with embers. |

## Tree 2 — Ashen Warcries *(replaces Warcries)*

| Skill | Description |
|-------|-------------|
| **Warcry of Embers** | Boosts ally damage and adds minor fire damage to attacks. |
| **Soot Roar** | Intimidates nearby enemies, lowering their defense. |
| **Howl of the Furnace** | Frightens weaker enemies and causes burning enemies to flee. |
| **Ashen Command** | Increases ally attack rating and movement speed. |
| **Battle Smoke** | Creates a cloud of ash around the Barbarian, reducing enemy accuracy. |
| **Roar of Ruin** | Lowers enemy resistances in a wide area. |
| **Iron Lung** | Increases the duration and strength of all warcries. |
| **Cinder Rally** | Restores a small amount of life and mana to nearby allies over time. |
| **Gravelord's Taunt** | Forces enemies to focus the Barbarian while reducing incoming damage. |
| **Voice of the Worldfire** | Ultimate warcry that empowers allies, weakens enemies, and causes nearby corpses to erupt in ash. |

## Tree 3 — Furnace Arms *(replaces Combat Masteries)*

| Skill | Description |
|-------|-------------|
| **Molten Strike** | A heavy weapon attack that adds fire damage and briefly weakens armor. |
| **Blacksteel Mastery** | Passive weapon mastery that increases damage and attack rating. |
| **Ashsplitter** | A powerful overhead strike that deals bonus damage to armored enemies. |
| **Cinder Throw** | Throws a weapon or axe charged with burning force. |
| **Hammerfall** | Smashes the ground with a weapon, stunning nearby enemies. |
| **Furnace Grip** | Increases dual-wield damage and chance to apply burning wounds. |
| **Obsidian Guard** | Raises weapon defense, increasing block/parry-style survivability. |
| **Anvilbreaker** | A crushing blow attack with a chance to stagger bosses and champions. |
| **Steelstorm** | Spins with weapons drawn, striking enemies around you with ember trails. |
| **World-Anvil Execution** | Ultimate weapon technique: a massive strike that cracks the ground and erupts with molten force. |

---

## Implementation notes

The Barbarian's native kit (Bash, Frenzy, Leap, Charge, Whirlwind, the full warcry set, weapon masteries) maps cleanly.

### Easy reskins (the bulk)

- **Cinder Rage:** Ember Cleave (Bash/Cleave), Bloodfire Frenzy (Frenzy), Cinder Leap (Leap Attack), Molten Rampage (Charge), Fury of the Pit (Berserk-style buff), Cinderborn Berserk (Berserk ultimate).
- **Ashen Warcries:** near 1:1 — Warcry of Embers (Battle Orders/Shout), Soot Roar (Battle Cry), Howl of the Furnace (Howl), Ashen Command (Battle Command), Iron Lung (Shout-duration passive), Gravelord's Taunt (Taunt), Cinder Rally (heal aura).
- **Furnace Arms:** Molten Strike (weapon attack + fire), Blacksteel Mastery (weapon mastery passive), Ashsplitter (Bash/Stun), Cinder Throw (Throwing/Double Throw), Hammerfall (Stun), Furnace Grip (Double Swing), Obsidian Guard (Iron Skin), Anvilbreaker (Crushing Blow attack), **Steelstorm (Whirlwind)**.

### Stitch-jobs (the puzzles)

- **Rage Ignition** — stacking heat ramp (charge-up system; reuse the Assassin implementation).
- **Volcanic Wrath** — on-kill chance to erupt (on-death trigger).
- **Scorched Wounds** — simultaneous bleed + burn (dual DoT application).
- **Voice of the Worldfire** — warcry + corpse eruption (warcry combined with corpse-explosion).
- **Cinder Leap / Ashbreaker Slam** — ground-impact AoE on landing/slam.
- **Anvilbreaker** — boss/champion stagger condition (conditional crowd-control).
- **Roar of Ruin** — lower-resist in an area (warcry carrying a curse-like effect).

**Shape of the work:** ~23 reskins + ~7 stitch-jobs. Warcries are the easiest tree in the whole class; Cinder Rage's triggers are where the work sits.
