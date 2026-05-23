---
title: Release
has_children: false
nav_order: 7
---

# Release

**Release Artifacts**

A single primary artifact is produced for this project: a compressed source distribution (ZIP).

**Contents:** The package includes the core Python source code, the visuals/ asset directory, the requirements.txt dependency list, and the README.md instruction manual.

**Repository:** The project is released via GitHub. This platform was chosen for its accessibility, integrated version control, and ability to host "Releases" (tags) that allow users to download specific, stable versions of the game as ZIP files.

## Choice of License
The **Apache License 2.0** was selected as the uniform open-source licensing model for both the project's codebase and its bundled release artifacts. 

Applying a single license across all software logic and media assets prevents compliance conflicts and ensures simplicity for external users. This permissive framework allows developers to freely run, modify, and distribute the source code or individual game modules for both educational and commercial applications. 

Additionally, the Apache License 2.0 provides robust legal protections, including an explicit grant of patent rights to safeguard the project against potential litigation and clear liability limitations establishing that the software is provided strictly on an "as-is" basis to protect the author from future warranty claims.

## Versioning schema
**Semantic Versioning (SemVer)** was adopted for this project. This schema is industry standard and provides clear expectations to users regarding the nature of updates.

**Schema Logic:** Versioning follows the MAJOR.MINOR.PATCH format:
- **Major** (e.g., 1.0.0): Incremented when incompatible changes are made (e.g., a total rewrite of the game engine).
- **Minor** (e.g., 0.1.0): Incremented when new features are added (e.g., adding a new obstacle type like the Bee).
- **Patch** (e.g., 0.0.1): Incremented when bugs are fixed (e.g., resolving a collision hitbox error).

**Alignment:** Since the project consists of one unified game artifact, version numbers are aligned globally.
