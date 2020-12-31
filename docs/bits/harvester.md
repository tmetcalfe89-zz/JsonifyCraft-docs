# Harvester

## Syntax

<pre class="styledpre">
{
  "tool": <a href="./../registries/tooltype">ToolType</a>,
  "level": int
}
</pre>

### Required
* `tool`: `ToolType`
    * The type of tool for this harvester.
    * Valid entries are given by the [Tool Type Registry](./../registries/tooltype).

### Optional
* `level`: `int`
  * The tier of tool for this harvester.
  * Defaults to 0.
