# Ultimate Roguelike Framework

A comprehensive Unreal Engine C++ plugin for creating Vampire Survivors-style roguelike games with Blueprint-First, Actor-Agnostic, Plug & Play architecture.

## 🎮 Overview

Ultimate Roguelike Framework provides a complete, production-ready system for building top-down roguelike games inspired by Vampire Survivors. The framework is built in C++ for performance but fully exposed to Blueprints for ease of use.

## ✨ Key Features

### Core Systems
- **6-Slot Weapon System** - Vampire Survivors-style weapon inventory with auto-fire
- **8 Weapon Types** - Projectile, Melee, Area, Orbit, Beam, Bounce, Passive, Summon
- **Weapon Evolution** - Evolve weapons when conditions are met
- **Experience & Leveling** - XP gain, level progression, and skill points
- **Health System** - Damage, healing, regeneration, and death handling
- **Player Stats** - Comprehensive stat system with PowerUp modifiers

### Progression Systems
- **Level-Up Cards** - Vampire Survivors-style card selection on level up
- **Fallback Cards** - Alternative cards when weapon pool is empty
- **PowerUp Shop** - Meta progression with persistent upgrades
- **Currency System** - Run-based and persistent currency tracking
- **Character Selection** - Multiple character support with unique stats

### Combat Systems
- **Auto-Fire** - Automatic weapon firing with individual cooldowns
- **Targeting System** - Flexible enemy targeting with class/tag filtering
- **Object Pooling** - Optimized projectile and pickup pooling
- **Vacuum System** - Automatic pickup collection
- **Separation Component** - Prevent enemy stacking

### Game Director
- **Wave System** - Wave-based enemy spawning with difficulty scaling
- **Time Limit** - Optional time limit or endless mode
- **Special Events** - Timed events with custom enemy spawns
- **Loot System** - Configurable loot drops from enemies

### Developer Features
- **Blueprint-Friendly** - All systems fully exposed to Blueprints
- **Easy UI Libraries** - Simplified functions for UI integration
- **Debug Tools** - Visual debugging and console commands
- **Performance Optimized** - Handles hundreds of enemies efficiently
- **Comprehensive Documentation** - 20+ detailed guides included

## 🔧 Technical Details

### Engine Compatibility
- Unreal Engine 5.0+
- Tested on UE 5.0 - 5.7

### Supported Platforms
- Windows (Win64)

### Architecture
- **C++ Core** - High-performance C++ implementation
- **Blueprint-First** - Designed for Blueprint users
- **Actor-Agnostic** - Works with any actor type
- **Component-Based** - Modular component architecture
- **Data-Driven** - Configuration through Data Assets

## 📦 Installation

### Method 1: Plugin Installation (Recommended)
1. Copy the `UltimateRoguelikeFramework` folder to your project's `Plugins/` directory
2. Restart Unreal Engine
3. Enable the plugin in Edit → Plugins → Search "Ultimate Roguelike Framework"
4. Restart the editor
5. Plugin is ready to use!

### Method 2: Example Project
1. Open the included Example Project
2. Explore the demo map and example implementations
3. Copy components and configurations to your project

## 🚀 Quick Start

### Basic Setup (5 Minutes)

1. **Add Components to Player**
```
Player Blueprint:
├── URFHealthComponent (Health system)
├── URFExperienceComponent (Leveling system)
├── URFWeaponComponent (Weapon management)
├── URFPlayerStatsComponent (Stat system)
├── URFLevelUpSystem (Card selection)
└── URFVacuumComponent (Pickup collection)
```

2. **Create Weapon Data Asset**
```
Right-click in Content Browser
→ Data Asset
→ URFWeaponDataAsset
→ Configure weapon properties
```

3. **Add Starting Weapon**
```
Player Blueprint
→ URFWeaponComponent
→ Starting Weapons
→ Add your weapon data asset
```

4. **Add Enemies**
```
Enemy Blueprint:
└── URFHealthComponent (Health system)

Configure enemy spawning in Game Director
```

5. **Test**
```
Press Play
→ Weapon auto-fires
→ Kill enemies to gain XP
→ Level up to get card selection
```

### Example Project Setup
The included Example Project contains:
- Fully configured player character
- Multiple weapon examples
- Enemy spawning system
- UI implementation
- Demo map with all features

Simply open the Example Project and press Play to see everything in action!

## 📚 Documentation

Comprehensive documentation is included in the `Documentation/` folder:

### Getting Started
- **QUICK_TEST_SETUP.md** - 5-minute quick start guide
- **WEAPON_SYSTEM_QUICKSTART.md** - Weapon system overview
- **FRAMEWORK_BLUEPRINT_REFERENCE.md** - Complete Blueprint API reference

### Core Systems
- **EVOLUTION_SYSTEM_GUIDE.md** - Weapon evolution system
- **LOOT_SYSTEM_GUIDE.md** - Loot drop configuration
- **VACUUM_SYSTEM_GUIDE.md** - Pickup collection system
- **PLAYER_STATS_DATAASSET_GUIDE.md** - Player stats configuration

### Progression Systems
- **POWERUP_SHOP_QUICKSTART.md** - PowerUp shop and meta progression
- **CHARACTER_SELECTION_QUICKSTART.md** - Character selection system
- **FALLBACK_CARDS_GUIDE.md** - Fallback card system

### Advanced Features
- **TIME_LIMIT_QUICKSTART.md** - Time limit and endless mode
- **WAVE_DATA_EXAMPLE.md** - Wave configuration examples
- **EXAMPLE_WEAPONS_GUIDE.md** - Weapon implementation examples

### UI Integration
- **PLAYER_UI_EASY_GUIDE.md** - Easy UI functions for widgets
- **PICKUP_DEBUG_COMMANDS.md** - Debug console commands

### Troubleshooting
- **WEAPON_CONFIGURATION_TROUBLESHOOTING.md** - Common issues and solutions
- **P0_FIXES_SUMMARY.md** - Critical fixes and best practices

## 🎯 Core Components

### URFHealthComponent
Manages health, damage, healing, and regeneration
- Armor support
- Health regeneration with delay
- Death handling
- Blueprint events for damage/healing

### URFWeaponComponent
Manages weapon inventory and firing
- 6-slot weapon inventory
- Auto-fire system
- Weapon leveling
- Evolution system
- Passive item tracking

### URFExperienceComponent
Handles XP and leveling
- Configurable XP curve
- Skill point system
- Level rewards
- Max level support

### URFPlayerStatsComponent
Calculates player stats with PowerUp bonuses
- Combat stats (Health, Armor, Recovery, Move Speed)
- Weapon stats (Might, Area, Speed, Duration, Cooldown, Amount)
- Progression stats (Growth, Greed, Magnet, Luck)
- Utility stats (Revival, Reroll, Skip, Banish, Curse)

### URFLevelUpSystem
Manages level-up card selection
- 3-card selection system
- Weapon acquisition and upgrades
- Fallback cards support
- Easy UI integration

### URFGameDirector
Controls wave-based enemy spawning
- Wave progression system
- Difficulty scaling
- Special events
- Time limit support

## 🛠️ Weapon Types

### Projectile Weapons
Fire projectiles at enemies
- Homing support
- Pierce support
- Bounce support
- Critical hits
- Example: Magic Wand

### Melee Weapons
Continuous damage aura
- Radius-based damage
- Damage intervals
- Critical hits
- Example: Garlic

### Beam Weapons
Rotating beam damage
- Sweeping area damage
- Configurable rotation speed
- Continuous damage
- Example: Holy Wand

### Area Weapons
Temporary damage zones
- Ground-based areas
- Duration-based
- Multiple instances
- Example: Santa Water

### Orbit Weapons
Orbiting damage objects
- Defensive rotation
- Multiple orbiters
- Collision damage
- Example: King Bible

### Bounce Weapons
Bouncing projectiles
- Chain between enemies
- Configurable bounces
- Damage falloff
- Example: Lightning Ring

### Passive Weapons
Passive effects
- No active firing
- Stat modifications
- Evolution requirements
- Example: Spinach

## 💎 PowerUp System

### PowerUp Shop
Meta progression between runs
- Persistent upgrades
- Currency-based purchases
- Stat modifications
- Unlock system

### PowerUp Types
- **Stat Modifiers** - Increase player stats
- **Weapon Unlocks** - Unlock new weapons
- **Character Unlocks** - Unlock new characters
- **Utility Upgrades** - Rerolls, skips, revivals

## 🎨 Easy UI Integration

Framework provides Easy UI functions for simplified widget integration:

```cpp
// Get player stats globally
Get Current Health (Easy UI)
Get Max Health (Easy UI)
Get Health Percentage (Easy UI)

// Get weapon info globally
Get Weapon Count (Easy UI)
Get All Weapon Slots (Easy UI)

// Card selection globally
Get Card Options (Easy UI)
Select Card (Easy UI)
Get Card Name (Easy UI)
```

No need to find player reference - works from any widget!

## 🐛 Debug Features

### Console Commands
```
URF.Debug.ShowPickups - Toggle pickup debug display
URF.Debug.ShowWeapons - Toggle weapon debug display
URF.Debug.ShowHealth - Toggle health debug display
URF.Debug.GiveXP [amount] - Grant XP
URF.Debug.SetLevel [level] - Set player level
URF.Debug.SpawnPickup [type] - Spawn test pickup
```

### Visual Debugging
- On-screen debug info for all systems
- Configurable per-component
- Performance metrics
- Collision visualization

## 📊 Performance

Optimized for Vampire Survivors-style gameplay:
- Handles 500+ enemies simultaneously
- Object pooling for projectiles and pickups
- Efficient collision detection
- Minimal garbage collection
- 60+ FPS on mid-range hardware

## 🤝 Support

### Documentation
- 20+ detailed guides included
- Complete Blueprint API reference
- Example implementations
- Troubleshooting guides

### Community
- Discord: https://discord.gg/QJxvpuyUv8
- GitHub: https://github.com/CanTATARDev/UltimateRoguelikeFramework

### Updates
Regular updates with new features and improvements

## 📄 License

Copyright 2026 CanTATAR. All Rights Reserved.

This plugin is licensed for use with Unreal Engine projects. See Fab EULA for details.

## 🏆 Credits

Developed by CanTATAR
Inspired by Vampire Survivors by poncle

## 📝 Version

**Version:** 1.0.0  
**Release Date:** 2026-02-18  
**Engine Version:** UE 5.0+

---

**Ready to build your roguelike?** Check out the Example Project and Documentation folder to get started!
