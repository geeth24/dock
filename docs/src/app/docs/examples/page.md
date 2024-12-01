---
title: Usage Examples
---

Get a hands-on understanding of **Dock** with these practical usage examples. These examples demonstrate how Dock simplifies Docker Compose workflows.

---

## Starting an Environment

To start a development environment:

```bash
dock dev u
```

This command:
1. Uses `docker-compose-dev.yml`.
2. Brings up the containers in detached mode.

---

## Stopping an Environment

To stop a production environment:

```bash
dock prod d
```

This command:
1. Stops all services defined in `docker-compose-prod.yml`.
2. Removes associated networks and resources.

---

## Building and Starting an Environment

To rebuild and start a test environment:

```bash
dock test b
```

This command:
1. Builds the services in `docker-compose-test.yml`.
2. Starts the environment in detached mode.

---

## Restarting Services

To restart services in a development environment:

```bash
dock dev r
```

This command:
1. Stops and then restarts all services in `docker-compose-dev.yml`.

---

## Viewing Logs

To follow logs in real time for a specific environment:

```bash
dock dev logs
```

---

## Checking Status

To check the status of services in an environment:

```bash
dock dev status
```

This command displays the state of all containers, including their ports and health.

---

## Removing Stopped Containers

To clean up stopped containers in an environment:

```bash
dock dev rm
```

---

## Stopping All Containers

To stop all running containers across all environments:

```bash
dock any_env stop_all
```

---

## Purging Docker Data

To remove all Docker containers, images, volumes, and networks:

```bash
dock any_env purge
```

---

These examples illustrate the simplicity and power of Dock, making Docker Compose workflows efficient and easy to manage.
