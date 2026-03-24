# MiniLibX 2D Engine

A 2D tile-based game engine and adventure game built in C using MiniLibX, featuring sprite animations, collectibles, enemy AI, and map parsing from custom `.ber` scene files.

## Features

- **Tile map system**: configurable maps via `.ber` ASCII files
- **Animated sprites**: frame cycling using delta time
- **Player movement**: W/A/S/D with wall collision detection
- **Collectibles**: counter displayed in HUD
- **Enemy pathfinding**: basic line-of-sight patrol AI
- **Move counter**: rendered on screen via pixel font

## Map Format (`.ber`)

```
1111111111111
10010000000C1
1000011111001
1P001E100001 1
1111111111111
```

| Symbol | Meaning |
|--------|---------|
| `1` | Wall |
| `0` | Floor |
| `P` | Player start |
| `E` | Exit |
| `C` | Collectible |

Rules: rectangular map, surrounded by walls, exactly one `P` and one `E`, at least one `C`, valid path must exist.

## Build & Run

```bash
make
./so_long maps/level1.ber
```

## Controls

| Key | Action |
|-----|--------|
| `W/A/S/D` | Move |
| `ESC` | Quit |

## Tech Stack

`C` `MiniLibX` `XPM Sprites` `2D Rendering` `Map Parsing` `Game Loop`

