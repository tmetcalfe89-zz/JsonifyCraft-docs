# Items

<a href="https://minecraft.gamepedia.com/Item" target="_blank">Vanilla Wiki</a>

## Syntax

<pre class="styledpre">
{
  "type": "item",
  "flags": <a href="./../items#flags">Flag[]</a>,
  "name": String,
  "group": <a href="./../registries#tabgroup">TabGroup</a>,
  "rarity": <a href="./../registries#rarity">Rarity</a>,
  "stack": int
}
</pre>

### Required

* `type`: `"item"`
    * Type must be set to "item" for the entry to describe an block.
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

### Flags
* `lore`
    * Adds a line of lore to the block's item.
    * The lang entry will have a key of `block.jsonifycraft.[blockname].lore`.
* `shimmer`
    * Causes the block's item to shimmer, similarly to an enchanted item.
