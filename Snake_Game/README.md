# Snake Game 🐍

A classic Snake game implementation in Python using the Turtle graphics library. Navigate your snake, eat food, and grow longer while avoiding walls and colliding with yourself!

## Overview

This is a single-player Snake game built with Python's Turtle module. The game features a simple yet engaging gameplay loop where players control a snake to eat food, grow in length, and accumulate points while avoiding collisions.

## Features

- 🎮 **Interactive Controls** - Smooth arrow key-based movement
- 🍎 **Food Collection** - Randomly spawned food items to grow your snake
- 📊 **Score Tracking** - Real-time score display at the top of the screen
- 🎯 **Collision Detection** - Game ends on wall collision or self-collision
- 🖥️ **Responsive Gameplay** - 600x600 pixel game window with optimized frame rate

## Game Mechanics

### Objective
Guide your snake to eat food and grow as long as possible without hitting the walls or colliding with your own tail.

### Controls
- **↑ Up Arrow** - Move snake up
- **↓ Down Arrow** - Move snake down
- **← Left Arrow** - Move snake left
- **→ Right Arrow** - Move snake right

### Game Rules
1. **Eating Food** - When the snake's head touches the blue food, the snake grows by one segment and your score increases by 1
2. **Wall Collision** - The game ends if the snake goes beyond the 600x600 pixel boundary
3. **Self-Collision** - The game ends if the snake's head touches any part of its own body
4. **Snake Movement** - The snake cannot reverse into itself (e.g., cannot go left if moving right)

## File Structure

### `main.py`
The main game loop and core logic:
- Initializes the game window (600x600 pixels, black background)
- Creates instances of Snake, Food, and Scoreboard
- Sets up keyboard event listeners for player input
- Implements collision detection (food, walls, and self)
- Updates the game state at regular intervals
- Manages game-over conditions

### `snake.py`
Defines the Snake class and movement logic:
- **`__init__()`** - Creates a snake with 3 initial segments
- **`create_snake()`** - Builds the starting snake configuration
- **`add_segment(position)`** - Adds a new segment to the snake
- **`extend()`** - Grows the snake when food is eaten
- **`move()`** - Moves the snake forward by updating segment positions
- **`up()`, `down()`, `left()`, `right()`** - Direction control methods with prevention of reverse movement

### `food.py`
Defines the Food class:
- **`__init__()`** - Creates a blue circular food item
- **`refresh()`** - Randomly spawns food at a new location within the game boundary

### `scoreboard.py`
Manages the game score and game-over display:
- **`__init__()`** - Sets up the scoreboard at the top of the screen
- **`update_scoreboard()`** - Displays current score
- **`increase_score()`** - Increments score when food is eaten
- **`game_over()`** - Displays "GAME OVER" message at the center of the screen

## Requirements

- Python 3.x
- Turtle module (built-in with Python)

## How to Run

1. Ensure Python 3 is installed on your system
2. Navigate to the project directory:
   ```bash
   cd Snake_Game
   ```
3. Run the main game file:
   ```bash
   python main.py
   ```
4. The game window will open - use arrow keys to play
5. Click anywhere on the game window to close it after Game Over

## Game Dimensions

- **Screen Size** - 600x600 pixels
- **Game Boundary** - -280 to 280 in both X and Y coordinates
- **Snake Segment Size** - 20x20 pixels
- **Food Size** - 10x10 pixels (scaled at 0.5)
- **Game Speed** - 100ms per frame

## Code Structure Highlights

- **Object-Oriented Design** - Uses classes for Snake, Food, and Scoreboard
- **Modular Architecture** - Each component is separated into its own file
- **Collision Detection** - Three types of collisions handled: food, wall, and self
- **Event-Driven Input** - Uses Turtle's `onkey()` for responsive controls

## Future Enhancement Ideas

- Add difficulty levels or increasing speed
- Implement high score tracking
- Add power-ups or special food items
- Create an obstacles feature
- Add sound effects and animations
- Implement pause/resume functionality

## License

This is a personal project for educational purposes.
