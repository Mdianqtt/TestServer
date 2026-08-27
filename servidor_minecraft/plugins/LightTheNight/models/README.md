# Adding Blockbench models

1. Put your `.bbmodel` files in this `plugins/LightTheNight/models` folder on the server (the plugin creates it automatically).
2. Reference the file path from a YAML sequence in `plugins/LightTheNight/sequences` (see that folder's README for the format).
3. Use `defaultBone` in your sequence to pick the origin bone for commands, and `animation` to choose the animation name inside the model.
4. Fireworks can be triggered from keyframe scripts or by naming bones with the `_groupId` suffix that matches a firework set in the `fireworks` folder. Scale keyframes that reach **1.0005** on those bones will also trigger their firework groups at the bone's relative position in-game.

Reload with `/ltn reload` after adding or updating models.