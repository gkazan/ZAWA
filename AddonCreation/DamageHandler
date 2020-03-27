# ZAWA Damage Handler

The damage handler as lots of options for you to use for your add-on. 
org.zawamod.entity.core.DamageHandler

Why use the ZAWA DamageHandler?

The ZAWA DamageHandler will handle, config options, what animals to attack and when, damage values, difficulties and more.

Nothing in this class is required for creating an animal, however if you want your animal to attack it should be done here.


## Setting attack damage for your animal

```java
DamageHandler.DAMAGE_MAP.put(EntityAfricanLion.class, 7f);
```
The code above should only be called once. Can be called at any time to "register" the damage, however it is suggested to do these damage handling in the post init.

## Telling your animal what other entities it should attack

```java
DamageHandler.TARGET_MAP.put(EntityPolarBear.class, Stream.of(EntityVillager.class, EntityChicken.class).collect(Collectors.toList()));
```
The code above will put into the target map a list of entity classes that the key entity should attack. There is NO need to add the EntityPlayer, EntityPlayer attacking is handled by the animal's nature. This code can be called at any time to "register" the attacks, however it is suggested to do this in the post init.

## Setting distance tolerance

```java
DamageHandler.DISTANCE_TOLERANCE.put(EntityPolarBear.class, 10f);
```
The code above will tell the animal how far to look for a player or other animal that is near it before attacking with the protective nature. Default is set to 3. The value will add 1 for normal, and 2 for hard.
