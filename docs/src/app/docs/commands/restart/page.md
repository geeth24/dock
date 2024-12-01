---
title: Restart Command
---

The `restart` command stops and then restarts the services in a Docker Compose environment. This is useful when you want to refresh your environment without fully tearing it down.

---

## Usage

To restart an environment using Dock:

```bash
dock <environment> r
```

---

## Examples

### Restarting the Development Environment
```bash
dock dev r
```

This command will:
1. Stop all running containers defined in `docker-compose-dev.yml`.
2. Restart the containers in the same environment.

### Restarting the Production Environment
```bash
dock prod r
```

This command will:
1. Use `docker-compose-prod.yml`.
2. Restart all services defined in the file.

---

## Behind the Scenes

The `r` command internally maps to the following Docker Compose commands:

```bash
docker-compose -f <compose-file> stop
docker-compose -f <compose-file> start
```

Dock simplifies this workflow by combining these steps into a single command.

---

## Tips

- **For Configuration Updates**: Use `r` to apply changes to configuration files without rebuilding the images.
- **Combine with Logs**: After restarting, monitor the environment with:
  ```bash
  dock dev logs
  ```

---

The `restart` command is a convenient way to refresh your Docker Compose environment without fully tearing it down or rebuilding.
