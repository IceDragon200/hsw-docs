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

