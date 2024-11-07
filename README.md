# Dock

**Dock** is a custom CLI tool designed to simplify the management of Docker Compose environments. With Dock, you can start, stop, build, and monitor your Docker services using a single configuration file and straightforward commands.

## Features

- Quick and easy setup for Docker Compose environments.
- Simplified commands to start, stop, restart, and manage logs.
- `purge` command to remove all Docker data (containers, images, volumes, networks) with a confirmation prompt.

## Prerequisites

- **Python** 3.6+ (Dock uses Python to manage dependencies)
- **Docker** and **Docker Compose**
- **Homebrew** (for easy installation)

## Installation with Homebrew

To install Dock via Homebrew, first tap the repository and then install Dock:

```bash
brew tap yourusername/dock
brew install dock
```

Once installed, you can use Dock by running `dock` followed by the environment and action.
