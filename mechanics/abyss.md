# Mechanic - Abyss

__Type__ System

The Abyss is not a place one goes to, but rather a container one lives in, when one makes reference to "go" to the abyss, the actual intent is to travel to the spaces between contained domains within the Abyss itself.

Technically speaking, the Abyss itself is a Domain which contains all other domains.

The Abyss has several functions, but most boil down to recycling resources.

In lore Mana is a finite resource, but is so abundant and its absence basically marks the end of life within an Abyss all together.

But for the purpose of HSW, mana is treated as basically infinite (mostly because I don't feel like doing any form of accounting on mana usage as it's heavily error prone in a highly destructive world).

## Function

The abyss is an invisible system to the player mostly, but performs a handful of things:

* Stores a massive global pool of mana that changes every tick
  * This includes a pool of Clean Mana which blocks can pull from
  * A pool of Dirty Mana extracted from blocks and will be converted back to clean mana
* Stores a global pool of spirits recovered from blocks
  * Some spirits will ultimately be deleted from the world as a whole (i.e. purification)
  * Some will have their stats stripped and then placed back on the list of spirits that can return
  * New spirits can be randomly created at any time, but will not exceed a certain threshold

## Scratchpad

Originally the Abyss was suppose to be just a "lore" thing that simply gets referenced everywhere.

But gradually, it started to make sense to make it a background system that actually does things.

## Related

* [Mana](mana.md)
* [Spirit](spirit.md)
