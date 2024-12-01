---
title: Stop All Command
---

The `stop_all` command stops all running Docker containers across all environments, regardless of their associated `docker-compose` files. This is a powerful command for halting all Docker activity on your system.

---

## Usage

To stop all running containers using Dock:

```bash
dock any_env stop_all
```

---

## Examples

### Stopping All Containers
```bash
dock dev stop_all
```

This command will:
1. Identify all running Docker containers, regardless of the environment.
2. Stop all of them safely.

---

## Behind the Scenes

The `stop_all` command internally maps to the following Docker command:

```bash
docker stop $(docker ps -q)
```

Dock simplifies this process, ensuring all containers are stopped without needing manual intervention.

---

## Tips

- **Before Cleanup**: Use `stop_all` before running cleanup commands like `purge` to ensure no containers are actively running.
- **System-Wide Impact**: This command affects all running containers, so use it with caution in multi-project setups.
- **Verify Results**: After running `stop_all`, check with:
  ```bash
  docker ps
  ```

---

The `stop_all` command is a quick way to halt all Docker activity on your system, making it an essential tool for resetting your environment.
