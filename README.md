# Built to Scale

A small browser-based puzzle platformer created as an attempt for the **GMTK Game Jam 2024** theme, **Built to Scale**.

Change your size to change what is possible. Cross scale gates to grow or shrink, use your new proportions to navigate platforms and obstacles, and experiment with moving boxes to make your way through nine handcrafted levels.

## Gameplay

The main mechanic is **scaling**: passing through a gate changes the size of the object that crosses it. Gates can affect both the player and movable boxes. Changing the player's size also changes movement and jumping, so choosing when and how to scale is part of each puzzle.

- **Nine levels**, introducing scale gates and increasingly involved platforming puzzles
- **Scale up or down** by crossing gates with different multipliers
- **Pushable boxes** that interact with platforms and scale gates
- **2D platformer physics** with gravity, friction, jumping, and collision handling
- **Music and sound controls** in the settings menu

This is a game-jam prototype rather than a polished commercial release.

## Controls

| Key | Action |
| --- | --- |
| **A** | Move left |
| **D** | Move right |
| **W** | Jump |
| **Esc** | Open or close the settings menu while playing |
| **Backspace** | Reset the current level |

**Tip:** Look for the numbers near gates: they indicate scale multipliers. Some gates can only be used a limited number of times.

## Play locally

The game is built with **HTML, CSS, and vanilla JavaScript**. No game engine, package manager, or build step is required.

1. Clone or download this repository.
2. Start a static HTTP server in the project folder. For example, with Python:

   ```bash
   python3 -m http.server 8000
   ```

3. Open **http://localhost:8000** in a desktop browser.
4. Select **SCALE** in the main menu to start.

A local server is recommended because browser restrictions may prevent fonts, audio, or other assets from loading correctly when opening `index.html` directly using `file://`.

## Technical overview

The game uses an **HTML Canvas** for rendering and a JavaScript animation loop for updates. Levels are defined as ASCII maps and enhanced with programmatically placed objects and triggers.

| File | Purpose |
| --- | --- |
| `index.html` | Game page, main menu, settings, and canvas |
| `styles.css` | UI styling and custom font |
| `scripts.js` | Game loop, physics, entities, level generation, and gate logic |
| `*.png` / `*.svg` | Sprites and UI images |
| `*.mp3` | Background music and sound effects |
| `built-to-scale.ttf` | Game font |
| `v1_0.zip` | Archived copy of the game |

### How levels work

`Level.fromASCII()` parses a text map into platforms, boxes, and the player spawn. Additional elements—including text, scale gates, and level exits—are configured in `generateAndReturnLevels()` inside `scripts.js`. Scale gates modify entity dimensions; the player also receives adjusted movement and jump properties.

## Project status

This repository preserves an experimental game-jam project. It is provided as-is for playing, exploring, and learning from the implementation.

## Credits

Created by [Rokoel](https://github.com/Rokoel) for the GMTK Game Jam's **Built to Scale** theme.

## License

No license file is currently included. Unless a license is added, the code and assets remain subject to their respective copyright restrictions.
