# Core Systems

Foundational, whole-game decisions. These flow into every class, monster, and item, so they're locked here as pillars.

## Immunity system — REMOVED

**Decision: delete immunities, keep resistances.** (The ESR route.)

### What this means precisely

- **Immunities are gone.** No monster is ever fully unkillable by a given damage type. The ≥100% resist cap that creates an immunity is removed.
- **Resistances stay.** A fire elemental can still resist fire (e.g. 50%); an icy beast still shrugs off some cold. Resistance remains a *dial* — flavor and mild build pressure — but never a *wall*.
- **`-enemy resist` sources toned down.** Like ESR, item sources of minus-enemy-resistance are dialed back to compensate, so single-element builds are viable but you can't stack absurd `-res` to faceroll everything.

### Why

- **Legibility.** Immunities are the most illegible mechanic in D2. The hidden rule — that `-enemy resist` works at only ~1/5 effectiveness against an immune target until broken below 100 — is exactly the kind of invisible wall this mod exists to eliminate. (See [Design Philosophy](Design-Philosophy.md).)
- **Frees class design.** Cinder Veins classes are mono-element and flavor-driven (e.g. the fire/ash Sorceress). Immunities would punish the player for the thematic identity the mod hands them. Removing immunities lets cohesive single-element classes stay viable into the endgame.
- **Difficulty lives elsewhere.** Brutal difficulty comes from monster stat scaling, not from immunity gating — so removing immunities doesn't make the game soft, it just removes the *unfair-feeling* deaths.

### Note on the "attack style" idea (considered, set aside)

We considered re-theming immunities as **styles** (Immune to Melee / Ranged / Magic). Engine reality: D2 only tracks six damage **types** (Physical, Magic, Fire, Cold, Lightning, Poison), not delivery style. Melee and ranged are *both* Physical natively, so a true 3-way style split would require reassigning all ranged attacks to a separate damage type across every weapon and skill — a large systemic lift. Decided against it in favor of simply removing immunities. Revisit only if a style system becomes worth the cost later.

## Difficulty model — "Brutal from level 1"

- Difficulty comes from **monster stat scaling** (`monstats.txt` / `monlvl.txt`): higher level, life, damage, attack rating, and XP — cranked from Act 1, ESR-style.
- The difficulty must stay **legible** (see philosophy). Hard because enemies *hit hard*, never because rules are hidden.
- This is an **ongoing tuning pass**, revisited constantly through playtesting — not a one-time task.

## Attribute & level-up systems

*(Phase 1 — to be designed.)* Both are value-driven table edits (stat scaling, points-per-level, max level). Placeholder until built.
