---
title: Future work
has_children: false
nav_order: 13
---

# Known issues and future work

This section assesses the current limitations of the application, identifying existing software constraints alongside planned feature enhancements to expand the game in future development cycles.

## Known Issues and Missing Features

While the core software loops function reliably, several elements are not working exactly as intended or remain incomplete due to the constraints of a solo development timeline:

- **Floating Tree Spawning Bug:** A known logical issue exists in the environmental generation system where decorative trees occasionally spawn at the exact same horizontal coordinate as a gorge obstacle. Because a gorge removes the ground texture layer, the decorative tree appears to be floating in mid-air. Attempts to resolve this by adding coordinate checks have not yet succeeded.

- **Jittery Ducking Animation Transition:** The visual transition when the cat sprite shifts from a running state to a ducking position is not as smooth as it should be. The bounding box changes size correctly for collision math, but the sprite frames themselves look slightly off and jump abruptly between frames instead of blending smoothly.

- **Missing Audio Layer:** The software currently lacks any auditory feedback. There are no background music tracks or real-time sound effects initialized when the player jumps, ducks, or encounters a collision event.

- **Lack of Persistence:** The application lacks local file storage or database integration. Consequently, player high scores cannot be saved across separate execution sessions.

## Future Developments
Future work will focus on fixing already mentioned bugs as well as improvement of the user experience and adition of structural depth to the application. Future development will also focus on the following expansions:

- **Audio Integration:** Implement a dedicated audio module using Pygame's mixer library to introduce background music and responsive sound effects for specific player actions and collision events.

- **Expanded Obstacle Variety:** Introduce a wider array of hazards with diverse behavioral patterns, movement speeds, and unique bounding boxes to make the gameplay loop more challenging and less predictable over time.

- **Character Backstory and Deepened Menu System:** Re-engineer the main menu interface to integrate a narrative prologue or backstory explaining the cat character's journey. This will give the game a clear thematic context, providing players with a stronger sense of purpose and immersion from the moment the application launches.