# Worms68k Party

Welcome to **Worms68k Party**, a full-featured Worms clone for the TI-89 and TI-89 Titanium graphing calculators. Inspired by *Worms World Party* (WWP), this project brings the classic artillery strategy experience to the Motorola 68000-based calculators, featuring 77 unique weapons, textured grayscale maps, and a robust physics engine.

**Note:** This version is a human-vs-human (hotseat) experience and does not currently include AI players.

### 🌐 Official Website
For more information, screenshots, and downloads, visit the main project page:  
[https://orokro.github.io/Worms68k-Party/#/](https://orokro.github.io/Worms68k-Party/#/)

---

## 🚀 Installation & Usage

The latest stable builds are located in the `/dist` folder.

1.  **Backup Your Data:** This game is memory-intensive. Backup your calculator and archive unused variables.
2.  **Create Folder:** On your TI-89, create a folder named `worms`.
3.  **Transfer Files:** Use TI-Connect or TILP to transfer the following into the `worms` folder:
    *   `wgame.89z` (The main game engine)
    *   `wmenu.89z` (The menu system and map generator)
    *   `worms68k.89p` (TI-Basic loader)
    *   `wormsdat.89e` (Essential game data)
4.  **Archive Everything:** In `[VAR-LINK]`, select all four files and **Archive** them. Running from archive is mandatory to prevent RAM-related crashes.
5.  **Launch:** Type `worms68k()` on the home screen and press `[ENTER]`.

---

## 🛠️ Development Information

### Build Environment
This project is built using the **GCC4TI IDE**, a community-maintained fork of the original TIGCC project. It provides a modern C/ASM development environment for the TI-68k series.
*   **Official Homepage:** [https://debrouxl.github.io/gcc4ti/info.html](https://debrouxl.github.io/gcc4ti/info.html)

### Sprite Management
The game uses a custom workflow for handling graphical assets:
*   **Automated Conversion:** `makeSprites.js` converts BMP images from the `SpriteBitmaps/` folder into C-style bitmask arrays.
*   **Extraction:** `extract_sprites.js` can reverse this process, extracting BMPs from the source code.
*   **Requirements:** These scripts require **Node.js** to run.
*   **Manual Editing:** While automated, the sprite data can be manually edited in `c/SpriteData.c` and `h/SpriteData.h`. Each sprite is stored as a series of binary literals (e.g., `0b101010...`) for easy visual tweaking.

---

## 🏗️ Architecture Overview

The project is split into two primary components: the **Main Game** and the **Menu System**.

### 🎮 Game Engine & State Machine
The core gameplay logic is driven by a robust state machine defined in `c/Game.c`. This design ensures clean transitions between different phases of gameplay:
*   **States (`c/States/`):** Individual logic for `Turn`, `WeaponSelect`, `Cursor`, `Death`, `AfterTurn`, and `Pause`.
*   **Physics & Collision (`c/PhysCol.c`):** Handles pixel-perfect collision detection against the destructible terrain and object physics.
*   **Map System (`c/Map.c`):** Manages the generated landscape, including destruction (explosions carving holes) and texture mapping.
*   **Rendering (`c/Draw.c`):** Orchestrates the grayscale drawing, including parallax backgrounds (clouds, mountains) and particle systems (leaves).
*   **Input (`c/System/Keys.c`):** Maps the TI-89's physical keys to logical game controls.

### 📋 Menus Project (`/Menus`)
The menu system is a separate project (compiling to `wmenu.89z`) that handles:
*   Match configuration (Health, Turn Time, Weapons).
*   Terrain generation (Island, Towers, Caves).
*   Inter-process communication via the `wormsdat` data file.

---

*(C) Greg Miller, 2026. This is a non-commercial fan project. Worms is a trademark of Team17.*
