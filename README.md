# OpenBattleship2D

A simple 2D Battleship–style game in C++ leveraging OpenGL (FreeGLUT/GLEW) and the CImg toolkit.

![Gameplay Sketch](screenshot.png)

## Features

* **OpenGL / FreeGLUT rendering** with basic primitives: squares, triangles, circles, rounded rectangles, torus
* **Randomized movement & timers** for dynamic object animation
* **CImg integration** for optional image handling and loading
* Cross-platform utility functions for degree/radian conversion, RNG, and primitive drawing

## Prerequisites

Tested on **Ubuntu 20.04 LTS**. Install dependencies with:

```bash
sudo apt-get update
sudo apt-get install build-essential freeglut3-dev glew-utils libglew-dev libfreeimage-dev
```

Ensure you have:

* A C++11-capable compiler
* OpenGL & GLUT development headers
* GLEW and FreeImage libraries
* (Optional) CImg header (`CImg.h`)

## Building

1. **Install libs**

   ```bash
   ./install-libraries.sh
   ```

2. **Build**

   ```bash
   make
   ```

Or compile manually:

```bash
g++ -std=c++11 game.cpp util.cpp -o Battleship \
    -lGL -lGLU -lglut -lGLEW -lfreeimage
```

## Usage

```bash
./Battleship
```

* Arrow keys and internal timer callback drive object movement
* Press **Esc** to quit

## File Structure

```
.
├── Makefile                 # Build rules
├── install-libraries.sh     # Installs Ubuntu dependencies
├── CImg.h                   # CImg image-processing toolkit
├── util.h / util.cpp        # Primitives & RNG utilities
└── game.cpp                 # Main game loop & rendering logic
```

## Extending

* Add new shapes or effects in `util.cpp`
* Expand `game.cpp` with full Battleship mechanics—ship placement, hit detection, scoring

---

**License:** MIT © 2025
