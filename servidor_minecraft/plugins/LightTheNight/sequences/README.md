# Animation sequences and model setup

Place one YAML file per animation sequence in this `plugins/LightTheNight/sequences` folder. Each file describes a model to load, the animation to play, and how it should be triggered.

**Example structure**
```yml
id: celebration
file: "models/celebrate.bbmodel"
defaultBone: "RocketOrigin"
animation: "LaunchSequence"
speed: 1.0
preventDamage: true
triggers:
  - command
```

## Scale-based firework triggers
- Inside your Blockbench animation, add scale keyframes that reach a value of `1.0005` on the bones you want to fire from.
- Name those bones with the suffix `_<fireworkGroup>` (for example, `RocketOrigin_cluster-red`).
- When the animation hits that scale keyframe, the plugin reads the triggering bone, calculates its position relative to the sequence's `defaultBone`, and launches the matching firework group at that relative spot in the world.

## Damage control
- Set `preventDamage: true` on a sequence to cancel any damage caused by its fireworks, making them purely visual.
- Even when damage is allowed, LightTheNight adds an identifying tag to each firework it spawns so other plugins can react to them if needed.

## Dropping in models
1. Put your `.bbmodel` files in `plugins/LightTheNight/models`.
2. Reference them from your sequence YAMLs using the `file` path relative to the plugin folder (e.g., `models/your-model.bbmodel`).
3. Reload the plugin with `/ltn reload` after adding or editing sequence files.