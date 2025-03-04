---
title: Vanilla Usage Spawn Rules
category: Documentation
---

# Spawn Rules

In Minecraft Bedrock Edition, spawn rules for most of the entities are data driven which allows you to adjust the spawn conditions of entities including new entities added to the game to spawn naturally. There are some entities such as the dragons that cannot be changed.

A basic spawn rule must always contain a population control. There is no way to add custom population controls into the game so you have to choose from one of the following:

-   animal
-   water_animal
-   monster
-   cat
-   villager
-   pillager

Although these are the available options within the game, some of them do come with pre-set conditions, for example the cat population rules and limits are based upon the amount within a village and not within the simulation distance.

Once a population control has been defined you can refine the spawning conditions with the components listed below.

# minecraft:biome_filter

This component is used to specify which biomes the entity can spawn in. A current known list of biomes and the tags used in them are located [here](https://wiki.bedrock.dev/world-generation/biome-tags.html)

Below is all the areas where this is used in the vanilla files.

### bat

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/bat.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "animal"
}
```

### bee

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/bee.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": [
    {
        "test": "has_biome_tag",
        "operator": "==",
        "value": "plains"
    },
    {
        "test": "has_biome_tag",
        "operator": "==",
        "value": "sunflower_plains"
    },
    {
        "test": "has_biome_tag",
        "operator": "==",
        "value": "flower_forest"
    }
]
```

### chicken

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/chicken.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "animal"
}
```

### cod

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/cod.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": [
    {
        "test": "has_biome_tag",
        "operator": "==",
        "value": "ocean"
    },
    {
        "test": "has_biome_tag",
        "operator": "!=",
        "value": "warm"
    }
]
```

### cow

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/cow.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "animal"
}
```

### creeper

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/creeper.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "monster"
}
```

### dolphin

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/dolphin.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": [
    {
        "test": "has_biome_tag",
        "operator": "==",
        "value": "ocean"
    },
    {
        "test": "has_biome_tag",
        "operator": "!=",
        "value": "frozen"
    }
]
```

### donkey

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/donkey.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "plains"
}
```

### drowned

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/drowned.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "ocean"
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "river"
}
```

### enderman

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/enderman.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "monster"
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "all_of": [
        {
            "test": "has_biome_tag",
            "operator": "==",
            "value": "nether"
        },
        {
            "test": "has_biome_tag",
            "operator": "==",
            "value": "spawn_endermen"
        }
    ]
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "warped_forest"
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": [
    {
        "test": "has_biome_tag",
        "operator": "==",
        "value": "the_end"
    }
]
```

### fox

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/fox.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "taiga"
}
```

### ghast

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/ghast.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "all_of": [
        {
            "test": "has_biome_tag",
            "operator": "==",
            "value": "nether"
        },
        {
            "test": "has_biome_tag",
            "operator": "==",
            "value": "spawn_ghast"
        }
    ]
}
```

### goat

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/goat.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "extreme_hills"
}
```

### hoglin

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/hoglin.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "crimson_forest"
}
```

### horse

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/horse.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "plains"
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "savanna"
}
```

### husk

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/husk.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "desert"
}
```

### llama

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/llama.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "extreme_hills"
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "savanna"
}
```

### magma_cube

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/magma_cube.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "spawn_magma_cubes"
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "spawn_many_magma_cubes"
}
```

### mooshroom

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/mooshroom.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "mooshroom_island"
}
```

### ocelot

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/ocelot.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "jungle"
}
```

### panda

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/panda.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": [
    {
        "test": "has_biome_tag",
        "operator": "==",
        "value": "jungle"
    },
    {
        "test": "has_biome_tag",
        "operator": "!=",
        "value": "bamboo"
    }
]
```

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "bamboo"
}
```

### parrot

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/parrot.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "jungle"
}
```

### phantom

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/phantom.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "monster"
}
```

### pig

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/pig.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "animal"
}
```

### piglin

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/piglin.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "spawn_piglin"
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "spawn_few_piglins"
}
```

### pillager_patrol

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/pillager_patrol.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "all_of": [
        {
            "test": "has_biome_tag",
            "operator": "!=",
            "value": "mooshroom_island"
        },
        {
            "test": "has_biome_tag",
            "operator": "!=",
            "value": "nether"
        },
        {
            "test": "has_biome_tag",
            "operator": "!=",
            "value": "the_end"
        }
    ]
}
```

### polar_bear

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/polar_bear.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": [
    {
        "test": "has_biome_tag",
        "operator": "==",
        "value": "frozen"
    },
    {
        "test": "has_biome_tag",
        "operator": "!=",
        "value": "ocean"
    }
]
```

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": [
    {
        "test": "has_biome_tag",
        "operator": "==",
        "value": "frozen"
    },
    {
        "test": "has_biome_tag",
        "operator": "==",
        "value": "ocean"
    }
]
```

### pufferfish

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/pufferfish.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": [
    {
        "test": "has_biome_tag",
        "operator": "==",
        "value": "ocean"
    },
    {
        "test": "has_biome_tag",
        "operator": "==",
        "value": "warm"
    }
]
```

### rabbit

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/rabbit.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "any_of": [
        {
            "all_of": [
                {
                    "test": "has_biome_tag",
                    "operator": "==",
                    "value": "taiga"
                },
                {
                    "test": "has_biome_tag",
                    "operator": "!=",
                    "value": "mega"
                }
            ]
        },
        {
            "test": "is_snow_covered",
            "operator": "==",
            "value": true
        },
        {
            "test": "has_biome_tag",
            "operator": "==",
            "value": "desert"
        }
    ]
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "flower_forest"
}
```

### salmon

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/salmon.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": [
    {
        "test": "has_biome_tag",
        "operator": "==",
        "value": "ocean"
    },
    {
        "test": "has_biome_tag",
        "operator": "!=",
        "value": "warm"
    }
]
```

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": [
    {
        "test": "has_biome_tag",
        "operator": "==",
        "value": "river"
    }
]
```

### sheep

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/sheep.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "animal"
}
```

### skeleton

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/skeleton.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "any_of": [
        {
            "all_of": [
                {
                    "test": "has_biome_tag",
                    "operator": "==",
                    "value": "monster"
                },
                {
                    "test": "has_biome_tag",
                    "operator": "!=",
                    "value": "frozen"
                }
            ]
        },
        {
            "test": "has_biome_tag",
            "operator": "==",
            "value": "soulsand_valley"
        }
    ]
}
```

### slime

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/slime.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "any_of": [
        {
            "test": "has_biome_tag",
            "operator": "==",
            "value": "monster"
        },
        {
            "test": "has_biome_tag",
            "operator": "==",
            "value": "swamp"
        },
        {
            "test": "has_biome_tag",
            "operator": "==",
            "value": "frozen"
        }
    ]
}
```

### spider

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/spider.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "monster"
}
```

### squid

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/squid.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "ocean"
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "any_of": [
        {
            "test": "has_biome_tag",
            "operator": "==",
            "value": "river"
        }
    ]
}
```

### stray

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/stray.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": [
    {
        "test": "has_biome_tag",
        "operator": "==",
        "value": "frozen"
    },
    {
        "test": "has_biome_tag",
        "operator": "!=",
        "value": "ocean"
    }
]
```

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": [
    {
        "test": "has_biome_tag",
        "operator": "==",
        "value": "frozen"
    },
    {
        "test": "has_biome_tag",
        "operator": "==",
        "value": "ocean"
    }
]
```

### strider

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/strider.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "nether"
}
```

### tropicalfish

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/tropicalfish.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": [
    {
        "test": "has_biome_tag",
        "operator": "==",
        "value": "ocean"
    },
    {
        "test": "has_biome_tag",
        "operator": "==",
        "value": "warm"
    }
]
```

### turtle

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/turtle.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": [
    {
        "test": "has_biome_tag",
        "operator": "==",
        "value": "beach"
    },
    {
        "test": "has_biome_tag",
        "operator": "==",
        "value": "warm"
    }
]
```

### witch

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/witch.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "monster"
}
```

### wolf

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/wolf.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "taiga"
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "all_of": [
        {
            "test": "has_biome_tag",
            "operator": "==",
            "value": "forest"
        },
        {
            "test": "has_biome_tag",
            "operator": "!=",
            "value": "mutated"
        },
        {
            "test": "has_biome_tag",
            "operator": "!=",
            "value": "birch"
        },
        {
            "test": "has_biome_tag",
            "operator": "!=",
            "value": "roofed"
        },
        {
            "test": "has_biome_tag",
            "operator": "!=",
            "value": "mountain"
        }
    ]
}
```

### zombie

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/zombie.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "monster"
}
```

### zombie_pigman

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/zombie_pigman.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "spawn_zombified_piglin"
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:biome_filter": {
    "test": "has_biome_tag",
    "operator": "==",
    "value": "spawn_few_zombified_piglins"
}
```

# minecraft:brightness_filter

This component is used to set the allowed light level range for spawning in the entity. This component has the following parameters;

| Parameters         | Type    | Description                                                                                                     |
| ------------------ | ------- | --------------------------------------------------------------------------------------------------------------- |
| adjust_for_weather | Boolean | When true this gives the ability to spawn in during certain weather conditions where it wouldn't normally spawn |
| min                | Decimal | The minimum value is 0.0                                                                                        |
| max                | Decimal | The minimum value is 15.0                                                                                       |

Below is all the areas where this is used in the vanilla files.

### axolotl

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/axolotl.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 0,
    "max": 0,
    "adjust_for_weather": false
}
```

### bat

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/bat.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 0,
    "max": 4,
    "adjust_for_weather": true
}
```

### bee

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/bee.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 7,
    "max": 15,
    "adjust_for_weather": false
}
```

### chicken

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/chicken.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 7,
    "max": 15,
    "adjust_for_weather": false
}
```

### cow

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/cow.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 7,
    "max": 15,
    "adjust_for_weather": false
}
```

### creeper

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/creeper.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 0,
    "max": 7,
    "adjust_for_weather": true
}
```

### donkey

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/donkey.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 7,
    "max": 15,
    "adjust_for_weather": false
}
```

### drowned

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/drowned.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 0,
    "max": 7,
    "adjust_for_weather": true
}
```

### enderman

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/enderman.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 0,
    "max": 7,
    "adjust_for_weather": true
}
```

### fox

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/fox.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 7,
    "max": 15,
    "adjust_for_weather": false
}
```

### goat

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/goat.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 7,
    "max": 15,
    "adjust_for_weather": false
}
```

### horse

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/horse.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 7,
    "max": 15,
    "adjust_for_weather": false
}
```

### husk

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/husk.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 0,
    "max": 7,
    "adjust_for_weather": true
}
```

### llama

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/llama.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 7,
    "max": 15,
    "adjust_for_weather": false
}
```

### mooshroom

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/mooshroom.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 9,
    "max": 15,
    "adjust_for_weather": false
}
```

### ocelot

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/ocelot.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 7,
    "max": 15,
    "adjust_for_weather": false
}
```

### panda

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/panda.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 7,
    "max": 15,
    "adjust_for_weather": false
}
```

### parrot

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/parrot.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 7,
    "max": 15,
    "adjust_for_weather": false
}
```

### phantom

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/phantom.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 0,
    "max": 7,
    "adjust_for_weather": true
}
```

### pig

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/pig.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 7,
    "max": 15,
    "adjust_for_weather": false
}
```

### pillager_patrol

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/pillager_patrol.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 0,
    "max": 7,
    "adjust_for_weather": false
}
```

### polar_bear

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/polar_bear.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 7,
    "max": 15,
    "adjust_for_weather": false
}
```

### rabbit

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/rabbit.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 7,
    "max": 15,
    "adjust_for_weather": false
}
```

### sheep

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/sheep.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 7,
    "max": 15,
    "adjust_for_weather": false
}
```

### skeleton

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/skeleton.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 0,
    "max": 7,
    "adjust_for_weather": true
}
```

### spider

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/spider.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 0,
    "max": 7,
    "adjust_for_weather": true
}
```

### stray

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/stray.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 0,
    "max": 7,
    "adjust_for_weather": true
}
```

### turtle

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/turtle.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 7,
    "max": 15,
    "adjust_for_weather": false
}
```

### witch

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/witch.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 0,
    "max": 7,
    "adjust_for_weather": true
}
```

### wolf

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/wolf.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 7,
    "max": 15,
    "adjust_for_weather": false
}
```

### zombie

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/zombie.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:brightness_filter": {
    "min": 0,
    "max": 7,
    "adjust_for_weather": true
}
```

# minecraft:delay_filter

### pillager_patrol

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/pillager_patrol.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:delay_filter": {
    "min": 600,
    "max": 660,
    "identifier": "minecraft:pillager_patrol_easy",
    "spawn_chance": 20
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:delay_filter": {
    "min": 600,
    "max": 660,
    "identifier": "minecraft:pillager_patrol_normal",
    "spawn_chance": 20
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:delay_filter": {
    "min": 600,
    "max": 660,
    "identifier": "minecraft:pillager_patrol_hard",
    "spawn_chance": 20
}
```

# minecraft:density_limit

This component specifies the amount of entities to spawn in depending on if its a surface or uderground spawn. This limit is only calculated based on the simulation distance, entities who are not loaded would not be considered for this rule.

This component has the following parameters;

| Parameters  | Type    | Description                                                |
| ----------- | ------- | ---------------------------------------------------------- |
| surface     | Integer | As there is a global cap, technically the max would be 200 |
| underground | Integer | As there is a global cap, technically the max would be 200 |

Below is all the areas where this is used in the vanilla files.

### bat

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/bat.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:density_limit": {
    "surface": 5
}
```

### cod

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/cod.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:density_limit": {
    "surface": 20
}
```

### creeper

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/creeper.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:density_limit": {
    "surface": 5
}
```

### dolphin

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/dolphin.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:density_limit": {
    "surface": 5,
    "underground": 0
}
```

### drowned

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/drowned.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:density_limit": {
    "surface": 5
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:density_limit": {
    "surface": 2
}
```

### ghast

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/ghast.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:density_limit": {
    "surface": 0,
    "underground": 2
}
```

### phantom

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/phantom.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:density_limit": {
    "surface": 5
}
```

### pufferfish

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/pufferfish.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:density_limit": {
    "surface": 3
}
```

### salmon

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/salmon.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:density_limit": {
    "surface": 10
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:density_limit": {
    "surface": 4
}
```

### squid

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/squid.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:density_limit": {
    "surface": 4
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:density_limit": {
    "surface": 2
}
```

### strider

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/strider.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:density_limit": {
    "surface": 3
}
```

### tropicalfish

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/tropicalfish.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:density_limit": {
    "surface": 20
}
```

# minecraft:difficulty_filter

This component is used to set what difficulty level the entity can spawn in on, for example if your mob is hostile you would not want it to spawn in when on peaceful mode.

This component has the following parameters;

| Parameters | Type   | Description                                                                |
| ---------- | ------ | -------------------------------------------------------------------------- |
| min        | String | This is the minimum difficulty level in which the entity should spawn from |
| max        | String | This is the maximum difficulty level in which the entity should spawn to   |

The min and max values must be one of the following only:

-   peaceful
-   easy
-   normal
-   hard

Below is all the areas where this is used in the vanilla files.

### creeper

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/creeper.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:difficulty_filter": {
    "min": "easy",
    "max": "hard"
}
```

### drowned

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/drowned.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:difficulty_filter": {
    "min": "easy",
    "max": "hard"
}
```

### enderman

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/enderman.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:difficulty_filter": {
    "min": "easy",
    "max": "hard"
}
```

### ghast

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/ghast.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:difficulty_filter": {
    "min": "easy",
    "max": "hard"
}
```

### hoglin

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/hoglin.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:difficulty_filter": {
    "min": "peaceful",
    "max": "hard"
}
```

### husk

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/husk.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:difficulty_filter": {
    "min": "easy",
    "max": "hard"
}
```

### magma_cube

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/magma_cube.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:difficulty_filter": {
    "min": "easy",
    "max": "hard"
}
```

### phantom

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/phantom.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:difficulty_filter": {
    "min": "easy",
    "max": "hard"
}
```

### piglin

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/piglin.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:difficulty_filter": {
    "min": "peaceful",
    "max": "hard"
}
```

### pillager_patrol

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/pillager_patrol.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:difficulty_filter": {
    "max": "easy"
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:difficulty_filter": {
    "min": "normal",
    "max": "normal"
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:difficulty_filter": {
    "min": "hard"
}
```

### skeleton

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/skeleton.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:difficulty_filter": {
    "min": "easy",
    "max": "hard"
}
```

### slime

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/slime.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:difficulty_filter": {
    "min": "easy",
    "max": "hard"
}
```

### spider

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/spider.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:difficulty_filter": {
    "min": "easy",
    "max": "hard"
}
```

### stray

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/stray.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:difficulty_filter": {
    "min": "easy",
    "max": "hard"
}
```

### strider

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/strider.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:difficulty_filter": {
    "min": "peaceful",
    "max": "hard"
}
```

### witch

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/witch.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:difficulty_filter": {
    "min": "easy",
    "max": "hard"
}
```

### zombie

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/zombie.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:difficulty_filter": {
    "min": "easy",
    "max": "hard"
}
```

### zombie_pigman

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/zombie_pigman.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:difficulty_filter": {
    "min": "easy",
    "max": "hard"
}
```

# minecraft:disallow_spawns_in_bubble

### axolotl

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/axolotl.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:disallow_spawns_in_bubble": {}
```

# minecraft:distance_filter

### cod

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/cod.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:distance_filter": {
    "min": 12,
    "max": 32
}
```

### pillager_patrol

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/pillager_patrol.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:distance_filter": {
    "min": 24,
    "max": 48
}
```

### pufferfish

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/pufferfish.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:distance_filter": {
    "min": 12,
    "max": 32
}
```

### salmon

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/salmon.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:distance_filter": {
    "min": 12,
    "max": 32
}
```

### tropicalfish

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/tropicalfish.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:distance_filter": {
    "min": 12,
    "max": 32
}
```

# minecraft:height_filter

### axolotl

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/axolotl.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:height_filter": {
    "min": 0,
    "max": 63
}
```

### bat

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/bat.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:height_filter": {
    "min": -63,
    "max": 63
}
```

### glow_squid

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/glow_squid.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:height_filter": {
    "min": 0,
    "max": 63
}
```

### stray

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/stray.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:height_filter": {
    "min": 60,
    "max": 66
}
```

### turtle

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/turtle.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:height_filter": {
    "min": 60,
    "max": 67
}
```

# minecraft:herd

This component is used to determine how many spawn in at once. When this happens its called a herd.

This component has the following parameters;

| Parameters       | Type    | Description                                          |
| ---------------- | ------- | ---------------------------------------------------- |
| event            | String  | This is used to trigger the entities spawn events    |
| event_skip_count | Integer | Number of entities spawned before event is triggered |
| min_size         | Integer | Minimum number of entities that can spawn.           |
| max_size         | Integer | Maximum number of entities that can spawn.           |

Below is all the areas where this is used in the vanilla files.

### axolotl

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/axolotl.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 1,
    "max_size": 4,
    "event": "minecraft:entity_born",
    "event_skip_count": 2
}
```

### bat

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/bat.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 2,
    "max_size": 2
}
```

### bee

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/bee.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 1,
    "max_size": 1
}
```

### chicken

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/chicken.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 2,
    "max_size": 4
}
```

### cod

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/cod.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 4,
    "max_size": 7
}
```

### cow

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/cow.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 2,
    "max_size": 3
}
```

### dolphin

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/dolphin.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 3,
    "max_size": 5
}
```

### donkey

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/donkey.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 2,
    "max_size": 6
}
```

### drowned

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/drowned.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 2,
    "max_size": 4
}
```

### enderman

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/enderman.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 1,
    "max_size": 2
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 1,
    "max_size": 1
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 4,
    "max_size": 4
}
```

### fox

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/fox.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 2,
    "max_size": 4,
    "event": "minecraft:entity_born",
    "event_skip_count": 2
}
```

### glow_squid

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/glow_squid.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 2,
    "max_size": 4
}
```

### goat

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/goat.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 2,
    "max_size": 3
}
```

### hoglin

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/hoglin.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 4,
    "max_size": 4
}
```

### horse

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/horse.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": [
    {
        "min_size": 2,
        "max_size": 6,
        "event": "minecraft:make_white"
    },
    {
        "min_size": 2,
        "max_size": 6,
        "event": "minecraft:make_creamy"
    },
    {
        "min_size": 2,
        "max_size": 6,
        "event": "minecraft:make_chestnut"
    },
    {
        "min_size": 2,
        "max_size": 6,
        "event": "minecraft:make_brown"
    },
    {
        "min_size": 2,
        "max_size": 6,
        "event": "minecraft:make_black"
    },
    {
        "min_size": 2,
        "max_size": 6,
        "event": "minecraft:make_gray"
    },
    {
        "min_size": 2,
        "max_size": 6,
        "event": "minecraft:make_darkbrown"
    }
]
```

### husk

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/husk.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 2,
    "max_size": 4
}
```

### llama

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/llama.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 4,
    "max_size": 6
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 4,
    "max_size": 4
}
```

### magma_cube

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/magma_cube.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 1,
    "max_size": 4
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 2,
    "max_size": 5
}
```

### mooshroom

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/mooshroom.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 4,
    "max_size": 8
}
```

### ocelot

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/ocelot.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 1,
    "max_size": 2
}
```

### panda

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/panda.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 1,
    "max_size": 2
}
```

### parrot

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/parrot.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 1,
    "max_size": 2
}
```

### pig

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/pig.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 1,
    "max_size": 3
}
```

### piglin

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/piglin.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 2,
    "max_size": 4
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 4,
    "max_size": 4
}
```

### pillager_patrol

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/pillager_patrol.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 2,
    "max_size": 5,
    "initial_event": "minecraft:promote_to_patrol_captain",
    "initial_event_count": 1,
    "event": "minecraft:spawn_as_patrol_follower",
    "event_skip_count": 1
}
```

### polar_bear

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/polar_bear.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 1,
    "max_size": 2,
    "event": "minecraft:entity_born",
    "event_skip_count": 1
}
```

### pufferfish

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/pufferfish.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 3,
    "max_size": 5
}
```

### rabbit

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/rabbit.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 2,
    "max_size": 3
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 2,
    "max_size": 4
}
```

### salmon

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/salmon.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 3,
    "max_size": 5
}
```

### sheep

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/sheep.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 2,
    "max_size": 3
}
```

### skeleton

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/skeleton.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 1,
    "max_size": 2
}
```

### squid

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/squid.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 2,
    "max_size": 4
}
```

### stray

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/stray.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 1,
    "max_size": 2
}
```

### strider

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/strider.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 2,
    "max_size": 4
}
```

### tropicalfish

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/tropicalfish.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": [
    {
        "min_size": 3,
        "max_size": 5,
        "event": "minecraft:become_anenonme"
    },
    {
        "min_size": 3,
        "max_size": 5,
        "event": "minecraft:become_black_tang"
    },
    {
        "min_size": 3,
        "max_size": 5,
        "event": "minecraft:become_blue_dory"
    },
    {
        "min_size": 3,
        "max_size": 5,
        "event": "minecraft:become_butterfly_fish"
    },
    {
        "min_size": 3,
        "max_size": 5,
        "event": "minecraft:become_cichlid"
    },
    {
        "min_size": 3,
        "max_size": 5,
        "event": "minecraft:become_clownfish"
    },
    {
        "min_size": 3,
        "max_size": 5,
        "event": "minecraft:become_cc_betta"
    },
    {
        "min_size": 3,
        "max_size": 5,
        "event": "minecraft:become_dog_fish"
    },
    {
        "min_size": 3,
        "max_size": 5,
        "event": "minecraft:become_e_red_snapper"
    },
    {
        "min_size": 3,
        "max_size": 5,
        "event": "minecraft:become_goat_fish"
    },
    {
        "min_size": 3,
        "max_size": 5,
        "event": "minecraft:become_moorish_idol"
    },
    {
        "min_size": 3,
        "max_size": 5,
        "event": "minecraft:become_ornate_butterfly"
    },
    {
        "min_size": 3,
        "max_size": 5,
        "event": "minecraft:become_parrot_fish"
    },
    {
        "min_size": 3,
        "max_size": 5,
        "event": "minecraft:become_queen_angel_fish"
    },
    {
        "min_size": 3,
        "max_size": 5,
        "event": "minecraft:become_red_cichlid"
    },
    {
        "min_size": 3,
        "max_size": 5,
        "event": "minecraft:become_red_lipped_benny"
    },
    {
        "min_size": 3,
        "max_size": 5,
        "event": "minecraft:become_red_snapper"
    },
    {
        "min_size": 3,
        "max_size": 5,
        "event": "minecraft:become_threadfin"
    },
    {
        "min_size": 3,
        "max_size": 5,
        "event": "minecraft:become_tomato_clown"
    },
    {
        "min_size": 3,
        "max_size": 5,
        "event": "minecraft:become_triggerfish"
    },
    {
        "min_size": 3,
        "max_size": 5,
        "event": "minecraft:become_yellow_tang"
    },
    {
        "min_size": 3,
        "max_size": 5,
        "event": "minecraft:become_yellow_tail_parrot"
    }
]
```

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 1,
    "max_size": 3
}
```

### turtle

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/turtle.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 2,
    "max_size": 6
}
```

### wolf

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/wolf.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 4,
    "max_size": 4
}
```

### zombie

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/zombie.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 2,
    "max_size": 4
}
```

### zombie_pigman

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/zombie_pigman.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:herd": {
    "min_size": 2,
    "max_size": 4
}
```

# minecraft:mob_event_filter

### pillager_patrol

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/pillager_patrol.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:mob_event_filter": {
    "event": "minecraft:pillager_patrols_event"
}
```

# minecraft:permute_type

<CodeHeader></CodeHeader>

```json

"minecraft:permute_type": [
    {
        "weight": 100,
        "entity_type": "minecraft:pillager<minecraft:spawn_as_patrol_follower>"
    }
]
```

<CodeHeader></CodeHeader>

```json

"minecraft:permute_type": [
    {
        "weight": 80,
        "entity_type": "minecraft:pillager<minecraft:spawn_as_patrol_follower>"
    },
    {
        "weight": 20,
        "entity_type": "minecraft:vindicator"
    }
]
```

### zombie

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/zombie.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:permute_type": [
    {
        "weight": 95
    },
    {
        "weight": 5,
        "entity_type": "minecraft:zombie_villager_v2"
    }
]
```

# minecraft:player_in_village_filter

This component is used to track when a player enters a village. This is useful for entities that should only spawn in villages such as cats / villager's or pillager patrols.

This component has the following parameters;

| Parameters               | Type    | Description                                                                    |
| ------------------------ | ------- | ------------------------------------------------------------------------------ |
| distance                 | Integer | Used to define how far away from the player the entity will spawn              |
| village_border_tolerance | Integer | Used to define how close to the village boarder the entity is allowed to spawn |

For the village_border_tolerance, if 0 this will allow the entity to spawn right on the village boarder; increasing the number will push the entity further away from the boarder.

Below is all the areas where this is used in the vanilla files.

### pillager_patrol

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/pillager_patrol.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:player_in_village_filter": {
    "distance": 48,
    "village_border_tolerance": 32
}
```

# minecraft:spawn_event

### stray

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/stray.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawn_event": {
    "event": "change_to_skeleton"
}
```

# minecraft:spawns_above_block_filter

### axolotl

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/axolotl.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_above_block_filter": {
    "blocks": "minecraft:stone",
    "distance": 10
}
```

# minecraft:spawns_lava

This component is used to specify if the entity should spawn in lava or not. There are no parameters for this component, if its added as a rule then it sets itself to true and if there isn't one its automatically considered false.

### strider

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/strider.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_lava": {}
```

# minecraft:spawns_on_block_filter

### chicken

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/chicken.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_block_filter": "minecraft:grass"
```

### cow

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/cow.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_block_filter": "minecraft:grass"
```

### donkey

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/donkey.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_block_filter": "minecraft:grass"
```

### horse

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/horse.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_block_filter": "minecraft:grass"
```

### llama

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/llama.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_block_filter": "minecraft:grass"
```

### ocelot

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/ocelot.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_block_filter": "minecraft:grass"
```

### panda

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/panda.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_block_filter": "minecraft:grass"
```

### parrot

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/parrot.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_block_filter": "minecraft:grass"
```

### pig

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/pig.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_block_filter": "minecraft:grass"
```

### polar_bear

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/polar_bear.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_block_filter": "minecraft:ice"
```

### rabbit

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/rabbit.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_block_filter": [
    "minecraft:grass",
    "minecraft:snow",
    "minecraft:sand"
]
```

### sheep

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/sheep.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_block_filter": "minecraft:grass"
```

### turtle

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/turtle.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_block_filter": "minecraft:sand"
```

### wolf

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/wolf.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_block_filter": [
    "minecraft:grass",
    "minecraft:podzol",
    "minecraft:dirt"
]
```

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_block_filter": "minecraft:grass"
```

# minecraft:spawns_on_block_prevented_filter

### hoglin

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/hoglin.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_block_prevented_filter": [
    "minecraft:nether_wart_block",
    "minecraft:shroomlight"
]
```

### magma_cube

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/magma_cube.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_block_prevented_filter": [
    "minecraft:nether_wart_block",
    "minecraft:shroomlight"
]
```

### piglin

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/piglin.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_block_prevented_filter": [
    "minecraft:nether_wart_block",
    "minecraft:shroomlight"
]
```

### skeleton

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/skeleton.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_block_prevented_filter": [
    "minecraft:nether_wart_block",
    "minecraft:shroomlight"
]
```

### zombie_pigman

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/zombie_pigman.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_block_prevented_filter": [
    "minecraft:nether_wart_block",
    "minecraft:shroomlight"
]
```

# minecraft:spawns_on_surface

This component allows entities to spawn on the ground / outside. There are no parameters for this component, if its added as a rule then it sets itself to true and if there isn't one its automatically considered false.

Below is all the areas where this is used in the vanilla files.

### bee

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/bee.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### chicken

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/chicken.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### cod

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/cod.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### cow

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/cow.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### creeper

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/creeper.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### dolphin

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/dolphin.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### donkey

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/donkey.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### drowned

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/drowned.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### enderman

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/enderman.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### fox

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/fox.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### goat

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/goat.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### horse

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/horse.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### husk

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/husk.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### llama

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/llama.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### mooshroom

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/mooshroom.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### ocelot

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/ocelot.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### panda

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/panda.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### parrot

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/parrot.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### phantom

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/phantom.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### pig

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/pig.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### pillager_patrol

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/pillager_patrol.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### polar_bear

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/polar_bear.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### pufferfish

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/pufferfish.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### rabbit

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/rabbit.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### salmon

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/salmon.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### sheep

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/sheep.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### skeleton

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/skeleton.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### slime

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/slime.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### spider

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/spider.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### squid

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/squid.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### stray

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/stray.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### tropicalfish

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/tropicalfish.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### turtle

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/turtle.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### witch

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/witch.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### wolf

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/wolf.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

### zombie

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/zombie.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_on_surface": {}
```

# minecraft:spawns_underground

This component allows entities to spawn underground in caves / mineshafts etc.. There are no parameters for this component, if its added it sets itself to true and if there isn't one its automatically considered false.

Below is all the areas where this is used in the vanilla files.

### axolotl

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/axolotl.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underground": {}
```

### bat

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/bat.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underground": {}
```

### creeper

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/creeper.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underground": {}
```

### enderman

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/enderman.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underground": {}
```

### ghast

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/ghast.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underground": {}
```

### glow_squid

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/glow_squid.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underground": {}
```

### hoglin

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/hoglin.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underground": {}
```

### magma_cube

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/magma_cube.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underground": {}
```

### piglin

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/piglin.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underground": {}
```

### skeleton

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/skeleton.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underground": {}
```

### slime

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/slime.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underground": {}
```

### spider

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/spider.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underground": {}
```

### stray

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/stray.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underground": {}
```

### strider

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/strider.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underground": {}
```

### witch

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/witch.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underground": {}
```

### zombie

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/zombie.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underground": {}
```

### zombie_pigman

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/zombie_pigman.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underground": {}
```

# minecraft:spawns_underwater

This component allows entities to spawn in water. There are no parameters for this component, if its added it sets itself to true and if there isn't one its automatically considered false.

Below is all the areas where this is used in the vanilla files.

### axolotl

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/axolotl.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underwater": {}
```

### cod

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/cod.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underwater": {}
```

### dolphin

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/dolphin.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underwater": {}
```

### drowned

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/drowned.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underwater": {}
```

### glow_squid

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/glow_squid.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underwater": {}
```

### guardian

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/guardian.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underwater": {}
```

### pufferfish

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/pufferfish.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underwater": {}
```

### salmon

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/salmon.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underwater": {}
```

### squid

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/squid.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underwater": {}
```

### tropicalfish

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/tropicalfish.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:spawns_underwater": {}
```

# minecraft:weight

This component is used to set the spawning priority for the entity.

This component has the following parameters;

| Parameters | Type    | Description                                                                                                    |
| ---------- | ------- | -------------------------------------------------------------------------------------------------------------- |
| default    | Integer | Entities with a lower weight value will have a lower chance to spawn than entities with a higher weight value. |

Below is all the areas where this is used in the vanilla files.

### axolotl

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/axolotl.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 8
}
```

### bat

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/bat.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 10
}
```

### bee

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/bee.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 10
}
```

### chicken

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/chicken.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 10
}
```

### cod

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/cod.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 75
}
```

### cow

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/cow.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 8
}
```

### creeper

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/creeper.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 100
}
```

### dolphin

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/dolphin.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 7
}
```

### donkey

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/donkey.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 1
}
```

### drowned

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/drowned.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 100
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 5
}
```

### enderman

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/enderman.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 10
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 6
}
```

### fox

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/fox.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 8
}
```

### ghast

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/ghast.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 40
}
```

### glow_squid

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/glow_squid.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 10
}
```

### goat

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/goat.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 20
}
```

### hoglin

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/hoglin.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 20
}
```

### horse

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/horse.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 4
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 1
}
```

### husk

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/husk.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 240
}
```

### llama

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/llama.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 5
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 8
}
```

### magma_cube

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/magma_cube.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 10
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 100
}
```

### mooshroom

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/mooshroom.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 8
}
```

### ocelot

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/ocelot.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 30
}
```

### panda

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/panda.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 10
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 40
}
```

### parrot

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/parrot.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 40
}
```

### phantom

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/phantom.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 100
}
```

### pig

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/pig.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 10
}
```

### piglin

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/piglin.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 5
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 15
}
```

### polar_bear

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/polar_bear.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 1
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 5
}
```

### pufferfish

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/pufferfish.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 25
}
```

### rabbit

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/rabbit.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 4
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 20
}
```

### salmon

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/salmon.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 26
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 16
}
```

### sheep

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/sheep.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 12
}
```

### skeleton

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/skeleton.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 80
}
```

### slime

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/slime.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 100
}
```

### spider

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/spider.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 100
}
```

### squid

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/squid.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 8
}
```

### stray

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/stray.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 120
}
```

### strider

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/strider.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 20
}
```

### tropicalfish

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/tropicalfish.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 75
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 25
}
```

### turtle

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/turtle.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 8
}
```

### witch

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/witch.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 5
}
```

### wolf

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/wolf.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 8
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 5
}
```

### zombie

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/zombie.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 100
}
```

### zombie_pigman

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/zombie_pigman.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 100
}
```

<CodeHeader></CodeHeader>

```json

"minecraft:weight": {
    "default": 1
}
```

# minecraft:world_age_filter

### pillager_patrol

<small>[View file](https://github.com/bedrock-dot-dev/packs/tree/master/stable/behavior/spawn_rules/pillager_patrol.json)</small>

<CodeHeader></CodeHeader>

```json

"minecraft:world_age_filter": {
    "min": 6000
}
```
