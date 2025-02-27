# Procedural Generation of Prefab Rooms with Random Seed and Objects

## Overview

This project demonstrates the procedural generation of rooms using prefab templates, a random seed, and random object placement within those rooms. The system generates room layouts based on a random seed, ensuring that the same layout is created for the same seed value. Additionally, objects are randomly placed within each room according to predefined rules.

## Features

- **Prefab Rooms**: Predefined room templates are used as building blocks for the environment.
- **Random Seed**: Ensures consistency across procedural generations by using the same seed for the same output.
- **Random Object Placement**: Objects such as furniture, enemies, or loot are randomly placed within each room.

## Requirements

- **Unreal Engine 5** or **Unity** (depending on your preferred engine)
- **Basic knowledge of procedural generation**, **Blueprints** (for Unreal Engine), or **C#** (for Unity)
- **Random number generation** to handle the seed and object placement.

## Installation

### Unreal Engine 5

1. **Create a New Project**:
   - Open **Unreal Engine 5**.
   - Create a **Blank** project with **Blueprints** enabled.
   - Make sure **Starter Content** is included.
   - Name your project (e.g., `ProceduralRooms`).

2. **Prefab Rooms**:
   - Design a set of **Prefab Rooms** in the editor. These can be simple meshes like a square room or a more complex dungeon layout.
   - Save each room as a **Blueprint** or **Static Mesh**.

3. **Random Seed System**:
   - Create a **Random Seed Manager** to manage and store random seed values.
   - Use this seed for generating random layouts and placing objects consistently.

4. **Random Object Placement**:
   - Create random object templates (e.g., furniture, enemies).
   - Use the **Random Seed** to determine the placement of objects in each room.

### Unity

1. **Create a New Project**:
   - Open **Unity** and create a new 3D project.
   - Ensure you have any necessary assets imported (room prefabs, object templates, etc.).

2. **Prefab Rooms**:
   - Create room prefabs (e.g., square rooms, corridors, and special rooms).
   - Save the prefabs in the **Assets** folder.

3. **Random Seed System**:
   - Create a `RandomSeedManager` script that generates and stores the seed for procedural generation.
   - Use the seed with `Random.Range()` to generate random values consistently.

4. **Random Object Placement**:
   - Write a system that randomly places objects (e.g., furniture, loot, enemies) in the rooms.
   - Randomly instantiate objects based on the seed, ensuring repeatable results with the same seed.

## Usage

1. **Set a Random Seed**:
   - You can set a custom seed or let the system generate one automatically. Using the same seed will regenerate the same level layout and object placement every time.
   
   Example in **Unreal Engine**:
   ```blueprint
   Seed = FMath::RandRange(0, 10000);
