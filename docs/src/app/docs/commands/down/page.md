---
title: Down Command
---

The `down` command stops a Docker Compose environment and removes containers, networks, and other resources created by the `up` command.

---

## Usage

To stop an environment using Dock:

```bash
dock <environment> d
```

---

## Examples

### Stopping the Development Environment
```bash
dock dev d
```

This command will:
1. Stop all running containers defined in `docker-compose-dev.yml`.
2. Clean up associated networks and resources.

### Stopping the Production Environment
```bash
dock prod d
```

This command will:
1. Use `docker-compose-prod.yml`.
2. Tear down all resources associated with the environment.

---

## Behind the Scenes

The `down` command internally maps to the following Docker Compose command:

```bash
docker-compose -f <compose-file> down
```

Dock handles selecting the appropriate `docker-compose` file automatically based on the `.dock` configuration.

---

## Tips

- **Preserve Volumes**: By default, the `down` command removes associated volumes. If you want to retain volumes, use the `--volumes` flag with the native `docker-compose` command.
- **Stop Specific Containers**: Use the `rm` command to remove specific stopped containers without bringing down the entire environment:
  ```bash
  dock dev rm
  ```

---

The `down` command is essential for stopping and cleaning up your Docker Compose environments effectively. Combine it with commands like `up` and `logs` for a complete workflow.
