---
title: Developer guide
has_children: false
nav_order: 11
---

# Developer Guide
This section provides a simple onboarding guide for anyone looking to understand or contribute to the project codebase. Since the project is currently managed by a solo developer, the workflow avoids complex corporate engineering structures and focuses strictly on clean, direct implementation.

## Organizational Information and Project Tracking

Because there is no external development team to coordinate, all project management happens directly on the primary GitHub repository.

If you find a bug or want to suggest an enhancement, simply open an issue directly in the repository's Issues tab. For direct communication regarding the codebase, you can reach out directly to the repository owner via email or GitHub profile contact info.

## Coding Style and Conventions

The codebase prioritizes readability and absolute simplicity, completely avoiding over-engineering, unnecessary abstractions or dense blocks of comments. Instead, the code relies on clear, self-explanatory naming conventions:

- **Code Versioning:** The project strictly follows Semantic Versioning (Major.Minor.Patch) to track releases, where major changes increment the first digit, new features increment the second and bug fixes increment the third.

- **Naming Formats:** Standard Python naming practices are followed. File names and functions use simple snake_case (e.g., check_collision), class names use PascalCase (e.g., ObstacleFactory), and global configuration constants are written in uppercase (e.g., SCREEN_WIDTH).

## Development Environment and Commands

Setting up the local development environment requires just a few standard commands. If you have already installed Python 3.10 or higher, you can clone the project repository from:

https://github.com/unibo-dtm-se-2425-MEOWRUNNER/MEOWRUNNER.git

It is recommended to use the virtual enviroment that can be setup using:

```bash
python -m venv venv
.\venv\Scripts\Activate
```
To properly set up the enviroment it is necessary to install the dependencies using:

```bash
pip install -r requirements.txt
```

To launch the game locally after setting up, execute the main entry file:
```bash
python main.py
```
To run the automated test suite and ensure that no existing code logic is broken, execute:

```bash
pytest --cov=source tests/
```
## Development Workflow

The workflow is completely straightforward. There are no rigid branching rules or review boards. When developing a new feature or fixing an issue, the standard practice is to create a temporary branch, commit the changes with a short descriptive message and push it to GitHub.