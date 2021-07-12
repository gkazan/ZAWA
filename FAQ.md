# Frequently Asked Questions

### Q: Will ZAWA: Rebuilt update past Minecraft 1.12.2?

A: The short answer is no. However, there is an entire recode in the works by our team! ZAWA: Evolved will be released for Forge 1.16.5, once for Forge 1.12.2, and Fabric versions are TBD. All of Rebuilt's animals will be brought back, as well as many new animals! Be sure to join our discord or follow our Twitter for more information on Evolved.

## How To Install ZAWA

- ZAWA: https://minecraft.curseforge.com/projects/zoo-wild-animals-rebuild
- Bookworm: https://minecraft.curseforge.com/projects/bookworm

[![Install](http://img.youtube.com/vi/qFdtD9AxQUM/0.jpg)](http://www.youtube.com/watch?v=qFdtD9AxQUM)

## General ZAWA Questions

#### Q: Can I use your mod in a modpack?

A: Only if the modpack is available solely on CurseForge/Twitch. There are NO exceptions.

#### Q: Will you make the mod for Minecraft 1.7.10 or any distribution of Minecraft other than Java?

A: No.

#### Q: My game crashed or I have found a bug!

A: Click the Issues tab at the top to report a bug.

#### Q: Can you add this animal?

A: We do NOT take any animal suggestions.

#### Q: What program do you use/should I use to make models?

A: [iChun's Tabula](https://minecraft.curseforge.com/projects/tabula-minecraft-modeler). If you are interested, this is the style guide we follow for our animals: https://docs.google.com/document/d/1GpKKnRLGA9qRiPsO8g650BJYC444HoEHMlMSK16lYcU/edit?usp=sharing

#### Q: How do I get my animal out of the ATV?

A: Shift + Right Click the vehicle

#### Q: How do I fix spawning issues?

A: Make sure you're on the latest version of zawa! If you still have issues use the config file located in .minecraft/config to fix it.

#### Q: Why are your discord admins mean?

A: You don't pay them.

#### Q: How do I find the crafting recipes?

A: Download and use JEI for help with recipes: https://www.curseforge.com/minecraft/mc-mods/jei, or check out our Wiki tab at the top of this page.

## ZAWA Configs

Locate your minecraft directory, find the config folder, and ZAWA's files will be there in their own folder: **ZooAndWildAnimalsRebuilt1.12.2-VERSION**. Every new version of ZAWA generates a new folder, you can delete version folders you are not using!

You MUST restart your game for any config changes to occur properly.

WorldGeneration.cfg
  - Use this file to disable world generation of any plants added by ZAWA.

ZAWA1.12.2-VERSION.cfg
  - This file contains general config options for ZAWA.
  - Enrichment deprecation and drinking cooldown can be configured here.

ZAWAModules.cfg
  - Main config for configuring hunger, thirst, and enrichment. ***Disable these in this config if you are having issues with your tamed animals dying!***

ZAWASpawnConfigurations.cfg
  - This file is where you can enable/disable individual ZAWA entities, control exactly which biomes they spawn in, exactly how many spawn together, and how often they spawn.
  - Spawn Chance is a weighted random number. The higher the number, the more likely that entity will spawn. You can also set this to -1 to disable spawns, in case the Enabled setting fails.
  
## Incompatible Mods
  
- Custom Mob Spawner -- *InControl mod can be used to adjust mob spawns in place of CMS*
- Better Agriculture
