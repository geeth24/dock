# Dock

**Dock** is a custom CLI tool designed to streamline the management of Docker Compose environments. With Dock, you can easily start, stop, build, and monitor your Docker Compose services using a single configuration file and straightforward commands.

---

## Table of Contents
- [Features](#features)
- [Installation](#installation)
  - [Using Homebrew](#using-homebrew)
  - [Manual Installation](#manual-installation)
- [Configuration](#configuration)
- [Commands](#commands)
  - [Up (`u`)](#up-u)
  - [Down (`d`)](#down-d)
  - [Build and Start (`b`)](#build-and-start-b)
  - [Restart (`r`)](#restart-r)
  - [Logs (`logs`)](#logs-logs)
  - [Status (`status`)](#status-status)
  - [Remove (`rm`)](#remove-rm)
  - [Stop All Containers (`stop_all`)](#stop-all-containers-stop_all)
  - [Purge (`purge`)](#purge-purge)
  - [Options](#options)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

---

## Features

- Simplifies Docker Compose workflows for multiple environments.
- Configurable through a `.dock` YAML file for custom environments.
- Supports commands to start, stop, build, restart, monitor, and clean Docker containers and services.
- Purge all Docker data in a single command (with confirmation).
- Supports building images without using cache (`--no-cache` or `-nc`).
- Installable via Homebrew or manual setup.

---

## Installation

### Using Homebrew

You can install Dock using Homebrew:

1. Add the Dock tap:
   ```bash
   brew tap geeth24/dock
   ```

2. Install Dock:
   ```bash
   brew install dock
   ```

After installation, you should be able to run `dock` commands from the terminal.

### Manual Installation

Alternatively, you can download and set up Dock manually:

1. Clone the repository:
   ```bash
   git clone https://github.com/geeth24/dock.git
   cd dock
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Make the script executable:
   ```bash
   chmod +x dock
   ```

4. Move the script to a directory in your PATH (e.g., `/usr/local/bin/`):
   ```bash
   sudo mv dock /usr/local/bin/
   ```

Now you can use `dock` from anywhere in your terminal.

---

## Configuration

To configure Dock for different environments, create a `.dock` file in your project root. This file should define each environment with its corresponding `docker-compose` file.

Example `.dock` file:

```yaml
dev: docker-compose-dev.yml
prod: docker-compose-prod.yml
test: docker-compose-test.yml
```

This allows you to use `dock <environment> <command>` for different Docker Compose setups.

---

## Commands

Dock uses short aliases for common Docker Compose commands. Here’s a complete list of commands:

### Up (`u`)

Start the specified environment in detached mode.

```bash
dock <env> u
```

Example:
```bash
dock dev u  # Starts the 'dev' environment in detached mode
```

### Down (`d`)

Stop the specified environment.

```bash
dock <env> d
```

Example:
```bash
dock dev d  # Stops the 'dev' environment
```

### Build and Start (`b`)

Build and start the specified environment.

```bash
dock <env> b [options]
```

Example:
```bash
dock dev b  # Builds and starts the 'dev' environment
```

### Restart (`r`)

Restart the services in the specified environment.

```bash
dock <env> r
```

Example:
```bash
dock dev r  # Restarts the 'dev' environment services
```

### Logs (`logs`)

Follow logs for the specified environment.

```bash
dock <env> logs
```

Example:
```bash
dock dev logs  # Follows logs for the 'dev' environment
```

### Status (`status`)

Display the status of services in the specified environment.

```bash
dock <env> status
```

Example:
```bash
dock dev status  # Shows status of the 'dev' environment services
```

### Remove (`rm`)

Remove stopped containers in the specified environment.

```bash
dock <env> rm
```

Example:
```bash
dock dev rm  # Removes stopped containers in the 'dev' environment
```

### Stop All Containers (`stop_all`)

Stops all currently running Docker containers across all environments.

```bash
dock any_env stop_all
```

Example:
```bash
dock dev stop_all  # Stops all Docker containers
```

### Purge (`purge`)

**Warning**: The `purge` command will delete all Docker containers, images, volumes, and networks.

```bash
dock any_env purge
```

Example:
```bash
dock dev purge  # Prompts for confirmation before purging all Docker data
```

**Note**: This command prompts for confirmation before proceeding.

---

## Options

Dock commands can include the following option:

### `--no-cache` or `-nc`

Use this flag with the `b` (build) command to ensure Docker builds images without using cached layers.

Example:
```bash
dock dev b --no-cache  # Builds 'dev' environment without cache
dock dev b -nc         # Alias for the same functionality
```

---

## Examples

Here are some example usages of Dock commands:

- **Start the Development Environment**:
  ```bash
  dock dev u
  ```

- **Stop the Production Environment**:
  ```bash
  dock prod d
  ```

- **Build and Start the Test Environment Without Cache**:
  ```bash
  dock test b --no-cache
  ```

- **Follow Logs in the Development Environment**:
  ```bash
  dock dev logs
  ```

- **Purge All Docker Data**:
  ```bash
  dock any_env purge
  ```

---

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Make your changes and commit (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.

---