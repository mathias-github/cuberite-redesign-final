---
sitemap: false
---
It is possible to configure many different aspects of individual worlds with Cuberite. Configuration options include:

- Changing the spawn point of a world.
- Changing the game mode of a world.
- Changing the world generator, so as to change the terrain generated.
- Changing the types of plants that generate in the world.
- Changing which types of animals are allowed to spawn.
- There are many more things that can be done, and these are just examples.

All this configuration can be done through one file. It is called ***world.ini*** and can be found in each world's individual folder. When a world is first created by Cuberite, the file is filled out with default values that are fairly close to vanilla Minecraft.

The ***world.ini*** file is split into many different sections, each with a name surrounded in square brackets. For example {{3.2 - <code>[SpawnPosition]</code>}} is a section. Each section contains configuration options related to a specific feature of Cuberite.

#### Default Settings

<div class="code-box">
[SpawnProtect]<br/>
ProtectRadius=10<br/>
<br/>
[WorldLimit]<br/>
LimitRadius=0<br/>
<br/>
[Difficulty]<br/>
WorldDifficulty=1<br/>
<br/>
[General]<br/>
Dimension=Overworld<br/>
IsDaylightCycleEnabled=1<br/>
Gamemode=1<br/>
Weather=0<br/>
TimeInTicks=188<br/>
<br/>
[Broadcasting]<br/>
BroadcastDeathMessages=1<br/>
BroadcastAchievementMessages=1<br/>
<br/>
[SpawnPosition]<br/>
MaxViewDistance=12<br/>
X=0.500000<br/>
Y=66.000000<br/>
Z=8.500000<br/>
PregenerateDistance=9<br/>
<br/>
[Storage]<br/>
Schema=Default<br/>
CompressionFactor=6<br/>
<br/>
[Plants]<br/>
MaxCactusHeight=3<br/>
MaxSugarcaneHeight=3<br/>
IsCactusBonemealable=0<br/>
IsCarrotsBonemealable=1<br/>
IsCropsBonemealable=1<br/>
IsGrassBonemealable=1<br/>
IsMelonStemBonemealable=1<br/>
IsMelonBonemealable=0<br/>
IsPotatoesBonemealable=1<br/>
IsPumpkinStemBonemealable=1<br/>
IsPumpkinBonemealable=0<br/>
IsSaplingBonemealable=1<br/>
IsSugarcaneBonemealable=0<br/>
<br/>
[Physics]<br/>
DeepSnow=1<br/>
ShouldLavaSpawnFire=1<br/>
TNTShrapnelLevel=2<br/>
WaterSimulator=Vanilla<br/>
LavaSimulator=Vanilla<br/>
SandInstantFall=0<br/>
RedstoneSimulator=Incremental<br/>
<br/>
[Mechanics]<br/>
CommandBlocksEnabled=0<br/>
PVPEnabled=1<br/>
UseChatPrefixes=1<br/>
MinNetherPortalWidth=2<br/>
MaxNetherPortalWidth=21<br/>
MinNetherPortalHeight=3<br/>
MaxNetherPortalHeight=21<br/>
<br/>
[Monsters]<br/>
VillagersShouldHarvestCrops=1<br/>
AnimalsOn=1<br/>
Types=bat, cavespider, chicken, cow, creeper, enderman, guardian, horse, mooshroom, ocelot, pig, rabbit, sheep, silverfish, skeleton, slime, spider, squid, wolf, zombie<br/>
<br/>
[Weather]<br/>
MaxSunnyTicks=180000<br/>
MinSunnyTicks=12000<br/>
MaxRainTicks=24000<br/>
MinRainTicks=12000<br/>
MaxThunderStormTicks=15600
MinThunderStormTicks=3600
<br/>
[LinkedWorlds]<br/>
NetherWorldName=world_nether<br/>
EndWorldName=world_end<br/>
<br/>
[Generator]<br/>
Generator=Composable<br/>
BiomeGen=Grown<br/>
ShapeGen=BiomalNoise3D<br/>
CompositionGen=Biomal<br/>
Finishers=RoughRavines, WormNestCaves, WaterLakes, WaterSprings, LavaLakes, LavaSprings, OreNests, Mineshafts, Trees, Villages, TallGrass, SprinkleFoliage, Ice, Snow, Lilypads, BottomLava, DeadBushes, NaturalPatches, PreSimulator, Animals<br/>
BiomeGenCacheSize=16<br/>
BiomeGenMultiCacheLength=128<br/>
SeaLevel=62<br/>
BiomalNoise3DFrequencyX=40.000000<br/>
BiomalNoise3DFrequencyY=40.000000<br/>
BiomalNoise3DFrequencyZ=40.000000<br/>
BiomalNoise3DBaseFrequencyX=40.000000<br/>
BiomalNoise3DBaseFrequencyZ=40.000000<br/>
BiomalNoise3DChoiceFrequencyX=40.000000<br/>
BiomalNoise3DChoiceFrequencyY=80.000000<br/>
BiomalNoise3DChoiceFrequencyZ=40.000000<br/>
BiomalNoise3DAirThreshold=0.000000<br/>
BiomalNoise3DNumChoiceOctaves=4<br/>
BiomalNoise3DNumDensityOctaves=6<br/>
BiomalNoise3DNumBaseOctaves=6<br/>
BiomalNoise3DBaseAmplitude=1.000000<br/>
CompositionGenCacheSize=64<br/>
RoughRavinesGridSize=256<br/>
RoughRavinesMaxOffset=128<br/>
RoughRavinesMaxSize=128<br/>
RoughRavinesMinSize=64<br/>
RoughRavinesMaxCenterWidth=8.000000<br/>
RoughRavinesMinCenterWidth=2.000000<br/>
RoughRavinesMaxRoughness=0.200000<br/>
RoughRavinesMinRoughness=0.050000<br/>
RoughRavinesMaxFloorHeightEdge=8.000000<br/>
RoughRavinesMinFloorHeightEdge=30.000000<br/>
RoughRavinesMaxFloorHeightCenter=20.000000<br/>
RoughRavinesMinFloorHeightCenter=6.000000<br/>
RoughRavinesMaxCeilingHeightEdge=56.000000<br/>
RoughRavinesMinCeilingHeightEdge=38.000000<br/>
RoughRavinesMaxCeilingHeightCenter=58.000000<br/>
RoughRavinesMinCeilingHeightCenter=36.000000<br/>
WormNestCavesSize=64<br/>
WormNestCavesGrid=96<br/>
WormNestMaxOffset=32<br/>
WaterLakesProbability=25<br/>
LavaLakesProbability=10<br/>
MineShaftsGridSize=512<br/>
MineShaftsMaxOffset=256<br/>
MineShaftsMaxSystemSize=160<br/>
MineShaftsChanceCorridor=600<br/>
MineShaftsChanceCrossing=200<br/>
MineShaftsChanceStaircase=200<br/>
VillageGridSize=384<br/>
VillageMaxOffset=128<br/>
VillageMaxDepth=2<br/>
VillageMaxSize=128<br/>
VillageMinDensity=50<br/>
VillageMaxDensity=80<br/>
VillagePrefabs=PlainsVillage, SandVillage<br/>
BottomLavaLevel=10<br/>
PreSimulatorFallingBlocks=1<br/>
PreSimulatorWater=1<br/>
PreSimulatorLava=1<br/>
<br/>
[WaterSimulator]<br/>
Falloff=1<br/>
TickDelay=5<br/>
NumNeighborsForSource=2<br/>
<br/>
[LavaSimulator]<br/>
Falloff=2<br/>
TickDelay=30<br/>
NumNeighborsForSource=-1<br/>
<br/>
[FireSimulator]<br/>
BurnStepTimeFuel=500<br/>
BurnStepTimeNonfuel=100<br/>
Flammability=50<br/>
ReplaceFuelChance=50000<br/>
<br/>
[Seed]<br/>
Seed=586392587<br/>
<br/>
[WaterSprings]<br/>
HeightDistribution=0, 0; 10, 10; 11, 75; 16, 83; 20, 83; 24, 78; 32, 62; 40, 40; 44, 15; 48, 7; 56, 2; 64, 1; 255, 0<br/>
Chance=24<br/>
<br/>
[LavaSprings]<br/>
HeightDistribution=0, 0; 10, 5; 11, 45; 48, 2; 64, 1; 255, 0<br/>
Chance=9<br/>
<br/>
[Animals]<br/>
AnimalSpawnChunkPercentage=10
</div>
