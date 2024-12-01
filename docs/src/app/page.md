---
title: Getting started
---

Learn how to get **Dock** set up in your project in under thirty minutes. {% .lead %}

{% quick-links %}

{% quick-link title="Installation" icon="installation" href="/docs/installation" description="Step-by-step guides to setting up Dock and installing it via Homebrew or manually." /%}

{% quick-link title="Configuration" icon="presets" href="/docs/configuration" description="Learn how to configure Dock for multiple Docker Compose environments using a `.dock` file." /%}

{% quick-link title="Commands" icon="plugins" href="/docs/commands/up" description="Discover the powerful commands Dock offers to simplify your Docker Compose workflows." /%}

{% quick-link title="Examples" icon="theming" href="/docs/examples" description="Explore real-world examples to see Dock in action and streamline your workflow." /%}

{% /quick-links %}

**Dock** is a custom CLI tool designed to streamline the management of Docker Compose environments. Configure environments, monitor services, and manage containers—all with simple commands.

---

## Quick start

Getting started with Dock is quick and straightforward. Follow these steps to have Dock up and running in minutes.

### Installing Dock

You can install Dock using Homebrew or manually. Check out the [Installation](docs/installation) guide for detailed instructions.

```shell
# Install via Homebrew
brew tap geeth24/dock
brew install dock

# Or clone the repository and set it up manually
git clone https://github.com/geeth24/dock.git
cd dock
pip install -r requirements.txt
chmod +x dock
sudo mv dock /usr/local/bin/
```

Dock is now ready to use! Start managing your Docker Compose environments with ease.

### Configuring Dock

Set up your `.dock` file to define multiple Docker Compose environments.

```yaml
dev: docker-compose-dev.yml
prod: docker-compose-prod.yml
test: docker-compose-test.yml
```

This allows you to switch between environments effortlessly with commands like:

```shell
dock dev up
dock prod down
```

---

## Basic usage

Here's how to start using Dock with minimal setup.

### Your first environment

To spin up a Docker Compose environment:

```shell
dock dev u  # Starts the 'dev' environment
```

### Restarting services

Need to restart services in an environment? It's as simple as:

```shell
dock dev r  # Restarts the 'dev' environment
```

### Monitoring logs

Follow the logs for any environment with:

```shell
dock dev logs
```

For more details on commands, check out the [Commands](docs/commands/up) section.

---

## Getting help

If you encounter issues or need help:

### Submit an issue

Visit the [GitHub repository](https://github.com/geeth24/dock/issues) to report bugs or request features.

### Join the community

Get involved and contribute to Dock's development. Check the [Contributing](docs/contributing) guide for more details.

Need more guidance? Check out the [Examples](docs/examples) section to see Dock in action.
