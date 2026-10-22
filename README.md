# Chassis: Limbs

Content mod of the **Chassis** mod family for **Minecraft 1.21.1 (NeoForge 21.1.262)**:
a seven-part body system with per-limb health pools, dismemberment, damage propagation,
a configurable death lock, a tactical HUD, healing items and in-game self-tests.

This repository is a release/distribution home: the built jar is published under
[Releases](https://github.com/woshixiaotiao/chassis-limb/releases). Source code is not
mirrored here yet.

## What it does

- **Seven-part body** (head, chest, abdomen, two arms, two legs) with bleeding, pain,
  bone integrity and infection values per part.
- **Part-based damage routing**: precise projectile entry points > melee line-of-sight
  geometry > weighted pseudo-random fallback.
- **Dismemberment**: massive, instant and accumulated damage can sever limbs; damage
  propagates along the body chain (limbs → abdomen → chest) and hits on severed parts
  spill upward to living parts instead of being absorbed.
- **Death lock**: body health is clamped to 1 HP; death is released only when a lethal
  part (head/chest) is actually destroyed. Configurable (players / all living entities,
  any/all modes).
- **HUD**: six templates (TARKOV / CLASSIC / MINIMAL / PIXEL / REALISTIC / DATA), target
  panel with progressive identification, persistent doll and aim hint.
- **Healing**: 19 items across 4 tiers with biome variants, loot drops and combat pacing.
- **Performance**: combat heat tracking and budget tokens; verify self-tests in game.

## Requirements

- Minecraft 1.21.1, NeoForge 21.1.262+, Java 21.
- **Chassis: API** (`chassis-api`) — required library mod:
  <https://github.com/woshixiaotiao/chassis-api/releases>
- Optional, detected at runtime: TaCZ (guns), Jade (body tooltips).

## Install

Put **both** jars into your `mods` folder:

- `chassis-limb-0.1.0-a.jar` (this mod)
- `chassis-api-0.1.0-a.jar` (required companion library)

## Downloads

- This repository: <https://github.com/woshixiaotiao/chassis-limb/releases>
- Companion library: <https://github.com/woshixiaotiao/chassis-api/releases>

Verify downloads with `SHA256SUMS` (attached to every release).