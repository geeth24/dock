---
title: Features
---

**Dock** simplifies Docker Compose workflows with the following features:

- **Multiple Environment Support**: Manage multiple Docker Compose configurations effortlessly with a `.dock` file.
- **Streamlined Commands**: Use intuitive, short commands to start, stop, build, and monitor services.
- **Comprehensive Logs**: Follow logs for any environment with a single command.
- **Full Cleanup Options**: Purge all Docker data (containers, images, networks, and volumes) in one command with confirmation.
- **Custom Configuration**: Define environments and their corresponding Docker Compose files in a YAML-based `.dock` configuration file.
- **Cross-Platform Compatibility**: Works seamlessly on macOS, Linux, and Windows (via WSL).
- **Homebrew Installation**: Install easily via Homebrew or set up manually.

---

## Why Dock?

Docker Compose can be complex when managing multiple environments. Dock simplifies this process by providing:

1. **Unified Configuration**: With a `.dock` file, you can switch between environments without changing commands.
2. **Efficiency**: Perform multiple Docker Compose operations with fewer commands and aliases.
3. **Clean Management**: Keep your environments organized and clean with built-in purge and remove commands.

---

## Key Highlights

### Environment-Based Workflow

Define your environments once in a `.dock` file:

```yaml
dev: docker-compose-dev.yml
prod: docker-compose-prod.yml
test: docker-compose-test.yml
```

Switch environments seamlessly:

```bash
dock dev u  # Starts the dev environment
dock prod d  # Stops the prod environment
```

### Easy Logs Access

Follow real-time logs with:

```bash
dock dev logs
```

### Comprehensive Cleanup

Remove unused containers or purge everything with:

```bash
dock dev rm      # Remove stopped containers
dock any_env purge  # Confirm before purging all Docker data
```

---

With Dock, you can focus more on development and less on managing your Docker Compose configurations.
