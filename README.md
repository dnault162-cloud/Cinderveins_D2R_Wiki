# Cinder Veins — D2R Total Conversion

Cinder Veins is a total-conversion mod for **Diablo II: Resurrected**, built on the **D2RLAN** loader. It takes inspiration from the depth of large mods like Eastern Sun Resurrected, but rebuilt from the ground up with its own systems, classes, items, and identity.

> **Design thesis:** Brutal, but legible. The game should try to kill you from level 1 — but you should always understand *why* you died.

This wiki is both the **design bible** (while building) and the **player reference** (at release). Same content, two lives.

---

## Start here

- [Design Philosophy](Design-Philosophy.md) — the core "brutal but legible" thesis and what we learned from ESR.
- [Roadmap & Build Order](Roadmap.md) — the phased plan; what's built, what's next.
- [Core Systems](Core-Systems.md) — immunity/resistance rework, difficulty model, foundational decisions.
- [Class: Sorceress](Class-Sorceress.md) — the first full class revamp. Three new trees, 30 custom skills.
- [Endgame: GR Portals](Endgame-GR-Portals.md) — the capstone rift system (vision capture; built last).
- [Toolchain & Dev Setup](Toolchain.md) — tools, repo layout, key data files.

---

## Status

**Current phase:** Phase 0 — Tooling & repo setup.

**Decisions locked so far:**

- Built on **D2RLAN** (multiplayer-capable loader, ESR's base).
- Immunity system **removed**; resistances kept. See [Core Systems](Core-Systems.md).
- **All seven classes drafted** (30 skills each, 210 total): [Sorceress](Class-Sorceress.md), [Druid](Class-Druid.md), [Necromancer](Class-Necromancer.md), [Paladin](Class-Paladin.md), [Assassin](Class-Assassin.md), [Barbarian](Class-Barbarian.md), [Amazon](Class-Amazon.md). First *built* class: Sorceress.
- Endgame: custom **GR-style rift portals** gated by keys from specific enemies. See [Endgame](Endgame-GR-Portals.md).
