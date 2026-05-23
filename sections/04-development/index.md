---
title: Development
has_children: false
nav_order: 5
---

# Development

## Distributed Version Control System (DVCS)

The project utilized Git for version control. Given that this is an individual software engineering project, the workflow was kept streamlined to focus on rapid iteration.

**Branching Strategy: *Linear workflow with Single Main Branch***

The project followed a simplified linear branching model. All development was conducted directly on the main branch. This approach was chosen to minimize the overhead of merging and to maintain a continuous, chronological history of the game's evolution.


**Commit Messages:**

Commits were used as save points after implementing core logic or fixing bugs.

Messages were written to clearly describe what was changed in each step. This ensured that if a new change broke the game, the project could easily be reverted to a previous working state.

**Local Development:**

Since there was only one developer, Pull Requests and formal code reviews were not necessary. Instead, validation was performed through manual testing before each commit was finalized.


## Implementation details
This section explains the technical choices made during the coding phase.

**Network Protocols:** As a local 2D game, the system does not require network communication. Using protocols like TCP/UDP would introduce unnecessary latency for a reflex-based game.

**In-Transit Data:** All data (scores, positions) are stored in the local machine's RAM. No data is serialized into JSON or XML for transit, as there is no external communication.

**Asset Management:** Images are loaded from the disk using the os module to ensure cross-platform path compatibility.

**State Reset Logic:** The implementation uses a recursive call where *menu()* calls *main()*. This ensures that every time a new game starts, the points and game_speed variables are reloaded to their original values.


## Technological details
This project was built using a modern Python stack designed for 2D multimedia applications.

**Programming Language:** Python
- Python was chosen for its rapid development speed and high readability. It allows for complex logic (like gravity physics) to be written in using simple code.

**Primary Framework:** Pygame
- Pygame is a robust library, that provides the essential tools for game development:
    - Drawing images onto the screen
    - Monitoring keyboard inputs
    - Using *pygame.Rect* class to handle hitboxes and collision detection.

**Standard Libraries:**
- **random:** It determines which obstacle *(Plant, Gorge, Bee)* or decorative object *(Tree)* spawns next and how often do they appear.
- **os:** Used for directory navigation to ensure the game can find the visuals folder on any computer.

**External Dependencies:** None
- The game is fully self-contained, meaning it does not rely on external APIs, databases, or cloud services, ensuring 100% offline playability.

## Development Tools
- **VS Code** was used for writing and debugging the Python scripts.
- **Graphics:** Pixel-art assets were used to maintain a consistent visual style and low memory footprint.
    - Cat visuals were drawn using **piskelapp**
    - Ostacles visuals were generated using **ChatGPT**