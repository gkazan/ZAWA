# ZAWA Animal Pack
```diff
With each new ZAWA update the accuracy of this tutorial will change.
This tutorial currently references methods and variables in unreleased versions.
```

## This tutorial currently references methods and code that are unreleased. This page should be used purely for preparation of the 2.1 update as things will change!

As of ZAWA 2.1 the AnimalPack class has been introduced. The AnimalPack is a way to load in JSON files to provide important information for each animal.
Why? Not only does this method allow add-on developers to easily change zawa/add-on animal information, but it also will allow the standard player to change information about animals using resource packs.

The JSON files go in assets/modid/data/animal/ANIMAL.json

Registration of the AnimalPack must be done through ZAWAMain$registerPack with the paramaters for the class of the animal and a location to the pack. This method will return the AnimalPack object for the animal and put the object into the PACKS map of ZAWAMain.

Properties. This list may expand/shorten with each update.

### Booleans
```
"swimming" //Although this will allow the animal to walk into water more frequenty it does NOT add swimming AI
"water_breathing"
"transportable" //If the animal can be placed in the ATV
"controllable" //If the animal can be controlled while ridden (like a horse)
"bird_shoulder" //If the bird can be held on the players shoulder
"flip_sleep" //If the sleep time of the animal should be reversed
```

### Floats
```
"damage" //Animals attack damage
"speed" //ZAWA handled speed (1.0 is default)
"distance_tolerance" //How close a player has to be (depending on nature) before the animal will attack
"flee_speed" //How fast the animal can run from predators
"step_height"
"max_health"
"inheritance_chance" //Chance of a baby getting the parent's variant (0.6 default)
"breed_variant_chance" //Chance for breed only variants to spawn (0.02 default)
"rare_variant_chance" //Chance for rare variants to spawn (0.02 default)
"male_gender_percent" //Chance for male animals to spawn (0.5 default)
"jump_upwards_motion"
```

### Doubles
```
"mc_speed" //MC handled speed (0.23 is default)
```

### ItemStack / Drops
In reference to an item you should use the unlocalized name: "zawa:kibble"
```
"vial"
"kibble"

"drops" //Drops is an array of objects. See the example below for what you can do
//"min" and "max" default to 1 and "chance" defaults to -1 (which causes a 100% drop chance)

```

### Other
```
"activity" //How often the animal moves: from quickest to slowest [ACTIVE, HASTY, NORMAL, CALM, LAZY, INACTIVE, NON_MOVING]
"nature" //Nature defines attacking/fleeing [NEUTRAL, PROTECTIVE, AGGRESSIVE, SKITTISH, PROVOKED]
//Protective attacks if you get close or hit the animal while provoked is only if the animal is attacked

"targets" //Targets is an array of resource locations, please review the example
"breed_variants" //An array of integers for variants only avaible by breeding
"rare_variants" //An array of integers for variants only availble with a rare spawn chance
```


Below is an example of a filled out JSON file for the indian gharial with modifications for this tutorial.

```json
{
  "max_health": 36.0,
  "variants": 6,
  "kibble": "zawa:crocodile_kibble",
  "vial": "zawa:crocodile_vial",
  "nature": "PROTECTIVE",
  "activity": "LAZY",
  "water_breathing": true,
  "mc_speed": 0.13,
  "speed": 1.35,
  "drops": [
    {
      "item": "zawa:reptile_meat_raw",
      "cooked_item": "zawa:reptile_meat_cooked"
    },
    {
      "item": "minecraft:leather",
      "max": 2
    }
  ],
  "targets": [
    "minecraft:sheep"
  ]
}
```
