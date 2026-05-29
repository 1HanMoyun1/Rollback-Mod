# Rollback-Mod

A Minecraft Forge mod providing a powerful rollback system and diverse core item abilities.

## Introduction

Rollback-Mod is a server-assist mod designed for Minecraft Forge, focused on delivering flexible rollback mechanics and a variety of core item systems. Players can use multiple types of "core" items to gain advanced abilities, including time control, target marking, self-sacrifice protection, and more.

## Core Items

This mod provides 8 core items, each producing distinct effects when used with an Inhaler:

| Core Type | Function Description |
|----------|----------------------|
| **Chronos Core** | Time rewind core that slows down time flow |
| **Disconnection Core** | Disconnection core |
| **Molting Core** | Molting core |
| **Tower Core** | Tower core |
| **Sand Core** | Sand core |
| **Causality Core** | Causality core enabling death rollback |
| **Myriad Core** | Myriad core preventing death |
| **Stasis Core** | Stasis core freezing target state |

## Main Features

### Checkpoint and Rollback System
- Create game checkpoints to record the current world state
- Upon player death, choose to rollback to a checkpoint
- Support rollback for all players or only the deceased player
- Configurable: automatically create an initial checkpoint on first world load

### Marking System
- Players can use cores to mark entities (players or mobs)
- When a marked target takes damage, corresponding effects are triggered
- Configurable options: one mark per player, clear mark when target dies, etc.

### Time Control
- Compatible with the Time Clock mod
- Activate/deactivate time-slowing effect via keybind
- Customizable time-slowing multiplier

### HUD Display
- Display current game day
- Support countdown mode
- Animated transition effects for day changes

## Configuration Options

This mod offers extensive customization via the `rollbackmod.toml` configuration file:

```toml
# Rollback Settings
enableDeathRollback = true          # Enable death rollback
destroyAllCoresOnRollback = false   # Destroy all cores upon rollback
saveOnFirstWorldLoad = true         # Save on first world load
rollbackAllPlayersOnDeath = false   # Rollback all players on death
syncInventoryAndHealth = true       # Sync inventory and health

# Chronos Settings
chronosDurationTicks = 12000        # Chronos duration in ticks
chronosKeyMode = "toggle"           # Key mode (toggle/hold)
chronosSlowTimeFactor = 0.5         # Time slow factor
requireTimeClockMod = false         # Require Time Clock mod

# Stasis Settings
stasisDurationTicks = 24000         # Stasis duration in ticks

# Marking Settings
onlyOneMarkPerPlayer = true         # Only one mark per player
markLostWhenTargetDead = true       # Clear mark when target dies
myriadRequiresWeaponToPreventDeath = true # Myriad core requires weapon to prevent death

# HUD Settings
showDayHUD = true                   # Show day HUD
showDayTransition = true            # Show day transition animation
countdownMode = false               # Enable countdown mode
countdownDays = 30                  # Countdown days
```

## Installation

1. Download the mod's JAR file
2. Place the JAR file into the `mods` folder of your Minecraft server or client
3. For servers, it is recommended to also install `fabric-api` (if using Fabric) or the corresponding Forge version
4. Launch the game; the configuration file will be automatically generated on first run

## Usage

### Basic Operations
1. **Obtain Core Items**: Find the desired core item in the Creative inventory tab
2. **Use Core**: Hold the Inhaler and right-click a player or mob to apply the core effect
3. **Create Checkpoint**: Create via in-game interaction or mod command
4. **Trigger Rollback**: Automatically rolls back to the checkpoint upon player death (if enabled)

### Key Bindings
- **Chronos Slow Time Key**: Default binding; customizable

## Compatibility

- Requires Minecraft Forge 1.20.1 or higher
- Optional: Install the Time Clock mod to enable advanced time control features

## License

This mod is open-sourced under the MIT License.

## Contributors

Thanks to all developers who contributed code and ideas to this mod.