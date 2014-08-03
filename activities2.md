#Additional ScriptCraft Commands to Test:

* A 3-block-wide road 100 blocks long:
<pre>/js box(blocks.cobblestone).right(1)times(2).fwd(1).left(2).times(100);</pre>

* A hollow cylinder of iron with a 10-block diameter and 30 blocks high:
<pre>/js cylinder0(blocks.iron, 10, 30);</pre>

* A village of 16 houses arranged in a 4x4 grid:
<pre>/js cottage().right(10).times(4).left(40).fwd(10).times(4);</pre>

* A rainbow:
<pre>/js rainbow()

* A message in large block letters made of glowstone:
<pre>/js blocktype("Your message", blocks.glowstone);</pre>
