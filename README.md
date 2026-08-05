# Maze Quest (PyOpenGL)

Maze Quest is a 2D grid-based maze explorer game built with **Python** and **PyOpenGL (GLUT)**.  
A random maze is generated each run, and the player must **collect all gold** and then reach the **goal** before the **time limit** ends — while avoiding obstacles.

## Gameplay Rules
- The maze is a **25×25 grid**.
- You start at **(0,0)** and the goal is at **(24,24)**.
- The maze contains:
  - **Gold (yellow circles)** → collect them all
  - **Obstacles (red circles)** → touching an obstacle ends the game
- You win only if:
  1) **All gold is collected**, and  
  2) You reach the **goal** square.
- If time runs out, the game ends.

## Features (based on the code)
- Random maze generation using a grid-based algorithm (paths + walls)
- Real-time movement with arrow keys and wall collision checking
- Gold placement and collection system
- Obstacle placement system (game over on collision)
- Time limit (default: **120 seconds**) with live countdown
- Mouse UI buttons:
  - **Restart** button resets the maze and game state
  - **Pause** button pauses gameplay and timer updates
- Simple character drawing using custom point/line/circle drawing logic

## Controls
### Movement
- ⬆️ Arrow Up: move up  
- ⬇️ Arrow Down: move down  
- ⬅️ Arrow Left: move left  
- ➡️ Arrow Right: move right  

### Actions
- **Enter**: collect gold (only works when standing on a gold cell)
- **J**: remove an obstacle (only works when standing on an obstacle cell)
- **ESC**: exit the game

### Mouse
- Click **Restart**: regenerate maze + reset everything
- Click **Pause**: pause/unpause the game

## Game Stats Display (right panel)
- Time limit and remaining time
- Gold collected and remaining
- Obstacles remaining
- Game state messages: PAUSED / GAME OVER / YOU'RE THE WINNER

## Requirements
- Python 3.x
- NumPy
- PyOpenGL and PyOpenGL_accelerate (recommended)

Install dependencies:
```bash
pip install numpy PyOpenGL PyOpenGL_accelerate
