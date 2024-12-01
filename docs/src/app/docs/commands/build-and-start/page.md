---
title: Build and Start Command
---

The `build and start` command combines building the Docker Compose services and starting the environment in detached mode. This command ensures that all services are built before being brought up.

---

## Usage

To build and start an environment using Dock:

```bash
dock <environment> b
```

---

## Examples

### Building and Starting the Development Environment
```bash
dock dev b
```

This command will:
1. Build all services defined in `docker-compose-dev.yml`.
2. Start the environment in detached mode.

### Building and Starting the Production Environment
```bash
dock prod b
```

This command will:
1. Build services using `docker-compose-prod.yml`.
2. Ensure all services are running.

---

## Behind the Scenes

The `b` command internally maps to the following Docker Compose commands:

```bash
docker-compose -f <compose-file> build
docker-compose -f <compose-file> up -d
```

Dock automates this process, selecting the appropriate compose file based on your `.dock` configuration.

---

## Tips

- **Use for Updates**: If you’ve made changes to your Dockerfiles or dependencies, use the `b` command to rebuild and restart your services.
- **Combine with Logs**: After starting the environment, use the `logs` command to monitor the services:
  ```bash
  dock dev logs
  ```

---

The `build and start` command is a powerful way to ensure your services are updated and running efficiently. It’s ideal for deploying environments where changes have been made.
