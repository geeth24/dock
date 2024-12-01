---
title: Remove Command
---

The `remove` command is used to clean up stopped containers in a Docker Compose environment. It’s a useful way to free up resources without affecting running containers.

---

## Usage

To remove stopped containers in an environment using Dock:

```bash
dock <environment> rm
```

---

## Examples

### Removing Stopped Containers in the Development Environment
```bash
dock dev rm
```

This command will:
1. Identify stopped containers in the `docker-compose-dev.yml` environment.
2. Remove these containers while leaving active services untouched.

### Removing Stopped Containers in the Production Environment
```bash
dock prod rm
```

This command will:
1. Target stopped containers associated with `docker-compose-prod.yml`.
2. Remove them safely.

---

## Behind the Scenes

The `rm` command internally maps to the following Docker Compose command:

```bash
docker-compose -f <compose-file> rm -f
```

Dock automates this process, allowing you to focus on your environments without worrying about command specifics.

---

## Tips

- **Regular Cleanup**: Use `rm` periodically to keep your environment clean and free of unnecessary stopped containers.
- **Data Safety**: Removing stopped containers doesn’t affect volumes or running containers.
- **Debugging Issues**: If you encounter errors, combine `rm` with `logs` to identify potential problems:
  ```bash
  dock dev logs
  ```

---

The `remove` command helps maintain a tidy and efficient environment by cleaning up unused containers. Use it as part of your regular Docker Compose workflow.
