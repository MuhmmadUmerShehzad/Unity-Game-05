# Game #05 - Lunar Lander

A Unity-based 2D space game where players control a lunar lander spacecraft, navigating through multiple levels while managing fuel and attempting precise landings.

## Project Overview

This is a multi-level space simulation game built in Unity featuring:
- **Lunar Lander Mechanics**: Control a spacecraft with directional thrusting and fuel management
- **Dynamic Levels**: Multiple procedurally-designed levels with varying difficulty
- **Scoring System**: Earn points based on landing accuracy, speed, and angle
- **Progressive Difficulty**: Advance through increasingly challenging levels
- **Audio & Visual Feedback**: Dynamic visuals and sound effects for immersive gameplay

## Features

### Core Gameplay
- **Lander Control**: Utilize up/left/right thrust to navigate and control your spacecraft
- **Fuel Management**: Limited fuel supply that depletes with thrust usage
- **Landing System**: Multiple landing conditions:
  - ✅ Successful landing on designated landing pads
  - ❌ Failed landings (wrong area, too steep angle, or excessive speed)
- **Coin Collection**: Collectible coins for bonus points

### Game Systems
- **Level Progression**: Complete levels sequentially to unlock the next challenge
- **Scoring Mechanics**: Dynamic scoring based on landing quality and angle
- **Cinemachine Camera Integration**: Smooth camera tracking following the lander
- **Real-time Timer**: Track gameplay duration for each level
- **Audio System**: Sound effects for thrust, landings, coin pickups, and fuel collection

### UI Elements
- **Stats Display**: Real-time score, fuel, and timer information
- **Main Menu**: Navigation to start the game
- **Landing Summary**: Post-landing statistics and results

## Project Structure

```
Assets/
├── Scripts/
│   ├── Game Manager.cs          # Core game logic and level management
│   ├── Lander.cs                # Player spacecraft controller
│   ├── GameLevel.cs             # Individual level setup and configuration
│   ├── GameInput.cs             # Input handling system
│   ├── LandingPad.cs            # Landing zone logic
│   ├── LandingPadVisual.cs      # Landing pad visual effects
│   ├── CoinPickup.cs            # Collectible coin mechanics
│   ├── Fuel.cs                  # Fuel collectible items
│   ├── LanderVisuals.cs         # Visual effects for the lander
│   ├── LanderAudio.cs           # Sound effects for the lander
│   ├── CinemechineCameraZoom2D.cs # Camera zoom mechanics
│   ├── StatsUI.cs               # In-game statistics display
│   ├── LandedUI.cs              # Landing result display
│   ├── MainMenuUI.cs            # Main menu interface
│   ├── SoundManager.cs          # Global audio management
│   ├── SceneLoader.cs           # Scene management and transitions
│   └── InputActions.cs           # Input action definitions
├── Scenes/
│   ├── MainMenuScene
│   └── GameScene
├── Prefabs/
│   ├── Lander
│   ├── Landing Pad
│   ├── Coin
│   └── Other interactive objects
├── Sounds/
│   ├── Thrust effects
│   ├── Landing effects
│   ├── Coin pickup
│   └── Background music
├── Textures/
│   ├── Lander sprites
│   ├── Environment assets
│   └── UI elements
└── Resources/
```

## Key Classes

### GameManager
Singleton class that manages:
- Level loading and progression
- Score tracking and updates
- Game state management
- Event handling for game events

### Lander
Main player-controlled spacecraft featuring:
- Physics-based movement with gravity
- Thrust control system
- Collision detection and landing logic
- Multiple landing outcome types
- Event system for game interactions

### GameLevel
Level configuration class handling:
- Level identification
- Starting position setup
- Camera target positioning
- Zoom parameters

### Input System
- Modern Unity Input System integration
- Support for keyboard and gamepad controls
- Touch input for mobile platforms

## Gameplay Mechanics

### Thrust System
- **Up Thrust**: Main engine acceleration
- **Left Thrust**: Counter-clockwise rotation and left movement
- **Right Thrust**: Clockwise rotation and right movement
- **Gravity**: Constant downward acceleration (0.7x normal)

### Fuel System
- Limited fuel reserve (10 units by default)
- Consumption rate: 1 fuel per thrust action
- Depletion halts propulsion
- Fuel pickups available in levels

### Landing Conditions
Landing success is determined by:
- Landing on designated pads (Success)
- Angle of approach (TooSteepAngle failure if exceeded)
- Landing velocity (TooFastLanding failure if exceeded)
- Landing location (WrongLandingArea failure)

### Scoring
Points awarded for:
- Successful precision landings (base score)
- Landing angle multiplier
- Landing speed bonus/penalty
- Coin collection (500 points each)
- Level completion bonuses

## Technologies Used

- **Engine**: Unity (2D)
- **Scripting**: C# (.NET)
- **Camera System**: Cinemachine
- **Input**: Unity Input System
- **Rendering**: Universal Render Pipeline (URP)
- **UI**: TextMeshPro
- **Physics**: 2D Rigidbody2D

## Controls

| Action | Input |
|--------|-------|
| Thrust Up | W / Up Arrow / Gamepad Y |
| Thrust Left | A / Left Arrow / Gamepad X |
| Thrust Right | D / Right Arrow / Gamepad B |
| Pause/Menu | Escape |

## Building & Running

### Prerequisites
- Unity 2022 LTS or later
- .NET 4.x or IL2CPP scripting backend


### Building Standalone
- Go to `File → Build Settings`
- Select target platform (PC, Mac, Web, etc.)
- Click `Build and Run`

## Development Notes

### Architecture Patterns
- **Singleton Pattern**: GameManager, Lander, SoundManager
- **Event-Driven**: Loose coupling through C# events
- **Prefab-Based**: Modular, reusable game objects

### Performance Optimization
- Cinemachine for efficient camera management
- 2D physics with Rigidbody2D
- Sprite-based rendering for mobile optimization
- Object pooling for collectibles

## Future Enhancements

- [ ] Mobile touch controls optimization
- [ ] Difficulty settings
- [ ] Leaderboard system
- [ ] Additional level packs
- [ ] Power-up mechanics
- [ ] Multiplayer/Co-op modes
- [ ] Online score submission
- [ ] Customizable spacecraft

## License

This project is part of a coding tutorial series and is provided as-is for educational purposes.

## Support

For issues or questions about the project, refer to the code comments or review the individual script documentation within the Assets/Scripts folder.

---

**Game #05** - Precision Lunar Landing Challenge
