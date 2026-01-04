# Mechanic - World Mana

__Type__ Resource, Function

World Mana is multiple systems present in the game that handle the mana cycle.

## Mana Cycle

```mermaid
flowchart LR
  clean_mana["Clean Mana"]
  dirty_mana["Dirty Mana"]

  abyss["Abyss"]
  world_tree["World Tree"]
  domain["Domain"]

  distributes@{shape: tri, label: "Distributes"}
  flows@{shape: tri, label: "Flows"}
  returns@{shape: tri, label: "Returns"}
  d2c@{shape: tri, label: "Cleans / Consumes"}
  c2d@{shape: tri, label: "Use / Depletes"}

  dirty_mana --> abyss --> d2c --> clean_mana --> world_tree --> distributes --> domain --> c2d --> flows --> world_tree --> returns --> dirty_mana
```

The Abyss provides clean mana to the domain or world keeping it charged.

When mana is consumed or used for magic or other applications, it is converted into negatively charged or dirty mana.

That dirty mana must then be returned to the abyss to receive new clean mana to replace it.

And that is the basics of the cycle, unfortunately, Harmonia doesn't have any actual sinks.

Players are therefore required to make sinks, typically mana filtering plants such as mushrooms.

## Scratchpad

As of this writing, 2026-01-02, mana would be generated per block and then spread over each block until it reaches equilibrium; this was fine when the mana system wasn't completely fleshed out and there was no "lore" behind it.

However with mana fleshed out as being tied to memories, it has almost zero reason to just "generate" out of the blue, it needs something, something that creates memory.
