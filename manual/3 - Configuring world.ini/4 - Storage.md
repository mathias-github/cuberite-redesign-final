---
sitemap: false
---
This section specifies if Cuberite should save world chunks or not, as well as the compression level for world files.

#### Available Options

| Variable          | Meaning                                                                                                                                                                                                                                                     | Default |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|
| Schema            | Specifies if world chunks should be saved or not. May be one of "Default", "Anvil" and "Forgetful". See table below for their description.                                                                                                                  | Default |
| CompressionFactor | How much the world files should be compressed. Lower values mean much larger file sizes, but slighly increased performance, and higher values mean slightly smaller file sizes and much lower performance. It is recommended just to keep with the default. | 6       |

#### Schema Options

| Schema    | File Type | Description                                                                                                                                                                                                           |
|-----------|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Default   | .mca      | This is just an alias for Anvil at the moment.                                                                                                                                                                        |
| Anvil     | .mca      | Saves chunks. Storage is compatible with other Minecraft-related tools and programs. MCA files are stored in the "region" subfolder of the world folder, and a "level.dat" file is generated inside the world folder. |
| Forgetful | N/A       | Doesn't save chunks. Changes to the world are lost as soon as the chunks are unloaded, making this useful for read-only public servers. Please note that Cuberite will still load chunks using other schemas.         |

#### Default Configuration

<pre>
[Storage]
Schema=Default
CompressionFactor=6
</pre>
