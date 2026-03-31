WORMS68K PARTY - README
=====================

Worms68k Party is a full Worms clone inspired by Worms World Party, for the TI-89 and TI-89 Titanium graphing calculators.

--------------------------------------------------------------------------------
I. INSTALLATION GUIDE
--------------------------------------------------------------------------------

IMPORTANT: BACK UP YOUR DATA!
Worms68k Party is memory-intensive and pushes the TI-89 to its limits. Ensure 
you have backed up all important variables and programs. ARCHIVE EVERYTHING 
you aren't using to free up RAM.

Requirements:
- TI-89 or TI-89 Titanium calculator.
- Approximately 96 KB of storage space.
- TI-Connect (Windows) or TILP (Linux/macOS) software.

Steps:
1. Download and Extract: Extract the contents of Worms68kParty.zip.
2. Setup Folder: On your TI-89, create a new folder called 'worms' 
   ([2nd] [VAR-LINK], then [F1] -> 5:Create Folder).
3. Set Directory: Set 'worms' as your current directory (Type setFold(worms) on 
   the home screen).
4. Connect: Connect your calculator to your computer.
5. Transfer Files: Use TI-Connect or TILP to transfer the following files into 
   the 'worms' folder:
   - wgame.89z (Game Engine)
   - wmenu.89z (Menu System)
   - worms68k.89p (TI-Basic Loader)
   - wormsdat.89e (Game Data)
6. ARCHIVE EVERYTHING: Open [VAR-LINK], select all four files, and press 
   [F1] -> 8:Archive. Running from Archive is mandatory to prevent crashes.
7. Launch: On your home screen, type worms68k() and press [ENTER].

--------------------------------------------------------------------------------
II. HOW TO PLAY
--------------------------------------------------------------------------------

Worms68k Party uses a logical key system mapped to the TI-89 keyboard.

Core Gameplay Controls:
- [Arrow Keys]    : Move Worm left/right, Aim weapon up/down.
- [Diamond]       : Jump forward.
- [Alpha]         : Backflip (jump backward).
- [2nd]           : Fire Weapon / Action.
- [APPS]          : Select next Worm (when enabled).
- [CATALOG]       : Open Weapon Selection menu.
- [Shift]         : Hold to enable Camera Control (use Arrows to pan).
- [ESC]           : Pause game / Back to menu.

Specialist Controls:
- [1], [2], [3]   : Set weapon fuse timer (when applicable).
- [+] / [-]       : Adjust settings in menus.

--------------------------------------------------------------------------------
III. SETTINGS & FEATURES
--------------------------------------------------------------------------------

The game offers extensive customization via the Menu System (wmenu.89z).

Match Settings:
- Worm Health     : Starting HP (50, 100, or 200).
- Select Worms    : Toggle manual worm selection at turn start.
- Strategic Base  : Toggle manual worm placement at game start.
- Turn Time       : Set turn duration (30s, 45s, 60s, or 90s).
- Sudden Death    : Enable/disable water rise after 10 minutes.
- Artillery Mode  : Worms cannot move; aim and fire only.

Object & Crate Options:
- Mines           : Toggle Mines and set Fuse Length (0s to 4s, or random).
- Dud Mines       : Toggle the chance for mines to be duds (smoke only).
- Oil Drums       : Toggle explosive oil drums on the map.
- Crates          : Individually toggle Health, Weapon, and Tool crates.

Environmental Settings (Help & Settings Tab):
- Draw Clouds     : Toggle background clouds for performance.
- Draw Leaves     : Toggle falling leaf particles.
- Draw Mountains  : Toggle distant background mountain layer.

Map Customization:
- Generate random terrain with various themes (Island, Towers, etc.) and
  land types (Dirt, Rock, etc.).

--------------------------------------------------------------------------------
IV. PROJECT HISTORY & SYNOPSIS
--------------------------------------------------------------------------------

The journey of Worms68k Party began over 20 years ago in 2004. As a young 
programmer, I set out to create a full clone of Worms World Party for 
the TI-89. While an initial version was published, 
technical limitations and the 65k size limit prevented its completion.

In 2017, inspired by optimizations suggested by Lionel Debroux, the project 
underwent a scratch rewrite. This version established a rock-solid foundation, 
including a robust state machine and a unique "Mix-In" weapon system. However, 
a persistent camera bug eventually led to a hiatus.

Recently, with the aid of modern AI tools, the elusive bug was finally 
identified and fixed. This led to a final sprint in development, adding 
77 unique weapons, textured gray-scale maps, and a refined physics engine.

--------------------------------------------------------------------------------
(C) Greg Miller, 2026
Worms IP is owned by Team17 / Everplay Group.
This is a non-commercial fan project.
