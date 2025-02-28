# Game Mechanics

## Player Object (o_player)

The player is the main character in The Colorful Creature, controlled by keyboard/gamepad or touch controls on mobile.

### Core Properties

- **Movement Speed**: Base walking speed is 4 pixels per frame
- **Gravity**: Default gravity is 0.5, can be modified by gravity items
- **Jump**: Configurable jump controls with coyote time of 0.2 seconds
- **Double Jump**: Can be acquired through power-ups
- **Ice Physics**: Special movement handling on ice blocks with gradual acceleration/deceleration

### States & Mechanics

- **Water Mechanics**
  - Breath meter (500 units)
  - Drowning when breath reaches 0
  - Slower movement in water (divided by water factor)
  - Visual breath indicator above player
  - Automatic breath recovery when out of water

- **Color System**
  - Can change between colors (Red, Yellow, Green, Blue, White)
  - Color affects interaction with matching blocks/items
  - Visual color blending on player sprite
  - Color pickup cooldown system
  - Stats tracking for color changes

### Interaction Mechanics

- **Item Collection**
  - Interactive pickup system with button press
  - Cooldown system for rapid interactions
  - Visual feedback particles on collection
  - Stats tracking for pickups
  - Platform-specific controls (PC/Mobile)

- **Special Interactions**
  - Spiral items for color changes
  - Oxygen refill items
  - Speed modification items
  - Gravity alteration items
  - Key collection system
  - Weapon/ammunition pickups
  - Double jump items

### Visual Features

- **Cosmetic Skins**
  - Customizable skins
  - Customizable hats
  - Customizable items
  - Support for modded hats, support for items and skins coming later.

### Controls

- **Keyboard/Gamepad**
  - Left/Right movement
  - Jump
  - Interact
  - Restart level
  - Platform-specific button mapping

- **Mobile**
  - Touch controls via Android-specific buttons
  - Left/Right virtual buttons
  - Jump button
  - Interact button
  - Restart button

### Special Features

- **Checkpoint System**
  If the player has casual mode enabled, the game will spawn checkpoints depending on if that setting is on or off.
  When it's on and the player has hit the checkpoint, if the player dies, the game will load the last checkpoint.

  - Saves position (X,Y)
  - Preserves color state
  - Maintains gravity settings
  - Keeps ammunition count
  - Remembers gun equipment status

- **Particle Effects**
  - Walking particles
  - Customizable particle frequency
  - Different effects based on movement direction
  - Special effects for different surfaces
  - Pickup effect particles

### Collision System

- **Block Types**
  - Standard solid blocks
  - One-way platforms (up/left/right)
  - Ice blocks with special physics
  - Moving blocks (all colors)
  - Ladder interaction
  - Slope handling
  - Hazard blocks (lava, fire)
  - Delete blocks

### Debug Features

- **Noclip Mode**: Free movement ignoring collisions
- **Jump Testing**: Debug variables for jump height analysis
- **Writing Mode**: Affects horizontal speed calculations
- **Visibility Toggle**: For testing invisible skin
- **FPS Compensation**: Movement adjusted for different frame rates
- **Cheat Detection**: Special skin features tied to cheat status