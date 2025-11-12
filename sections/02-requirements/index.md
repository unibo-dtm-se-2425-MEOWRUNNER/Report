---
title: Requirements
has_children: false
nav_order: 3
---

# Requirements

## User stories

As a player: 
- I want the cat to run automatically, so that I can focus on jumping. 
- I want the cat to jump when I press the spacebar, so I can avoid puddles, rocks.
- I want to see my score and see it increase over time, so it motivates me to play again and again to reach better score.
- I want the game to get harder and faster the longer I play, so it feels more challenging.
- I want the game to end when I hit an obstacle, so I know I lost.
- I want simple pixel art graphics as well as fun and easy interface, so the game experience is good. 

---
- Write down [user stories](https://www.atlassian.com/agile/project-management/user-stories) to devise the main __personas__ (user roles) and the activities they will perform via the system to be developed.

## Requirements analysis

- The requirements must explain **what** (not how) the software being produced should do.
    - You should not focus on the particular problems, but exclusively on what you want the application to do.
- Requirements must be clearly identified, and possibly numbered.
- Requirements are divided into:
    - **Functional**: some functionality the software should provide to the user.
    - **Non-functional**: requirements that do not directly concern behavioral aspects, such as consistency, availability, security, efficiency, etc.
    - **Implementation**: constrain the entire phase of system realization, for instance by requiring the use of a specific programming language and/or a specific software dependency.
        - These constraints should be adequately justified by political / economic / administrative reasons (which must be written down)...
        - ...otherwise, implementation choices should emerge *as a consequence of* design (and therefore described in the design section).
- If there are domain-specific terms, these should be explained in a **glossary**.
- Each requirement must have its own **acceptance criteria**.
    - These will be important for the validation phase. 

> You may consider adding a use-case diagram here (via PlantUML) to better visualize the requirements and their relationships