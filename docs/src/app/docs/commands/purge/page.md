---
title: Purge Command
---

The `purge` command removes all Docker containers, images, volumes, and networks from your system. This is a powerful and potentially destructive command, used to completely reset Docker.

---

## Usage

To purge all Docker data using Dock:

```bash
dock any_env purge
```

---

## Examples

### Purging All Docker Data
```bash
dock dev purge
```

This command will:
1. Prompt for confirmation to ensure intentional use.
2. Remove all Docker containers, images, volumes, and networks.

---

## Behind the Scenes

The `purge` command internally maps to a series of Docker commands that reset your system:

```bash
docker system prune --all --volumes --force
```

Dock automates this, making it easier to reset Docker environments safely and efficiently.

---

## Warning

- **Destructive Action**: This command removes all Docker data on your system, so use it with caution.
- **Confirmation**: Dock will prompt you to confirm before proceeding with the purge.

---

## Tips

- **Before Purging**: Ensure no critical data is stored in Docker volumes. Back up important data if necessary.
- **Monitor Disk Space**: Use `docker system df` to check disk usage before and after purging.
- **For Specific Environments**: If you want to clean up only a specific environment, consider using `rm` or `down` instead.

---

The `purge` command is a last-resort tool for resetting Docker completely. Use it when you need a clean slate for your development or production environment.
