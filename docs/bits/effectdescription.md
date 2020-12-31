# Effect Description

## Syntax

<pre class="styledpre">
{
  "effect": <a href="./../registries/effectregistry">Effect</a>,
  "duration": int,
  "amplifier": int,
  "probability": float
}
</pre>

### Required

* `effect`: `Effect`
    * The effect this effect description describes.
    * Valid entries are given by the [Effect Registry](./../registries/effectregistry).
* `duration`: `int`
    * The number of game ticks to apply this effect for.
* `amplifier`: `int`
    * The tier of the effect to apply.

### Optional
* `probability`: `float`
    * The chance for this effect to occur.
    * Maximum is 1.
    * Minimum is 0.
    * Defaults to 1, or 100%.
