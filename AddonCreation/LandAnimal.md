# ZAWABaseLand
```diff
With each new ZAWA update the accuracy of this tutorial will change.
This tutorial currently references methods and variables in unreleased versions.
```

The org.zawamod.entity.base.ZAWABaseLand will handle everything you see regular zawa animals do. The class also provides its own implementations of many methods you would see in minecraft to help scalability. Your entity should extend this class.

```java
public class EntityOrangutan extends ZAWABaseLand{

}
```

ZAWABaseLand is abstract. If for whatever reason you're not using an IDE that will auto create the methods, copy the methods below.

```java
public class EntityOranguatan extends ZAWABaseLand {
	public EntityOranguatan(World worldIn) {
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

	@Nullable
	@Override
	public EntityAgeable createChild(EntityAgeable ageable) {
		return null;
	}
}
```

Below is an example of what these methods would look like filled in.

```java
public class EntityOranguatan extends ZAWABaseLand {
	public EntityOranguatan(World worldIn) {
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

	@Nullable
	@Override
	public EntityAgeable createChild(EntityAgeable ageable) {
		return new EntityOranguatan(world);
	}
}
```

Once you have created the class it is very important to go to the [Setting entity critical data](https://github.com/0SoggyMustache0/ZAWA/blob/master/AddonCreation/1GettingStarted.md#setting-entity-critical-data) section to make sure that your animal has things like a diet. There is nothing more you need to add to the entity class to get a functional ZAWA entity.

## Useful Methods
```java
//Returns the Gender enum of the animal
Gender getGender();

//Returns true if the stack is a food. Handled by the diethandler and should not be overwritten unless you require a special case.
boolean isFoodType(ItemStack);

//Returns a DataItem of StringedItems for the animal data book gui.
DataItem getIconList();

//Returns if the animal's eyes are closed. True if the animal is asleep
boolean getBlinking();

//Returns if the animal should randomly wander to items : default false
boolean displayCuriosity();

//Returns if the animal can be transported in the animal transport vehicle
boolean isTransportable();

//Returns if zawa should consider the animals gender when breeding is attempted
boolean countGenderForBreeding();

//Returns if the animal should be nocturnal : default false
boolean flipSleep();

//Returns if the animal can generate sleep animations and actually sleep
boolean canSleep();

```
