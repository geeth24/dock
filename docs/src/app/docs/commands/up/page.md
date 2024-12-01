---
title: Up Command
---

The `up` command is used to start a Docker Compose environment in detached mode. This is one of the most commonly used commands in **Dock**.

---

## Usage

To start an environment using Dock:

```bash
dock <environment> u
```

---

## Examples

### Starting the Development Environment
```bash
dock dev u
```

This command will:
1. Bring up the containers specified in `docker-compose-dev.yml`.
2. Run the containers in detached mode.

### Starting the Production Environment
```bash
dock prod u
```

This command will:
1. Use `docker-compose-prod.yml`.
2. Ensure all services are started and running in detached mode.

---

## Behind the Scenes

The `up` command internally maps to the following Docker Compose command:

```bash
docker-compose -f <compose-file> up -d
```

Dock simplifies the process by automatically selecting the correct `docker-compose` file based on the `.dock` configuration.

---

## Tips

- **Check Logs After Start**: Use the `logs` command to follow logs after starting the environment:
  ```bash
  dock dev logs
  ```
- **Combine with Build**: If you want to rebuild services before starting, use the `b` command instead:
  ```bash
  dock dev b
  ```

---

The `up` command is an essential part of your Docker Compose workflow. Combine it with other commands like `logs` and `status` for seamless environment management.
