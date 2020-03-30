# ZAWABaseLand
```diff
With each new ZAWA update the accuracy of this tutorial will change.
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
