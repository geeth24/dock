---
title: Status Command
---

The `status` command provides an overview of the running state of services in a Docker Compose environment. It’s a quick way to check the health and activity of your containers.

---

## Usage

To view the status of an environment using Dock:

```bash
dock <environment> status
```

---

## Examples

### Checking the Status of the Development Environment
```bash
dock dev status
```

This command will:
1. Display the state of all containers defined in `docker-compose-dev.yml`.
2. Indicate whether each service is running, stopped, or exited.

### Checking the Status of the Production Environment
```bash
dock prod status
```

This command will:
1. Use `docker-compose-prod.yml`.
2. Show the health and activity of all services in the production environment.

---

## Behind the Scenes

The `status` command internally maps to the following Docker Compose command:

```bash
docker-compose -f <compose-file> ps
```

Dock simplifies this by automatically selecting the appropriate `docker-compose` file based on your configuration.

---

## Output Example

After running `dock dev status`, you might see output like this:

```
 Name               Command               State         Ports       
-------------------------------------------------------------------
 app       docker-entrypoint.sh npm ...   Up      0.0.0.0:3000->3000/tcp
 db        docker-entrypoint.sh mysqld    Up      3306/tcp
 redis     docker-entrypoint.sh redis ... Up      6379/tcp
```

---

## Tips

- **Monitor Services**: Use `status` regularly to ensure all services are running as expected.
- **Debugging Stopped Containers**: If a service isn’t running, use `logs` to investigate:
  ```bash
  dock dev logs
  ```
- **Combine with Other Commands**: Use `status` after `up` or `restart` to confirm that all services are operational.

---

The `status` command provides an at-a-glance view of your Docker Compose services, making it an essential tool for environment management.
