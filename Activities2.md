###Some additional ScriptCraft commands to test:

* A 3-block-wide road 100 blocks long:
/js box(blocks.cobblestone).right(1)times(2).fwd(1).left(2).times(100);

* A hollow cylinder of iron with a 10-block diameter and 30 blocks high:
/js cylinder0(blocks.iron, 10, 30)

*A village of 16 houses arranged in a 4x4 grid:
/js cottage().right(10).times(4).left(40).fwd(10).times(4)

*A rainbow:
/js rainbow()

*A message in large block letters made of glowstone:
/js blocktype("Your message", blocks.glowstone)
