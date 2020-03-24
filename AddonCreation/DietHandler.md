# ZAWA Diet Handler

The diet handler as lots of options for you to use for your add-on. 
org.zawamod.entity.core.DietHandler

The DietHandler class has all the diets ZAWA animals and add-on animals use. 
* HERBIVORE
* KELP
* WOOD_EATER
* FRUGIVORE
* INSECTIVORE
* SMALL_CARNIVORE
* LEAF_EATER
* PARROT
* NECTIVORE
* EUCALYPTUS
* OMNIVORE
* GRAZER
* PISCIVORE
* LARGE_CARNIVORE
* SHELLFISH
* SCAVENGER
* OPPORTUNIST
* TURTLE
Unpopulated, yet present lists for add-on use.
* CARNIVORE_FISH
* VEGGIE_FISH
* OMNIVOROUS_FISH

## Binding your diet type to an animal

After deciding which of these options best fits your animal-use the DIET_MAP to define the class and food list.
```java
DietHandler.DIET_MAP.put(EntityAfricanLion.class, DietHandler.LARGE_CARNIVORE);
```
The code above should only be called once. Can be called at any time to "register" the diet, however it is suggested to do these diet handling in the post init.

## Adding your food type to an existing diet

```java
DietHandler.TURTLE.add(Items.SEEDS);
```
The code above will add the minecraft seeds to the turtle diet type. This code can be run at any time and will affect all animals that use the diet type.

