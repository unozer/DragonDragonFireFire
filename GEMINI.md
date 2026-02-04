# Dragon Dragon Fire Fire Project Overview

"Dragon Dragon Fire Fire" is a Godot 4 game project developed using GDScript. It is structured around a robust autoloading system that provides centralized management for global signals, game state, high scores, sound effects, background music, and user settings. The `GameRoot` scene serves as the primary orchestrator, managing transitions between different game scenes (Title Screen, Main Game Scene, and End Screen) and handling rendering configurations, including CRT shader effects. The project defines custom input actions and 2D physics layers for a well-organized gameplay experience.

## Project Structure Highlights

*   **`src/`**: Contains all project files, including Godot scenes (`.tscn`), scripts (`.gd`), and assets.
*   **`src/autoloads/`**: Houses global scripts that are automatically loaded at game startup, providing common functionalities across the project (e.g., `GameState`, `Signals`, `SoundPool`, `MusicPlayer`, `Settings`).
*   **`src/game_root/`**: Contains the `GameRoot.gd` script and `game_root.tscn` scene, which act as the main entry point and scene manager for the entire game. `SceneDefinitions.gd` within this directory defines all playable scenes.
*   **`src/player/`**: Contains player-related scripts and scenes. `PlayerUtils.gd` is an autoloaded utility script for player-specific functions.
*   **`src/assets/`**: Dedicated directory for all game assets (textures, music, sound effects).

## Building and Running

This project is built with the Godot Engine (version 4.x). To open and run the game:

1.  **Install Godot Engine 4.x:** If you don't have it, download and install the appropriate version of the Godot Engine from the official website.
2.  **Open the Project:**
    *   Launch the Godot Engine.
    *   From the project list, select "Import" or "Scan" and navigate to the `src/` directory of this project.
    *   Select the `project.godot` file.
3.  **Run the Game:** Once the project is open in the Godot editor, you can run the game by pressing the "Play" button (typically F5).

## Development Conventions

*   **Language:** GDScript is the primary scripting language used throughout the project.
*   **Global State Management:** The project makes extensive use of Godot's autoload feature to manage global game state, signals, audio, and settings, promoting a clean separation of concerns and easy access to core functionalities.
*   **Scene Transitions:** Scene changes are centrally managed by the `GameRoot` script, which uses `SceneDefinitions` to orchestrate transitions between the Title Screen, Main Game Scene, and End Screen.
*   **Input Mapping:** All significant player inputs (e.g., `jump`, `fire`, movement) are defined as actions in `project.godot`, allowing for flexible remapping and consistent input handling.
*   **Physics Layers:** Custom 2D physics layers are defined in `project.godot` (e.g., `Player`, `Enemies`, `Projectiles`, `StaticGeometry`), aiding in precise collision detection and interaction management.
*   **Asset Organization:** All art, sound, and music assets are organized within the `src/assets/` directory as per the project template's guidelines.
