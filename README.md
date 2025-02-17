# Cub3D

### Overview

Cub3D is a 3D graphical project inspired by Wolfenstein 3D, developed as part of the 42 curriculum. It features a custom raycasting engine, allowing for real-time rendering of a simple 3D world based on a 2D map.

![Gameplay Preview](./simplescreenrecorder-2025-02-14_09.49.53-ezgif.com-video-to-gif-converter.gif)

### Features

- Raycasting-based 3D rendering

- Custom parser for map validation

- Player movement and rotation

- Wall textures and basic shading

- MLX42 for graphical rendering

### Collaborators

- [**Vova Shkonda**](https://github.com/vovashko) - worked and the raycaster, graphical rendering and controls

- **Paulius Minialga (me)** - responsible for parsing and validation

### Installation
   ```bash
   git clone <repo-url>
   cd cub3D
   git submodule init
   git submodule update
   ```

To compile the project, ensure you have **GLFW** installed, then run:
   ```bash
   make
   ```
This will generate the cub3D executable.

### Usage

Run the program with a valid map file:
   ```bash
   ./cub3D maps/good/*.cub
   ```
### Map Format

The map should be a .cub file with the following format:

- First lines define textures and colors.

- Last section contains the map layout using **1** for walls, **0** for empty space and **NESW** for player placement.

Example:
   ```bash
   NO ./textures/north.jpg
   SO ./textures/south.jpg
   WE ./textures/west.jpg
   EA ./textures/east.jpg

   F 220,100,50
   C 255,255,255
   
   111111
   1S0001
   101001
   100001
   111111
   ```
### Controls

W / S - Move forward / backward

A / D - Strafe left / right

← / → - Rotate view left / right

ESC - Quit the game

### Dependencies

MLX42

GNU Make

cc

