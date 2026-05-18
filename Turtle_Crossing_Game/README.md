# Turtle Crossing Game

A simple Python Turtle game where the player guides a turtle across the road while avoiding moving cars. Each successful crossing advances the level and increases traffic speed.

## Gameplay

- Press the `Up` arrow key to move the turtle upward.
- Reach the top of the screen to complete a level.
- Each crossing increases the level and speeds up the cars.
- If the turtle collides with a car, the game ends.

## Requirements

- Python 3.x
- The built-in `turtle` module (included with standard Python installations)

## How to Run

1. Open a terminal or command prompt.
2. Change directory to `Turtle_Crossing_Game`.
3. Run:

```bash
python main.py
```

## File Overview

- `main.py` — game setup, main loop, collision detection, level progression
- `player.py` — turtle player class and movement logic
- `car_manager.py` — creates and moves cars, increases car speed per level
- `scoreboard.py` — displays current level and game over message

## Notes

- The game uses `time.sleep(0.1)` to control frame rate.
- Cars appear randomly from the right side and move left toward the player.
- The current implementation does not remove off-screen cars, so the car list may grow over time.

Enjoy the game!
