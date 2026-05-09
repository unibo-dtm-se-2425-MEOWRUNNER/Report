---
title: Concept
has_children: false
nav_order: 2
---

# Concept

### Product Description
Meow Runner is a 2D infinite-runner desktop application inspired by the classic "Chrome Dino" game. Developed using the Pygame framework, the project features a cat-themed aesthetic using pixel-art assets.

The application is built on a real-time game loop that manages physics, animations and collision detection. The gameplay loop consists of a player-controlled cat navigating a continiously generated environment. To succeed, the player must use two primary movement mechanics, jumping and ducking, to avoid a variety of ground-based and air-based obstacles.

### Use case collection
**Target Audience:** Casual gamers, children, and users seeking quick, high-engagement entertainment.

**Usage Pattern:** The system is designed for single-session, high-frequency interaction. Because the game scales in difficulty, users typically engage in short "runs" (1–5 minutes) with the goal of beating their previous session's score.

**Interaction Model:** Users interact via standard keyboard inputs (arrows up and down).

**Data Persistence:** The system operates as a stateless application. Scores are tracked during the active session but are not stored into a database or local file after the application is closed.

### System Roles and Interaction
The system defines two primary roles:

**1. Player**
- **Controls:** Uses the UP arrow (jumping) and DOWN arrow (ducking) to manipulate the cat character.
- **Navigation:** Interacts with the Main Menu and Game Over screens using any key to transition between game states.

**2. Game Engine**
- **State Management:** Orchestrates the transition between Main Menu, Active Play and Game Over.
- **Obstacle Spawner:** Randomly selects and deploys entities (plant, gorge, bee) and manages decorative elements (tree) to create a sense of movement.
- **Difficulty Increase:** Automatically increases game speed every 100 points to ensure a progressive challenge.

### Interface and Environment

**GUI Components:**
- **Main Menu:** Displays the "Start" state and wait-for-input logic.
- **Score Display:** A real-time display of the current session score in the upper-right corner.
- **Game Over Screen:** A terminal state triggered by collision, displaying the final score and a prompt to restart.

**Deployment:** 
- The system runs on desktop computers or laptops. It is developed to be playable on most modern operating systems that support Python. 