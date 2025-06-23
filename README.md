# pacman-game-using-python
A fully functional Pac-Man game built in Python using Pygame! Navigate the maze, collect berries, avoid or chase ghosts, and aim for a high score.

📥 Features
Classic maze gameplay with dots (berry) and power-ups (big berries)

Four ghosts with basic AI movement

Multi-level progression: faster ghosts and respawned berries

Player life system with lives shown on-screen

Score tracking and level display

Game Over and restart functionality

🔧 Getting Started
Prerequisites
Python 3.7+

Pygame

Install Pygame using pip:

bash
Copy
Edit
pip install pygame
🗂 Repository Structure
bash
Copy
Edit
.
├── assets/               # Sprite and life icon images
├── animation.py         # Sprite loading
├── cell.py              # Wall tiles
├── berry.py             # Dot/power-up logic
├── ghost.py             # Ghost behavior
├── pac.py               # Player (Pac-Man) logic
├── settings.py          # Map layout & constants
├── world.py             # Game world, rendering & logic
└── main.py              # Game loop entry point
📘 Map & Game Settings
Maze is defined in settings.py as a 2D MAP array:

'1' = walls

' ' = small berries

'B' = big berries (power-ups)

'P' = Pac-Man start

's', 'p', 'o', 'r' = ghost start positions (sky‑blue, pink, orange, red)

Other key settings include tile size, screen dimensions, and movement speeds.

🎨 Asset Loading
animation.py contains:

python
Copy
Edit
def import_sprite(path):
    # Loads all images in directory at runtime into Pygame surfaces
All assets in assets/ are loop-loaded to create animations.

👻 Game Logic
All main gameplay happens in world.py using the World class:

_generate_world(): Spawns walls, berries, ghosts, and player

update(): Handles movement, collisions, score, level transitions

_dashboard(): Displays lives, score, level on screen

generate_new_level(): Refills berries and speeds up ghosts

restart_level(): Resets everything after Game Over

Ghost and player collisions deduct lives unless within power-up time.

🖱 Controls
Key	Action
Arrows	Move Pac-Man
R	Restart after Game Over

Close window or press ESC to quit.

🚀 Playing the Game
Run:

bash
Copy
Edit
python main.py
A window opens with Pac-Man navigating the maze. Eat berries (10 points), big berries (50 points + power-up), and vulnerable ghosts (+100 points). After clearing the stage, move to the next level—ghosts get faster!

🛠 Possible Enhancements
Improved ghost AI (easy/moderate/hard chase modes)

Smooth animation and sprite direction control

Sound effects and background music

High-score saving and menu system

Graphical menus or portal logic for screen wrap-around

✅ License
MIT License — feel free to use, modify, and share!
