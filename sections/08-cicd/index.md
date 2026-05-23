---
title: CI/CD
has_children: false
nav_order: 9
---

# CI/CD

## Continuous Integration Workflow
The primary element automated in this project is the testing pipeline. Every time new code is pushed to GitHub, or a pull request is created, an automated workflow triggers automatically. This system builds the project from scratch, installs the required packages, and runs all 23 automated tests to verify that the code coverage remains at the required 92 percent baseline.

This automation is necessary because manual testing is time-consuming and prone to human error. In a game with connected components, changing code in one file (like character movement) can easily break another file (like collision detection) without the developer noticing. Automating these checks provides instant feedback, ensuring that no broken code is accidentally merged into the main project.

## Implementation Details and Environment Variables
The pipeline executes by performing three basic steps: cloning the repository code, setting up a clean Python 3.10 environment, and installing the dependencies from the requirements file.

Because this is a standalone desktop game, the pipeline does not require any sensitive data, database access, or encrypted GitHub secrets to run. It operates entirely independently of external networks.