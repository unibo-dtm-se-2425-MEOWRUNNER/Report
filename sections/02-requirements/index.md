---
title: Requirements
has_children: false
nav_order: 3
---

# Requirements

### User stories

As a player: 
- I want the cat to run and animate automatically so the game feels dynamic. 
- I want the cat to run automatically, so that I can focus on jumping. 
- I want to jump over ground obstacles (gorges/plants) and duck under airborne obstacles (bees) to stay alive.
- I want the cat to jump when I press the arrow up, so I can avoid gorges and plants.
- I want the cat to duck when I press the arrow down, so I can avoid bees.
- I want to see my score and see it increase over time, so it motivates me to play again and again to reach better score.
- I want the game to get harder and faster the longer I play, so it feels more challenging.
- I want the game to end when I hit an obstacle, so I know I lost.
- I want simple pixel art graphics as well as fun and easy interface, so the game experience is good. 


## Requirements analysis

### Functional requirements
1.	The system allows player to see and control the cat character. 
    - When the game starts, the player sees an animated cat. The system listens for keyboard inputs (UP and DOWN arrows) to trigger actions.
2.	The system allows the cat to jump to avoid ground obstacles. 
    - Pressing the UP arrow causes the cat to move upward and then return to the ground. The cat cannot jump again until it touches the ground.
3.  The system allows the cat to duck to avoid airborne obstacles.
    - Pressing the DOWN arrow changes the cat's visuals to a ducking pose and reduces the height of the collision box by 30 pixels.
4.	The system generates randomized obstacles and background decorations.
    - The system spawns plants, gorges or bees at the right edge of the screen. It also generates trees as background decorations that do not cause collisions.
5.	The system detects collisions between the cat and obstacles.
    - The system constantly checks if the cat’s rectangle overlaps with an active obstacle’s rectangle. If an overlap occurs, the game state changes to "Dead".
6.	The system provides a scoring system that increases over time.
    - A point counter is displayed in the upper-right corner. The score increases by 1 point per frame during active gameplay.
7.	The system increases difficulty as the player progresses.
    - Every time the player reaches a 100-point milestone, the game speed increases by 1, making obstacles move faster toward the cat.
8.  The system displays a Game Over screen and allows for a restart.
    - After collision, the game pauses, displays the "Game Over" graphic and the final score, and allows the player to restart the game by pressing any key.


### Non-Functional requirements
These requirements describe the performance and quality constraints.
- **Performance:** The game must maintain a consistent frame movement to ensure smooth visuals and acurate collision detection.
- **Visual Feedback:** When a collision occurs, the cat's visual must change to the DEAD picture to provide immediate visual feedback of failure.
- **Stability:** The application must handle asset loading via relative paths to ensure it runs on different machines without path errors.

### Implementation requirements 
- **Language & Library:** The project must be implemented in Python 3 using the Pygame library for window management and rendering.
- **Code Structure:** The system must use Object-Oriented Programming (OOP), specifically using inheritance for obstacles to allow for easy addition of new obstacle types in the future.
---

> You may consider adding a use-case diagram here (via PlantUML) to better visualize the requirements and their relationships

