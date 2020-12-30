# Blocks

<a href="https://minecraft.gamepedia.com/Block" target="_blank">Vanilla Wiki</a>

## Syntax

<pre class="styledpre">
{
  "type": "block",
  "flags": <a href="./../blocks#flags">Flag[]</a>,
  "name": String,
  "group": <a href="./../registries#tabgroup">TabGroup</a>,
  "rarity": <a href="./../registries#rarity">Rarity</a>,
  "stack": int,
  "material": <a href="./../registries#material">Material</a>,
  "sounds": <a href="./../registries#soundtype">SoundType</a>,
  "mapcolor": <a href="./../registries#mapcolor">MapColor</a>,
  "light": int,
  "resistance": float,
  "hardness": float,
  "slip": float,
  "harvester": <a href="./../bits#harvester">Harvester</a>
}
</pre>

### Required

* `type`: `"block"`
    * Type must be set to "block" for the entry to describe an block.
* `name`: `string`
    * The unique registry name for this block.

### Optional

* `flags`: `String[]`
    * An array of flag strings given in the format `["flag1", "flag2", ...]`.
    * For valid flags and their effects, see [Flags](./#flags)
    * Defaults to no activated flags.
* `group`: `TabGroup`
    * The Tab Group this belongs to in Creative mode.
    * Valid entries are given by the [Tab Group Registry](./../registries#tab-group).
    * Defaults to misc.
* `rarity`: `Rarity`
    * The color of this block's item's name, given as a rarity string.
    * Valid entries are given by the [Rarity Registry](./../registries#rarity).
    * Defaults to common.
* `stack`: `int`
    * The maximum stack size of this block's item.
    * Maximum is 64.
    * Minimum is 1.
    * Defaults to 64.
* `material`: `Material`
    * Determines the default map color, liquid, solid, solid blocking, block movement, can burn, can replace, and piston status of blocks.
    * Valid entries are given by the [Material Registry](./../registries#material).
    * Defaults to earth.
* `sounds`: `SoundType`
    * The types of sounds this block makes.
    * Valid entries are given by the [Sound Registry](./../registries#sound-type).
    * Defaults to stone.
* `mapcolor`: `MapColor`
    * The color this block makes when it shows up on a map.
    * Being empty causes this to be inherited from the material.
    * Valid entries are given by the [Material Color Registry](./../registries#material-color).
    * Defaults to empty.
* `light`: `int`
    * The amount of light this block makes.
    * Maximum is 15.
    * Minimum is 0.
    * Will automatically constrain to bounds if provided with a number outside the bounds.
    * Defaults to 0.
* `resistance`: `float`
    * The resistance this block has to an explosion.
    * Defaults to 0.
* `hardness`: `float`
    * How hard this block is to break, in seconds.
    * Using the proper tool reduces this time.
    * Defaults to 0.
* `slip`: `float`
    * The percentage of momentum this block allows to continue while an entity passes over it.
    * The maximum in vanilla is blue ice at .989.
    * Maximum is 0.999.
    * Minimum is 0.001.
    * Will automatically constrain to bounds if provided with a number outside the bounds.
    * -1.0 will ignore this property.
    * Defaults to -1.0.
* `harvester`: `Harvester`
    * The tool type that works on this block.
    * See [Harvester](../bits#harvester) for more information.
    * Defaults to empty.

### Flags
* `ghost`
    * Stops the block from blocking entity movement.
* `model`
    * Renders the block as though it wasn't a full block.
    * This fixes the x-ray issues you get with custom models.
* `lore`
    * Adds a line of lore to the block's item.
    * The lang entry will have a key of `block.jsonifycraft.[blockname].lore`.
* `shimmer`
    * Causes the block's item to shimmer, similarly to an enchanted item.

## Examples

* [Dirt](../examples/dirt)
* [Tall Grass](../examples/tallgrass)