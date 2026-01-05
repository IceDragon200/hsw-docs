# Mechanic - Metallurgy

```mermaid
flowchart TD
  bloom["Bloom"]
  dust["Dust"]
  dirty_dust["Dirty Dust"]
  ingot["Ingot"]
  lump["Lump"]
  nugget["Nugget"]
  ore["Ore"]
  shards["Shards"]
  enriched_shards["Enriched Shards"]
  shavings["Shavings"]
  slag["Slag"]
  molten_metal["Molten Metal"]
  grit["Grit"]
  machine_parts["Machine Parts"]
  tool_parts["Tool Parts"]
  plate["Plate"]

  break@{shape: tri, label: "Break"}
  crack@{shape: tri, label: "Crack"}
  crush@{shape: tri, label: "Crush"}
  dirty_crush@{shape: tri, label: "Dirty Crush"}
  smelt@{shape: tri, label: "Smelt"}
  dirty_smelt@{shape: tri, label: "Dirty Smelt"}
  shard_smelt@{shape: tri, label: "Shard Smelt"}
  shaving_smelt@{shape: tri, label: "Shaving Smelt"}
  shape@{shape: tri, label: "Shape"}
  cast@{shape: tri, label: "Cast"}
  enrich@{shape: tri, label: "Enrich"}
  blend@{shape: tri, label: "Blend"}
  wash@{shape: tri, label: "Wash"}

  ore --> break --> shards & ore & grit
  grit & shards --> crush --> dust
  enriched_shards & shards --> shard_smelt --> bloom --> crack --> lump & slag
  slag --> dirty_crush --> grit & dirty_dust
  shards --> enrich --> enriched_shards --> dirty_crush --> dirty_dust --> wash --> dust & grit

  dust --> blend --> dust
  nugget & shavings & lump & ingot & plate & dust --> smelt --> lump & molten_metal
  dirty_dust --> dirty_smelt --> bloom

  lump --> shape --> ingot & plate & machine_parts & shavings
  shavings --> shaving_smelt --> nugget
  molten_metal --> cast --> ingot & tool_parts & machine_parts
```

If that graph was a little intimidating, don't worry it's rather straight forward.

## Ore, Shards, and Grit

Players will start off typically with some metal ore:

* Ore bearing stones (Iron in Stone)
* Mixed material ores (Carrollite)
* Pure material ores (Raw Iron)

These are broken down into Shards, leftover Ore or Grit.

Shards represent a "pure" piece of unrefined metal, and are the base unit for additional processing.

Grit is similar to shard, but usually in smaller amounts, but most time Stone Grit is the byproduct, which is not useful in this context.

Leftover ores typically happen with Mixed Material Ores, such as breaking off Cobalt Shards from Carrollite which leaves copper and sulphur.

Note that Breaking is done with a Hammer at a Workbench, or an equivalent machine or magical contraption.

## Bloom, Lump, and Slag

For early progression further refinement may prove difficult or even process, so Shards can be processed into their respective Blooms and cracked with a Hammer to produce their Lump and respective Slag.

Lumps can be considered the pre-final form of refined metal and cannot be doubled, but can be processed into other materials at this stage.

Slag however proves more useless early on, but can be recycled and refined to extract additional metal from the same yield.

## Enrichment, Dirty Shards, Dirty Dust, Washing

Once access to additional metal processing machines and techniques become available, players can enrich their shards before processing to increase their yield.

However until the material is washed it will continue to produce large amounts of Slag if it is ever smelted.

## Dust Blends

One may have noticed the small loop in the graph above where Dust Blends into more Dust.

This is the alloying blend, such as mixing copper and tin to produce bronze dust.

Note, you cannot mix Dirty Dusts into Dirty Alloy Dusts, that isn't a thing.

## Smelting, and Casting

The process of Shard/Dust to Lump is typically done in a simple early game furnace, it is by no means inefficient, it simply produces a solid Lump that can be used immediately.

However, the [Smelter](../devices/smelter.md) takes most metallic inputs and produces its Molten (fluid) form which can be cast into other materials except Lumps.

## Shaping

While not directly part of the smelting process, Lumps can be shaped into other materials without the need for casting primarily in the [Roller](../devices/roller.md) with the appropriate [Die](roller.md#dies).
