# Firestorm: 2D Platformer Game (Assembly)

[![Demo Video](https://img.youtube.com/vi/oKZdytaCIBE/0.jpg)](https://www.youtube.com/watch?v=oKZdytaCIBE)  
*Click the image above to watch the gameplay demo.*

https://www.youtube.com/watch?v=oKZdytaCIBE

---

## Overview

**Firestorm** is a 2D platformer written in **Assembly**, featuring custom sprite rendering, interactive mechanics, and asset pipelines built from scratch. The project demonstrates how low-level programming concepts can be applied to design engaging gameplay experiences.

---

## Features

- 🎮 **Core Mechanics**: Jumping, moving, hazard detection (lava)  
- 🖼 **Graphics**: Custom sprite and background rendering  
- ⚙️ **Physics**: Manual collision detection and movement logic  
- 🛠 **Asset Pipeline**: Python script to convert RGB images into usable Assembly data  
- 🧩 **Level Design**: Modular structure for adding more stages  

---

## Architecture & Implementation

- **Assembly (`game.asm`)**: Implements rendering, collision, input, and core game loop  
- **Python Converter**: Preprocesses background and sprite assets into binary-compatible formats  
- **Memory Management**: Handles sprite placement, platform movement, and hazard resets  
- **Rendering**: Uses Assembly routines for pixel drawing and background loading  

---

## Getting Started

### Prerequisites

- Assembly toolchain (assembler, linker, and emulator or physical hardware support)  
- Python 3.x (for asset conversion)  
- Terminal / IDE with build support  

### Build & Run

1. **Clone the repository**  
   ```bash
   git clone https://github.com/andrewaucie/platformgame.git
   cd platformgame
   ```
2. **Convert assets**
  ```bash
  python asset_converter.py input.png output.data
  ```

3. **Assemble & link**
  ```bash
  nasm -f elf game.asm -o game.o
  ld -m elf_i386 game.o -o game
  ```

3. **Run the game**
  ```bash
  ./game
  ```
## Controls

| Action            | Keybinding        |
|-------------------|------------------|
| Move Left/Right   | ← / → (or A / D) |
| Jump              | Space / ↑        |
| Reset Level       | R                |

---

## Roadmap

- Add multiple levels with progressive difficulty  
- Introduce enemies and AI behavior  
- Power-ups and collectibles  
- Background music and sound effects  
- Performance optimization and smoother rendering  

---

## Credits

- **Development**: [Andrew Aucie](https://github.com/andrewaucie)  
- **Assets**: Custom-created and converted with Python tooling  
- Special thanks to peers and mentors for feedback during development  

---

## License

This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.
