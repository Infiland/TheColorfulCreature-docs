# Game Engine

The Colorful Creature is built using GameMaker Studio 2, a 2D game engine.

## Engine Version
- GameMaker 2024.11 (Latest stable release)
- [Download GameMaker](https://gamemaker.io/en/download)

## Key Features Used

### Core Engine Features
- Built-in physics system for precise platformer mechanics
- Sprite-based animation system for fluid character movement
- Particle systems for visual effects
- Room-based level design
- Built-in collision detection system

### Performance
- Hardware-accelerated rendering
- Optimized for both low-end systems
- Efficient memory management for large levels

### Platform Support
- Windows (Primary platform)
- macOS
- Linux

## Development Tools

### GameMaker IDE Features
- Visual room editor for level design
- Sprite editor with animation tools
- Built-in code editor with GML support
- Asset management system
- Integrated debugger (F6)
- Real-time testing (F5)

### GML (GameMaker Language)
The game is written in GML, GameMaker's proprietary scripting language. Key features used:

- Object-oriented programming
- Event-driven architecture
- Built-in functions for:
  - Color manipulation
  - Physics calculations
  - Input handling
  - File I/O
  - Steam integration

## Extensions
- Steamworks SDK integration
- Google Play Games Services integration
- Google AdMob integration
- Custom shader for color-blindness simulation

## Issues
- No delta time, so movement is affected by frame rate, which is why the game is forced to run at 60 FPS.
- No UI system, so all UI is handled in the game.
- No particle system implemented
- The game has forced resolution at 1024x768, so scaling is not possible without a major rewrite.

## Resources
- [GameMaker Documentation](https://manual.yoyogames.com/)
- [GML Reference](https://manual.yoyogames.com/GameMaker_Language/GML_Reference/GML_Reference.htm)
- [GameMaker Marketplace](https://marketplace.yoyogames.com/) 