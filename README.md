# MEOW RUNNER - Project Report

Meow Runner is a cat-themed remake of the classic Chrome offline dinosaur game, developed as the final project for the Software Engineering course at UNIBO.

## Project Overview
Meow Runner is an arcade-style game built entirely in Python using the Pygame framework. The player controls a cat avatar that must jump over low obstacles (*plants, gorges*) and duck under flying obstacles (*bees*). The system includes dynamic difficulty scaling that ramps up the game speed in real-time based on the player's performance.

## Tech Stack & Architecture
- **Language:** Python 3.11+
- **Core Library:** Pygame (for real-time 2D rendering, inputs, and spatial physics)
- **Testing Framework:** Unittest
- **Architecture:** Modular Object-Oriented Design separating player state logic, obstacle factories and background environmental rendering.

## Validation Summary
The system has been thoroughly validated using a dual-testing approach detailed in the report:
1. **Automated Testing:** 23 logical test cases executed via *unittest*, achieving 92% overall code coverage across the codebase.
2. **Manual Acceptance Testing:** Verified through an integrated visual DEBUG_MODE that displays live collision boundaries (*pygame.Rect*) to confirm pixel-accurate hitboxes during active gameplay.
