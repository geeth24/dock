---
title: Configuration
---

Set up **Dock** to manage multiple Docker Compose environments with ease.

---

## The `.dock` File

Dock uses a simple YAML-based configuration file named `.dock` to define your environments and their associated Docker Compose files.

### Example `.dock` File

```yaml
dev: docker-compose-dev.yml
prod: docker-compose-prod.yml
test: docker-compose-test.yml
```

### How It Works

- Each key (e.g., `dev`, `prod`, `test`) represents an environment.
- The value is the path to the corresponding Docker Compose file.
- Place the `.dock` file in the root directory of your project.

---

## Creating a `.dock` File

Follow these steps to create and configure your `.dock` file:

### Step 1: Navigate to Your Project Directory
```bash
cd /path/to/your/project
```

### Step 2: Create the `.dock` File
```bash
touch .dock
```

### Step 3: Add Your Environments
Edit the `.dock` file and specify the environments:

```yaml
dev: docker-compose-dev.yml
prod: docker-compose-prod.yml
test: docker-compose-test.yml
```

---

## Using the `.dock` File

Once configured, Dock allows you to switch between environments effortlessly.

### Starting an Environment
```bash
dock dev up
```

### Stopping an Environment
```bash
dock prod down
```

### Viewing Logs
```bash
dock test logs
```

---

## Tips for Configuration

- **Relative Paths**: Use relative paths to keep your `.dock` file portable.
- **Custom Compose Files**: Ensure your Docker Compose files include the required configurations for each environment.
- **Version Control**: Add the `.dock` file to your version control system for team collaboration.

---

Dock’s configuration is simple yet powerful, enabling seamless environment management. Check out the [Commands](docs/commands/up) section for more usage details.
