---
title: Deployment
has_children: false
nav_order: 8
---

# Deployment

## User installation
To successfully run the software, the end-user is required to have a Python runtime environment established on their local machine.

Specifically, the system requires Python version 3.10 or higher, alongside the standard pip package manager. All supplementary framework requirements, such as Pygame, are encapsulated and managed directly through the project's dependencies.

The installation procedure is executed via the command-line interface within the project's root directory. The user must install the required libraries using the following command:

```bash
pip install -r requirements.txt
```

To maintain system integrity and prevent package version conflicts with the global operating system, establishing an isolated virtual environment prior to dependency installation is strongly recommended. This is achieved via the following sequence:

```bash
python -m venv venv
.\venv\Scripts\Activate
```

Regarding system configuration, the application is entirely self-contained. It requires no manual initialization of environment variables, external configuration files or system registry modifications. Following the installation of dependencies, the software is launched directly via the primary execution script:

```bash
python -m artifact.source.main
```

## Server-side installation

The software does not need any server-side deployment, remote infrastructure or network configuration.

The application is architected exclusively as a standalone, client-side desktop program. All core system processes (game state evaluation, asset rendering, spatial physics calculations and user input processing) are computed locally within the user's hardware memory space.

There is also no requirement for external databases, web hosting environments, message brokers or remote data pipelines. No additional server-side software is needed.