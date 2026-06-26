# Class: Paladin

**Fourth class revamp.** The Paladin becomes a **holy-fire crusader** — sacred flame, ash-forged wards, and blessed burning melee. Original trees (Combat / Offensive Auras / Defensive Auras) are reimagined as **Cinder Oaths**, **Ashen Bulwarks**, and **Sanctified Arms**.

## Identity & damage

- **Theme:** sacred fire — holy flame that burns harder against the undead and demonic.
- **Damage:** **Fire** and **Magic** (holy fire), plus **Physical** from the melee tree.
- **Role:** the frontline holy bruiser. Tanky like the Druid, but support-leaning — auras and wards that protect allies (strong in co-op).

## Signature mechanic — Brand & burn

- **Brand of Penance / Branding Smite** — mark enemies for bonus fire and magic damage.
- **Final Oath** — slain enemies explode in sacred flame (the burn-detonate theme).
- **Vow of Embers / Consecrated Edge** — weapon-imbue buffs that add holy fire on hit.

## Survivability (the protector)

An entire tree is defense, and it shields allies too:

- **Molten Aegis / Cinder Shield** — damage reduction + retaliation.
- **Hearthlight Blessing** — heal-over-time for self and allies (Prayer lineage).
- **Citadel of Ash** — capstone zone: enemy damage down, ally resist up, attackers burn.

---

## Tree 1 — Cinder Oaths *(replaces Offensive Auras)*

| Skill | Description |
|-------|-------------|
| **Oathfire Bolt** | Launches a sacred ember projectile that burns undead and demons harder. |
| **Judgment Flame** | Calls down a pillar of holy fire on a target area. |
| **Brand of Penance** | Marks an enemy, causing them to take bonus fire and magic damage. |
| **Cleansing Pyre** | Burns away poison and curses while damaging nearby enemies. |
| **Ashen Verdict** | Releases a cone of radiant ash that blinds and burns enemies. |
| **Vow of Embers** | Temporarily adds holy fire damage to your attacks. |
| **Martyr's Blaze** | Sacrifices a portion of life to unleash a strong fire burst around you. |
| **Sacred Cinders** | Creates lingering holy embers on the ground that damage enemies over time. |
| **Wrath of the Furnace Saint** | Strikes enemies with repeated waves of molten holy fire. |
| **Final Oath** | A powerful ultimate vow that greatly boosts holy fire spells and causes slain enemies to explode in sacred flame. |

## Tree 2 — Ashen Bulwarks *(replaces Defensive Auras)*

| Skill | Description |
|-------|-------------|
| **Cinder Shield** | Forms a glowing shield of ash and holy fire, increasing defense. |
| **Sanctuary Ward** | Creates a holy circle that pushes back undead and weakens demons. |
| **Molten Aegis** | Reduces incoming damage and burns melee attackers. |
| **Ashguard Aura** | Grants nearby allies fire resistance and minor damage reduction. |
| **Purge Aura** | Slowly removes poison, curses, and negative effects from allies. |
| **Shield of the Faithful** | Blocks the next heavy hit and releases a holy shockwave. |
| **Hearthlight Blessing** | Restores life over time to the Paladin and nearby allies. |
| **Iron Vow** | Temporarily increases block chance, defense, and resistance. |
| **Bulwark of Saints** | Summons spectral shields around allies, reducing damage taken. |
| **Citadel of Ash** | Creates a large protective zone that reduces enemy damage, boosts ally resistance, and burns attackers. |

## Tree 3 — Sanctified Arms *(replaces Combat Skills)*

| Skill | Description |
|-------|-------------|
| **Cinder Strike** | A basic blessed melee attack that adds fire damage. |
| **Zeal of Ash** | Rapidly strikes nearby enemies with ember-charged weapon attacks. |
| **Hammer of Embers** | Throws a spinning holy hammer that leaves a fiery trail. |
| **Branding Smite** | Shield-bashes an enemy and brands them with holy flame. |
| **Consecrated Edge** | Empowers your weapon with radiant heat, increasing damage against undead. |
| **Ashen Charge** | Charges forward, slamming into enemies and leaving burning ground behind. |
| **Crusader's Reprisal** | Counterattacks after blocking, dealing bonus holy fire damage. |
| **Furnace Zeal** | Each successful hit builds heat, increasing attack speed and fire damage. |
| **Solar Cleave** | Sweeps your weapon in a wide arc of bright, burning light. |
| **Saintfire Ascension** | Temporarily empowers all melee skills with splash damage, holy fire, and increased attack speed. |

---

## Implementation notes

The Paladin's native kit (auras, Blessed Hammer, Smite, Charge, Zeal, Holy Fire) maps onto this cleanly.

### Easy reskins (the bulk)

- **Cinder Oaths:** Oathfire Bolt (Holy Bolt), Judgment Flame (Fist of Heavens-style pillar), Sacred Cinders (ground DoT), Vow of Embers (Holy Fire imbue), Cleansing Pyre (Cleansing + damage), Wrath of the Furnace Saint (Fist of Heavens waves).
- **Ashen Bulwarks:** these are **auras** almost 1:1 — Ashguard Aura (Resist Fire / Salvation), Purge Aura (Cleansing), Hearthlight Blessing (Prayer), Iron Vow (Defiance), Sanctuary Ward (Sanctuary), Cinder Shield / Molten Aegis (defensive buffs).
- **Sanctified Arms:** Cinder Strike (basic + fire), Zeal of Ash (Zeal), Hammer of Embers (Blessed Hammer), Branding Smite (Smite), Ashen Charge (Charge), Consecrated Edge (weapon imbue), Solar Cleave (wide melee arc).

### Stitch-jobs (the puzzles)

- **Martyr's Blaze** — life-sacrifice burst (consume-life-for-effect; Sacrifice/Blood-style trigger).
- **Final Oath** — ultimate buff + slain-enemy explosion (buff + on-death-detonate).
- **Shield of the Faithful** — block-the-next-hit then shockwave (block-trigger reaction).
- **Crusader's Reprisal** — counterattack *after blocking* (block-trigger again).
- **Furnace Zeal** — stacking "heat" charge-up (same charge-up stitch as the Druid's Primal Furnace — see note below).
- **Bulwark of Saints / Citadel of Ash** — ally-targeted protective auras/zones (multi-target ally buff).

> **Cross-class note:** "build heat per hit, release at max" appears on Druid (**Primal Furnace**), Paladin (**Furnace Zeal**), and Assassin (**Furnace Zeal**-style finishers). Build the charge-up mechanic **once**, reuse everywhere. The Assassin natively has this (see [Class: Assassin](Class-Assassin.md)) — borrow that implementation for the others.
