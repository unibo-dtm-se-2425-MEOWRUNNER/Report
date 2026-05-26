---
title: Validation
has_children: false
nav_order: 6
---

# Validation

## Testing approach
The primary testing approach for "Meow Runner" was **manual functional testing** with **visual debugging**.

**Test-Driven Development:** 

TDD was not utilized for this project. Because the application relies heavily on real-time rendering, framerates and spatial physics (hitboxes), writing tests before writing the Pygame rendering logic was not practical.

**Testing Framework:** 

Automated testing was executed using python's native *unittest* standard library framework, while code coverage metrics were monitored and gathered using the *Coverage.py* tool via automated Poe tasks. A visual Debug Mode was also implemented within the main game loop to allow for real-time verification of hitboxes and collision physics during active development. 

## Testing

### Unit testing
Unit testing were used for testing individual functions in isolation to ensure they produce the correct output for a given input. 

These tests were performed to ensure that non-graphical logic was correct before being integrated into the game loop.

**Logical Verification:**

 - The scoring function was tested to confirm that game_speed increments by 1 exactly when the points variable reaches a multiple of 100.
 - The jump velocity formula was verified to ensure the cat returns to the ground level following a jump action.

 **Results:** 
 - A 100% success rate was achieved for these logical units.
- Test coverage results *(gathered via poetry un poe coverage-report)*:

| Module Name | Executable Statements | Missed Lines | Coverage Percentage |
| :--- | :---: | :---: | :---: |
| *artifact\source\__init__.py* | 0 | 0 | 100% |
| *artifact\source\cat.py* | 69 | 8 | 88% |
| *artifact\source\config.py* | 7 | 0 | 100% |
| *artifact\source\obstacles.py* | 48 | 4 | 92% |
| *artifact\source\visuals.py* | 27 | 0 | 100% |
| **TOTAL** | **151** | **12** | **92%** |

### Integration testing
The communication between independent modules was verified through integration checks within the *unittest* tests.

Components tested togheter: 
- **Cat and Obstacles:** Tests like *test_collision_detected* and *test_no_collision_when_separated* made sure that when the cat's hitbox overlaps with a plant or a bee, the game correctly flags it as a hit. 
- **Player State and Movement Logic:** Tests like *test_jump_avoids_collision* and *test_duck_avoids_bee* verified that changing the cat's state (jumping or ducking) successfully moves the hitboxes out of harm's way over time.
- **Memory Cleanup:** The test test_obstacle_move_left ensured that once an obstacle moves completely off the left side of the screen, it is deleted from the active list to keep the game running smoothly.

**Test Doubles:** Instead of forcing the tests to wait for a real person to press keys on a keyboard, fake inputs (called Stubs) were used. Python dictionaries like {pygame.K_UP: True} were passed directly into the code to trick the game into thinking a button was pressed, letting the tests run automatically.

**Results** 

A 100% success rate was achieved across these integration components, contributing directly to the 88% coverage of *cat.py* and 92% coverage of *obstacles.py.*

### System testing

System testing evaluated the entire game loop from start to finish to ensure all the rules worked together perfectly.

Tests inheriting from *unittest.TestCase* like *TestGameDifficulty* and *TestGameMechanics* simulated an entire play session. They forced the game to calculate what happens at extreme milestones (hitting a massive score of 5,000 points) to confirm the speed goes up smoothly, reaches its intended cap and never breaks or goes backward.

*Containers: Isolated containers like Docker were not used.*

**Results** 

The system-level tests passed with a 100% success rate, proving the core math of the game lifecycle is completely stable within the unified environment runner.


## Acceptance tests (manual)
Because the game relies on player reflexes and visual feedback, Manual Acceptance Testing was the most rigorous validation phase. Testing was executed by setting *DEBUG_MODE = True* in *main.py*, which draws visible green (player) and red (obstacle) *pygame.Rect* boundaries to visually verify mathematical collisions.

**Tests Repetition:** 
- In the main.py set *DEBUG_MODE = True* to see the green and red boudaries and launch main.py,
- manually try the keyboard inputs listed in the plan below.

The final manual test cases:

| ID | Action | Expected Result | Result |
| :--- | :--- | :--- | :---: |
| **01** | Open the game and press any key on the main menu. | The menu disappears and the active running game starts smoothly. | **Pass** |
| **02** | Press the UP arrow key while running. | The cat plays its jumping animation, rises in an arc, and falls back to the exact starting floor line. | **Pass** |
| **03** | Press and hold the DOWN arrow key while running. | The cat switches to a ducking sprite, and the green debug hitbox instantly shrinks by 30 pixels. | **Pass** |
| **04** | Run directly into a Plant or a Gorge. | The game freezes instantly, displays the DEAD cat sprite and brings up the GAME OVER state. | **Pass** |
| **05** | Run directly through a background Tree. | The cat passes cleanly in front of the tree without dying, confirming it is just a background decoration. | **Pass** |
| **06** | Keep playing until the score counter hits 100 points. | The game speed visibly jumps up by 1, confirming the difficulty scaling works in real-time. | **Pass** |


**Results**

The final manual playthroughs achieved a 100% pass rate. The game ran without lagging, crashing or getting stuck on any screens.