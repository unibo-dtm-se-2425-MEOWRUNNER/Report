---
title: Home
layout: home
has_children: false
nav_order: 1
---

# MEOW RUNNER

### Author

- [Veronika Angyalová](mailto:veronika.angyalova@studio.unibo.it)

## Abstract
MeowRunner is a simple 2D endless runner game built in Python using the Pygame library. Inspired by the famous Google Chrome dinosaur game, the project is a standalone desktop application where players control a cat running along a track. The goal is to survive as long as possible by jumping over plants and gorges, and ducking under flying bees, while the game speed gets faster and faster over time.

The game layout consists of a scrolling ground surface where active hazards spawn at random intervals to challenge the player's reaction time. To prevent unfair gameplay scenarios, the system distinguishes between active obstacles and purely decorative elements. While the player must actively jump over plants and gorges or duck under airborne bees to avoid a collision, other environmental assets like background trees are entirely decorative. These decorations are managed by a separate rendering layer that does not register physical contact, allowing them to pass behind the player character without affecting the cat's collision state. If a collision does occur with an active hazard, the game immediately transitions to a Game Over state, pausing the main loop and displaying the final score until the player presses any key to reset and instantly start a new run.

The code is designed to be clean and modular, keeping the game logic separate from the visual graphics. This structure ensures that updates to the player's bounding boxes or physics loops do not conflict with asset drawing routines. To make sure the game runs smoothly and stays stable, the project includes 23 automated tests built with pytest. These tests check important features like character movement and collision hitboxes, maintaining a solid 92% code coverage baseline. Running these automated validation scripts helps catch structural errors early, ensuring that the gameplay loops, animation states, and speed progression mechanics remain reliable and bug-free across different development sessions.

## Disclaimer

During the preparation of this work, the author utilized the following AI tools and software applications to assist in development:
- **Gemini** was used to refine the phrasing, improve grammatical consistency and format the technical documentation chapters.
- **Claude** was used to assist with writing and debugging the Python source code, resolving runtime errors and expanding the pytest suite to improve overall test coverage.
- **ChatGPT** was used to generate the initial concept artwork and raw visual assets for the game's obstacles and background decorations.
- **Photoshop** was used to edit, crop, and modify the AI-generated obstacle and decoration assets to make them compatible with the game engine.
- **Piskel App** was used by the author to manually draw and animate the pixel art frames for the main cat character.

After using this tools and service, the author reviewed and edited the content as needed
and takes full responsibility for the content of the final report, source code and game artifact.