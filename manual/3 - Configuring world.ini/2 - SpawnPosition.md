---
sitemap: false
---
Specifies the spawn point for new players. The coordinates are absolute, in blocks, and may be fractional. If any of the values are missing, Cuberite provides a default.

#### Available Options

| Variable             | Meaning                                    | Default                                                  |
|----------------------|--------------------------------------------|----------------------------------------------------------|
| `Variable: `X        | `Meaning: `X coordinate of the spawn point | `Default: `32                                            |
| `Variable: `Y        | `Meaning: `Y coordinate of the spawn point | `Default: `The height of the terrain at the point (X, Z) |
| `Variable: `Z        | `Meaning: `Z coordinate of the spawn point | `Default: `32                                            |

#### Default Configuration

<div class="code-box">
[SpawnPosition]<br/>
MaxViewDistance=12<br/>
X=32.000000<br/>
Y=62.600000<br/>
Z=32.000000<br/>
PregenerateDistance=20
</div>
