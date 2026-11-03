# Mirthwood Fishing Tweaks

**A configurable fishing quality-of-life and cheat mod for Mirthwood, developed by Sarakiel.**

Make fishing faster, remove fishing spot cooldowns, improve Fish Creels, and customize fish quantities, Survival XP rewards, and rare fish chances.

All major features can be enabled, disabled, or customized independently using the BepInEx configuration file.

**Version:** 1.2.0  
**Author:** Sarakiel  
**Mod Loader:** BepInEx 5.x  
**Platform:** Windows

[Download Latest Release](https://github.com/sarakiel-id/MirthwoodFishingTweaks-Sarakiel/releases/latest) | [Nexus Mods](https://www.nexusmods.com/mirthwood/mods/15) | [Report an Issue](https://github.com/sarakiel-id/MirthwoodFishingTweaks-Sarakiel/issues)

---

## Features

### 🎣 Rod Fishing

- **Instant Bite** — Removes almost all waiting time before a fish bites.
- **Instant Catch** — Automatically hooks and catches fish without requiring manual input during the fishing minigame.
- **Fishing Yield Multiplier** — Increase the number of fish received from successful catches.
- **Fishing XP Multiplier** — Increase Survival XP rewards earned from fishing.
- **Rare Fish Multiplier** — Increase the probability of catching higher-rarity fish.

Rare fish calculations preserve location-specific fishing pools. Lake, river, and sea fishing continue to use their respective fish selections.

### 🪤 Fish Creels

- **Instant Fish Creel** — Fish Creels become ready immediately.
- **Unbreakable Fish Creel** — Prevents Fish Creels from breaking during normal use.
- **Creel Yield Multiplier** — Increase the amount of fish collected.
- **Creel XP Multiplier** — Increase Survival XP earned from collecting fish.
- **Creel Rarity Multiplier** — Increase the probability of receiving rare fish from Fish Creels.

Fish Creel settings are independent of rod fishing settings.

### 🌊 Fishing Spots

- **Infinite Fishing Spots** — Prevents fishing spots from entering their normal depletion or respawn cooldown.
- **Restore Fishing Spot Ripples** — Keeps the game's original fishing spot visual effects visible.

No additional hotkeys or in-game menus are required.

---

## Default Gameplay Settings

| Feature | Default |
|---|---|
| Instant Bite | Enabled |
| Instant Catch | Enabled |
| Fishing Yield | 5× |
| Fishing XP | 10× |
| Fishing Rarity | 5× |
| Instant Fish Creel | Enabled |
| Unbreakable Fish Creel | Enabled |
| Fish Creel Yield | 5× |
| Fish Creel XP | 10× |
| Fish Creel Rarity | 5× |
| Infinite Fishing Spots | Enabled |
| Fishing Spot Ripples | Enabled |

Every feature can be customized individually.

## Requirements

- Mirthwood for Windows
- BepInEx 5.x (recommended: 5.4.23.2)

**Recommended BepInEx installer:**  
[Mirthwood BepInEx Pre-Configured](https://www.nexusmods.com/mirthwood/mods/1)

The mod uses BepInEx and Harmony to modify Mirthwood's fishing behavior at runtime.

## Installation

1. Install BepInEx into your Mirthwood game directory.
2. Download the latest release ZIP from [GitHub Releases](https://github.com/sarakiel-id/MirthwoodFishingTweaks-Sarakiel/releases).
3. Extract the ZIP into your main Mirthwood directory, preserving the folder structure.
4. Verify that the DLL is installed at:

   `Mirthwood\BepInEx\plugins\MirthwoodFishingTweaks\MirthwoodFishingTweaks.dll`

5. Start Mirthwood and load your saved game.
6. Enjoy fishing!

The configuration file is automatically generated when the mod launches for the first time.

**Updating:** Replacing the mod DLL does not reset your existing configuration when using the standard release package.

## Configuration

All features are configurable through:

`BepInEx\config\sarakiel.mirthwood.fishingtweaks.cfg`

Close the game before editing the configuration file.

### Fishing Settings

| Setting | Default | Description |
|---|---|---|
| `Enabled` | `true` | Enable fishing tweaks |
| `InstantBite` | `true` | Minimize bite waiting time |
| `InstantCatch` | `true` | Automatically complete catches |
| `InstantBiteWaitSeconds` | `0.01` | Pre-bite waiting duration |
| `UICloseSafetyMarginSeconds` | `0.08` | UI timing safety margin |
| `FishingYieldMultiplier` | `5` | Rod fishing reward quantity |
| `FishingXpMultiplier` | `10` | Survival XP multiplier |
| `FishRarityMultiplier` | `5` | Rare fish probability multiplier |

### Fish Creel Settings

| Setting | Default | Description |
|---|---|---|
| `InstantCreelCatch` | `true` | Instant Fish Creel production |
| `UnbreakableFishCreel` | `true` | Prevent Fish Creels from breaking |
| `CreelYieldMultiplier` | `5` | Fish Creel reward quantity |
| `CreelXpMultiplier` | `10` | Fish Creel Survival XP multiplier |
| `CreelRarityMultiplier` | `5` | Fish Creel rare fish multiplier |

### Fishing Spot Settings

| Setting | Default | Description |
|---|---|---|
| `InfiniteFishingSpots` | `true` | Disable fishing spot depletion |
| `RestoreFishingSpotRipples` | `true` | Preserve ripple visual effects |

### Diagnostics

| Setting | Default | Description |
|---|---|---|
| `VerboseLogging` | `false` | Enable detailed diagnostic logging |

Enable verbose logging only when troubleshooting.

### Multiplier Behavior

Setting an individual multiplier to `1` preserves the corresponding vanilla quantity, XP, or rarity behavior.

For example:

```ini
FishingYieldMultiplier = 1
FishingXpMultiplier = 1
FishRarityMultiplier = 1
```

This allows you to enjoy Instant Bite and Instant Catch while keeping normal fishing rewards.

**Important notes:**

- Rare fish multipliers preserve location-specific fishing pools.
- Non-fish rewards can also be affected by yield multipliers.
- Non-fish Fish Creel rewards do not receive additional Fish Creel XP.
- Very high rarity multipliers can make the rarest available fish dominate catches.
- Very high XP multipliers can significantly accelerate Survival progression.

Moderate multiplier values are recommended for normal gameplay.

---

## Compatibility

Fishing Tweaks v1.2.0 was developed against Mirthwood's existing fishing, inventory, Fish Creel, and experience systems.

Compatibility with all future Mirthwood versions is not guaranteed.

If the mod stops working after a game update:

1. Verify BepInEx loads correctly.
2. Check whether the DLL is installed in the correct folder.
3. Enable `VerboseLogging = true` if needed.
4. Report the problem through [GitHub Issues](https://github.com/sarakiel-id/MirthwoodFishingTweaks-Sarakiel/issues).

Include your game version and relevant information from:

`BepInEx\LogOutput.log`

Remove any sensitive information before sharing logs.

## Uninstallation

Delete:

`BepInEx\plugins\MirthwoodFishingTweaks\`

Optionally delete the configuration:

`BepInEx\config\sarakiel.mirthwood.fishingtweaks.cfg`

Uninstalling restores normal fishing behavior, but items and XP already earned remain in your save.

## Changelog

### v1.2.0

- Added rod fishing yield multiplier.
- Added Fish Creel yield multiplier.
- Added independent fishing and Fish Creel XP multipliers.
- Added rare fish multipliers for both fishing methods.
- Preserved location-specific fishing pools.
- Improved handling of very large rarity multiplier values.
- Added optional detailed diagnostic logging.
- Preserved instant fishing and infinite fishing spot functionality.

### v1.1.0

- Instant Bite and Instant Catch.
- Instant Fish Creel.
- Unbreakable Fish Creel.
- Infinite Fishing Spots.
- Fishing spot ripple restoration.

## Credits

**Developed by Sarakiel**

Built using BepInEx and Harmony.

Special thanks to the creator of the pre-configured Mirthwood BepInEx installer.

This is an unofficial community mod and is not affiliated with or endorsed by the developers or publishers of Mirthwood.

The source code is maintained separately from this public release repository.