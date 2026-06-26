# Class: Druid

The **second full class revamp.** The Druid is reimagined as a **fire-nature hybrid** — scorched roots, burning wildlife, and fire-touched beast forms. The three original trees (Elemental / Shape Shifting / Summoning) are rethemed into **Wildfire Rites**, **Beastblood Forms**, and **Hearthroot Wards**.

## Identity & damage

- **Theme:** nature set ablaze — burning growth, molten beasts, and smoldering wards. A versatile, tanky hybrid.
- **Damage:** **Fire** from the spell and ward trees, plus **Physical** from the beast forms. Because immunities are removed (see [Core Systems](Core-Systems.md)), this mix is purely for flavor and playstyle variety, not coverage — but it does make the Druid naturally flexible between casting and melee.
- **Role contrast with the Sorceress:** where the Sorc is a glass cannon, the Druid is the **durable** fire user — shapeshift tankiness, ward/heal sustain, and retaliation defense.

## Signature mechanic — Burn & capitalize

Carries the mod's burning theme, with beast-form payoffs:

- **Charclaw Rend** — bonus damage to already-burning enemies.
- **Volcanic Bloom** / **Primal Furnace** — delayed and stacking fire detonations.
- Beast forms apply burn on hit, setting up the spell tree's burn-synergy skills.

## Survivability (the tanky fire user)

The Druid is *built* to survive — defensive options across two trees:

- **Molten Hide** — beast-form armor + fire resistance.
- **Stone-Sap Skin** — flat damage reduction.
- **Rootguard / Smoldering Renewal** — defense buff + life regen.
- **Worldroot Sanctuary** — capstone warded area: heal + slow + damage reduction.

---

## Tree 1 — Wildfire Rites *(replaces Elemental)*

| Skill | Description |
|-------|-------------|
| **Embervine** | Summons burning vines that lash enemies and deal fire damage over time. |
| **Cinder Swarm** | Releases a cloud of flaming insects that seek nearby enemies. |
| **Ashbark Growth** | Causes scorched roots to burst from the ground, damaging and slowing enemies. |
| **Wildfire Totem** | Places a fiery spirit totem that burns nearby enemies. |
| **Scorchleaf Gale** | Sends a gust of burning leaves forward, striking multiple enemies. |
| **Blazing Thorns** | Covers the Druid in burning briars, damaging enemies that hit him. |
| **Volcanic Bloom** | Grows a molten flower that erupts after a short delay. |
| **Cinderstorm** | Calls down a storm of ash, sparks, and fire over an area. |
| **Rootfire Maw** | Opens a fiery root-filled pit beneath enemies, trapping and burning them. |
| **Heart of Wildfire** | Temporarily empowers nature fire spells, adding splash burn and increased area damage. |

## Tree 2 — Beastblood Forms *(replaces Shape Shifting)*

| Skill | Description |
|-------|-------------|
| **Ashen Wolf Form** | Transform into a fast wolf with fire-touched melee attacks. |
| **Cinderbear Form** | Transform into a powerful bear with heavy burning strikes. |
| **Feral Ignite** | A claw attack that sets enemies ablaze. |
| **Bloodfang Rush** | Dash through enemies, biting and bleeding targets in your path. |
| **Molten Hide** | Hardens your beast form with volcanic armor, increasing defense and fire resistance. |
| **Howl of Embers** | Releases a fiery howl that frightens weaker enemies and boosts attack speed. |
| **Charclaw Rend** | A brutal claw strike that deals bonus damage to burning enemies. |
| **Primal Furnace** | Builds heat with each melee hit, releasing a fire burst at maximum stacks. |
| **Beastblood Frenzy** | Temporarily increases movement speed, attack speed, and life steal. |
| **Avatar of the Cinderbeast** | Ultimate transformation that enhances all beast attacks with fire explosions. |

## Tree 3 — Hearthroot Wards *(replaces Summoning)*

The defensive / sustain tree — protective roots, healing earth, and guardian spirits.

| Skill | Description |
|-------|-------------|
| **Rootguard** | Summons protective roots around the Druid, increasing defense. |
| **Stone-Sap Skin** | Coats the Druid in hardened bark and mineral sap, reducing damage taken. |
| **Hearthroot Circle** | Creates a healing circle of warm roots and glowing earth. |
| **Ashen Bulwark** | Raises a wall of scorched roots and stone to block enemies. |
| **Cinderseed Ward** | Plants a seed that heals allies and burns enemies nearby. |
| **Guardian Briar** | Summons thorny roots that retaliate against attackers. |
| **Earthen Pulse** | Sends a pulse through the ground, knocking back nearby enemies. |
| **Smoldering Renewal** | Restores life over time and grants temporary fire resistance. |
| **Ancient Root Spirit** | Summons a protective nature spirit that absorbs damage. |
| **Worldroot Sanctuary** | Creates a large warded area that heals allies, slows enemies, and reduces incoming damage. |

---

## Implementation notes

Same rule as always: **recombine existing skill functions**, swap FX freely. The Druid has unusually good native bones to build on — he already has shapeshift, summons, and fire/earth elemental skills (Armageddon, Volcano, Fissure, Cyclone Armor, Oak Sage, etc.).

### Easy reskins (the bulk)

- **Elemental fire:** Cinderstorm (Armageddon), Rootfire Maw / Ashbark Growth (Volcano / Fissure bones), Scorchleaf Gale (Twister / Tornado), Embervine (Fire Wall-style ground DoT), Heart of Wildfire (self-buff).
- **Beast forms:** Ashen Wolf / Cinderbear (Werewolf / Werebear), Feral Ignite (Feral Rage / Maul + fire), Beastblood Frenzy (Feral Rage buff), Molten Hide (shapeshift defensive buff), Howl of Embers (Howl + buff).
- **Wards / summons:** Rootguard, Stone-Sap Skin (Cyclone Armor), Smoldering Renewal & Ancient Root Spirit (Oak Sage / Spirit Wolf bones), Hearthroot Circle (heal aura), Guardian Briar (Thorns-style).

### Stitch-jobs (the puzzles)

- **Primal Furnace** — stacking "heat" charge-up that bursts at max. No native Druid stack mechanic; fake it with a charge-up system (Assassin charge-skill bones) + triggered burst. *(Hardest.)*
- **Volcanic Bloom** — delayed-erupt flower (timed-trigger explosion).
- **Charclaw Rend** — conditional bonus vs *burning* targets (the condition check is the stitch).
- **Bloodfang Rush** — dash-through attack (no native Druid dash; Leap / Charge-style movement + bleed).
- **Cinderseed Ward / Worldroot Sanctuary** — dual/multi-effect ground zones (heal allies *and* burn/slow enemies in one area).
- **Wildfire Totem** — stationary burning summon (turret-style summon behavior).

**Shape of the work:** the strong native foundation means even more of this is reskins than the Sorc — roughly ~24 reskins + ~6 stitch-jobs, with Primal Furnace the one real head-scratcher.
