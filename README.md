# Snake Game in Python

## 🎮 Introduction

This is a classic **Snake Game** built using **Python and Pygame**. The player controls a snake to eat apples, growing in size while avoiding collisions with the walls and itself. The game features smooth animations, sound effects, and engaging graphics.

## 🚀 Features

- **Classic Snake Mechanics**: Eat apples to grow the snake and increase the score.
- **Pixel-Perfect Graphics**: Smooth snake movement with head, body, and tail rendering.
- **Sound Effects**: Crunch sound when eating apples.
- **Automatic Movement**: The snake moves continuously in the last pressed direction.
- **Game Over Logic**: Restart the game when colliding with itself or the walls.
- **Score Counter**: Display of the player’s current score.

## 🛠️ Installation & Setup

1. **Clone the Repository**
   ```sh
   git clone https://github.com/yourusername/snake-game.git
   cd snake-game
   ```
2. **Install Dependencies**
   Ensure you have Python installed (3.8+ recommended), then run:
   ```sh
   pip install pygame
   ```
3. **Run the Game**
   ```sh
   python main.py
   ```

## 🎨 Game Assets

Make sure the following assets exist inside the correct directories:

- `Graphics/`
  - `head_up.png`, `head_down.png`, `head_left.png`, `head_right.png`
  - `body_vertical.png`, `body_horizontal.png`
  - `body_tr.png`, `body_tl.png`, `body_br.png`, `body_bl.png`
  - `tail_up.png`, `tail_down.png`, `tail_left.png`, `tail_right.png`
  - `apple.png`
- `Sound/`
  - `crunch.wav`
- `Font/`
  - `PoetsenOne-Regular.ttf`

## 🎮 Controls

| Key           | Action     |
| ------------- | ---------- |
| `Arrow Up`    | Move Up    |
| `Arrow Down`  | Move Down  |
| `Arrow Left`  | Move Left  |
| `Arrow Right` | Move Right |
| `ESC`         | Quit Game  |

## 🌍 Deploying the Game to the Web (Using pygbag & Vercel)

1. **Ensure Pygbag is Installed**
   ```sh
   pip install pygbag
   ```
2. **Move `main.py` to a Web-Friendly Folder**
   ```sh
   mkdir snake_game_web
   mv main.py snake_game_web/
   cd snake_game_web
   ```
3. **Run Pygbag**
   ```sh
   python -m pygbag .
   ```
4. **Build for Web Deployment**
   ```sh
   python -m pygbag --build .
   ```
   The final game files will be available inside `build/web/`.
5. **Deploy on Vercel**
   - In Vercel's project settings, set:
     - **Install Command**:
       ```sh
       pip install pygbag
       ```
     - **Build Command**:
       ```sh
       python -m pygbag --build .
       ```
     - **Output Directory**:
       ```
       build/web
       ```
6. **Host the Game Online**
   Upload the `build/web/` folder to Vercel or other static hosting services like **GitHub Pages, Netlify, or Itch.io**.

## ❗ Troubleshooting

- If `pygame` fails to install, try updating `pip`:
  ```sh
  python -m pip install --upgrade pip
  ```
- If assets are missing, ensure the `Graphics/`, `Sound/`, and `Font/` folders are correctly placed in the project directory.
- If the game is lagging, try reducing the `clock.tick(144)` value inside `main.py`.


