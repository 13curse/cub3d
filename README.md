# cub3d 🤖
This project aims to create a dynamic **3D view** inside a maze using the **raycasting** technique. Inspired by classic games like Wolfenstein 3D, it is built using the **MiniLibX** library, focusing on fundamental **3D game** mechanics, graphics **rendering**, and user interaction from a **first-person** perspective.

## Features

**Raycasting Engine:** Creates a 3D graphical representation from a 2D map using raycasting algorithms for immersive first-person view.

**Texture Mapping:** Applies textures to walls to enhance visual realism.

**Map Parsing:** Parses .cub map files which define the layout, wall textures, floor and ceiling colors.

**Player Movement:** Supports smooth player movement with collision detection to avoid walking through walls.

**Event Handling:** Handles keyboard inputs for moving and rotating the player, and window close events.

**Double Buffering:** Uses a double-buffer technique to render smooth frames without flickering.

## Bonus

**MiniMap:** Displays a minimap showing player position and orientation. 

**Minimap Zoom:** Controlled by the mouse wheel﻿, allows smooth zooming in and out to get a better view of the map.

**Mouse Camera Rotation:** Intuitive and fluid first-person perspective control by mouse movement.

## Getting Started

**Prerequisites**

• C compiler (gcc or clang)

• Make

• MiniLibX graphics library (included when git clone)

**Installation**

Clone the repository:

```git clone <your-repository-url>```
```cd cub3d```

Build the project:

```make```

Or to recompile everything:

```make re```

Running the game

```./cub3d maps/example.cub```

Example .cub map file format

```NO ./textures/wall_north.xpm```

```SO ./textures/wall_south.xpm```
```WE ./textures/wall_west.xpm```
```EA ./textures/wall_east.xpm```
```F 220,100,0```
```C 100,100,255```

```111111```
```100001```
```1000N1```
```111111```

**Controls**

**W / Z:** Move forward

**S:** Move backward

**A / Q:** Strafe left

**D:** Strafe right

**Left/Right Arrow:** Rotate view

**ESC:** Exit game

**Mouse:** Rotate camera view smoothly

**M:** Enable/disable camera rotation with mouse movement

**Mouse Wheel:** Zoom in and out into the minimap

**Project Structure**

```cub3d/```
```├── extern_files/    # Extern library (mlx and libft)```
```├── includes/        # Header files```
```├── srcs/            # Source files (parsing, raycasting, rendering, events)```
```├── textures/        # Texture assets```
```├── maps/            # Map files (.cub) and tester```
```├── Makefile```
```├── main.c```
```├── en.subject.pdf   # Project subject```
```└── README.md```

**Map Testing Script**

To facilitate testing multiple map files easily, a shell script is provided:

```./maps/test_maps/mapTester.sh ./maps/map_to_test.cub```

• This script runs your cub3d executable on multiple maps automatically.

• It helps verify your program's handling of different map configurations quickly.

• You just need to pass the path of the map to test as an argument.

• It can test all maps in a directory or specific maps, depending on your setup.

• This tool is useful for catching parsing errors, crashes, or visual bugs in your maps.

Use this script regularly during development to ensure robustness across various map designs.

**Authors**

@sbehar and @ltcherep
