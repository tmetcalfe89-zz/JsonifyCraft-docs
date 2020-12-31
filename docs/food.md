# Food

<a href="https://minecraft.gamepedia.com/Food" target="_blank">Vanilla Wiki</a>

## Syntax

<pre class="styledpre">
{
  "type": "food",
  "flags": <a href="./blocks#flags">Flag[]</a>,
  "name": String,
  "group": <a href="./../registries/tabgroup">TabGroup</a>,
  "rarity": <a href="./../registries/rarity">Rarity</a>,
  "stack": int,
  "hunger": int,
  "saturation": float,
  "meat": boolean,
  "canEatWhenFull": boolean,
  "fastToEat": boolean,
  "effects": <a href="./../bits/effectdescription">EffectDescription[]</a>
}
</pre>

### Required

* `type`: `"food"`
    * Type must be set to "food" for the entry to describe a food.
* `name`: `string`
    * The unique registry name for this food.
* `hunger`: `int`
    * The number of half-hunger shanks to restore when this food is eaten.
* `saturation`: `float`
    * The saturation ratio of this food.
* `meat`: `boolean`
    * Whether or not this food is meat.
    * If true, this can be fed to wolves.
* `canEatWhenFull`: `boolean`
    * Whether or not this food can be eaten when a player's hunger bar is full.
* `fastToEat`: `boolean`
    * Whether or not this food takes half as long as normal food to eat.

### Optional

* `flags`: `String[]`
    * An array of flag strings given in the format `["flag1", "flag2", ...]`.
    * For valid flags and their effects, see [Flags](./#flags)
    * Defaults to no activated flags.
* `group`: `TabGroup`
    * The Tab Group this belongs to in Creative mode.
    * Valid entries are given by the [Tab Group Registry](./../registries/tabgroup).
    * Defaults to misc.
* `rarity`: `Rarity`
    * The color of this food's name, given as a rarity string.
    * Valid entries are given by the [Rarity Registry](./../registries/rarity).
    * Defaults to common.
* `stack`: `int`
    * The maximum stack size of this food.
    * Maximum is 64.
    * Minimum is 1.
    * Defaults to 64.
* `effects`: `EffectDescription[]`
    * An array of effect descriptions detailing what effects the player incurs after eating.
    * See [Effect Description](../bits/effectdescription) for more information.
    * Defaults to empty.

### Flags
* `lore`
    * Adds a line of lore to the food.
    * The lang entry will have a key of `block.jsonifycraft.[blockname].lore`.
* `shimmer`
    * Causes the food to shimmer, similarly to an enchanted item.
