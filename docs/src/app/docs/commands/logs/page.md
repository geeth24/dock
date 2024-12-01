---
title: Logs Command
---

The `logs` command allows you to view and follow real-time logs for a specific Docker Compose environment. This is essential for debugging and monitoring your services.

---

## Usage

To view logs for an environment using Dock:

```bash
dock <environment> logs
```

---

## Examples

### Viewing Logs for the Development Environment
```bash
dock dev logs
```

This command will:
1. Fetch logs from all services defined in `docker-compose-dev.yml`.
2. Stream logs in real time.

### Viewing Logs for the Production Environment
```bash
dock prod logs
```

This command will:
1. Fetch logs from services in `docker-compose-prod.yml`.
2. Allow you to monitor production services interactively.

---

## Behind the Scenes

The `logs` command internally maps to the following Docker Compose command:

```bash
docker-compose -f <compose-file> logs -f
```

Dock makes it easy to run this command for any configured environment by automatically selecting the appropriate `docker-compose` file.

---

## Tips

- **Filter Specific Services**: To view logs for a specific service, use the native Docker Compose syntax:
  ```bash
  docker-compose -f <compose-file> logs <service-name>
  ```
- **Debugging**: Use the `logs` command in conjunction with `restart` or `up` to identify and resolve issues.
- **Exit Logs Stream**: Press `Ctrl+C` to stop following the logs.

---

The `logs` command is an invaluable tool for monitoring your Docker Compose services in real-time, ensuring you can diagnose and resolve issues quickly.
