# ZAWABaseWater
```diff
With each new ZAWA update the accuracy of this tutorial will change.
```
**Please read the [ZAWABaseLand Tutorial](https://github.com/0SoggyMustache0/ZAWA/blob/master/AddonCreation/LandAnimal.md) before continuing.**

The org.zawamod.entity.base.ZAWABaseWater extends upon ZAWABaseLand. Your entity should extend this class if you are making a water creature for zawa.

```java
public class EntityCoolFish extends ZAWABaseWater {

}
```

ZAWABaseWater is abstract, however it does not provide any abstract methods. If for whatever reason you're not using an IDE that will auto create the methods, copy the methods below.

```java
public class EntityCoolFish extends ZAWABaseWater {
	public EntityCoolFish(World worldIn) {
		super(worldIn);
	}

	@Override
	public ItemStack setVial() {
		return null;
	}

	@Override
	public ItemStack setTameItem() {
		return null;
	}

	@Override
	public int setVariants() {
		return 0;
	}

	@Override
	public AnimalData.EnumNature setNature() {
		return null;
	}
}
```

Below is an example of what these methods would look like filled in.

```java
public class EntityCoolFish extends ZAWABaseWater {
	public EntityCoolFish(World worldIn) {
		super(worldIn);
	}

	@Override
	public ItemStack setVial() {
		return new ItemStack(ZAWAItems.APE_KIBBLE);
	}

	@Override
	public ItemStack setTameItem() {
		return new ItemStack(ZAWAItems.APE_VIAL);
	}

	@Override
	public int setVariants() {
		return 3; // This means there are 3 variants : 0, 1, and 2
	}

	@Override
	public AnimalData.EnumNature setNature() {
		return AnimalData.EnumNature.PROTECTIVE; // This nature will make the entity attack when the player is too close
	}
}
```

Unlike ZAWABaseLand this class does not require the createChild method and by default it is expected that water animals cannot create children.
