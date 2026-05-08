# 👻 Pacman

A Python implementation of the classic Pacman arcade game, built using the `turtle` graphics library and the `freegames` package. By Gael Leyva and Emma Sofía García.

## Overview

The player controls Pacman through a maze, eating dots to score points while avoiding ghosts. The game ends when a ghost catches Pacman. Each session picks a random board layout and places Pacman at a random starting position, keeping every run fresh.

## Requirements

- Python 3.x
- [`freegames`](https://pypi.org/project/freegames/) library

Install the dependency with:

```bash
pip install freegames
```

## How to Run

```bash
python pacman.py
```

## Controls

| Input | Action |
|---|---|
| `Arrow keys` | Move Pacman |

## Changes from the Original

### 1. Multiple board layouts
Three distinct maze layouts (`board1`, `board2`, `board3`) were designed and added. A random board is selected at the start of each game, so the maze is different every time you play.

### 2. Random Pacman starting position
Instead of a fixed spawn point, Pacman now starts at a randomly chosen valid tile on whichever board was selected. This ensures the starting position is always on a walkable path regardless of the layout.

### 3. Extra ghost
A fifth ghost was added to the original four, increasing the difficulty of the game.

### 4. Faster ghosts
Ghost speed was increased from `5` to `8` units per step, making them more challenging to outrun.

### 5. Smarter ghosts
Ghosts no longer move randomly when they hit a wall. Instead, they calculate the direction toward Pacman and attempt to take the most direct valid path. If the preferred direction is blocked, they choose randomly from the remaining valid directions, preventing them from getting stuck.
