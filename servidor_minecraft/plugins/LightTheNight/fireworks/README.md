# Firework sets

* Place any number of `.yml` files in this `plugins/LightTheNight/fireworks` folder. The plugin loads every top-level key as a firework set id (for example `cluster-red`).
* Name a Blockbench bone `<boneName>_<setId>` to trigger the matching set when that bone is animated, or run `/ltn firework <setId>` to test it.
* Each set contains a `fireworks:` section where every entry fires together with optional `delay` values to stagger them.
* Offsets:
  * `xo`, `yo`, `zo` – global X/Y/Z offsets from the bone position.
  * `rx`, `ry` – rotation adjustments.
  * `fo`, `ho` – forward/back and up/down offsets based on the player's facing direction.
  * `so` – sideways offset relative to the facing direction (`+` right, `-` left).
* Other fields: `type`, `colors`, `fade`, `power`, `maxLife`/`life` (ticks), `trail`, `flicker`, `count`, `spread`, and `delay` (ticks).

Use these defaults as inspiration and create as many files as you like.

# 95877RWOP