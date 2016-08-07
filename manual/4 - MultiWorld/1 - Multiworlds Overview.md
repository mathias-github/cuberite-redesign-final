---
sitemap: false
---
Cuberite supports multiple worlds. Each world has its own ***world.ini*** file. Additional Worlds can be added by editing ***settings.ini***. This is explained in the example below.

#### Adding Worlds

<div class="code-box">
[Worlds]<br/>
DefaultWorld=world<br/>
World=world_nether<br/>
World=world_end<br/>
World=myNewWorld<br/>
World=HappyLand<br/>
</div>

In the example above, 2 extra worlds are added to the server. Note that this automatically creates 2 additional configuration files, namely ***myNewWorld/world.ini*** and ***HappyLand/world.ini***.

#### Dimensions (World types)

To create a nether type world, you should append the ***_nether*** suffix to your world name, e.g. ***World=myHellishWorld_nether***. This creates a ***world.ini*** preconfigured as a nether. For end worlds, the same rules apply, append the ***_end*** suffix to your world name. Once a default ***world.ini*** is created, you are free to tweak it to your liking.

The ***_nether*** and ***_end*** suffixes are only used when no ***world.ini*** exists, and guide the server in choosing the contents of the default world.ini it's about to create. When a world.ini is present, the suffixes do not matter any more and the dimension is dictated by the ***Dimension*** option inside each ***world.ini***.

The rest of this section deals with linking worlds and travelling between them.
