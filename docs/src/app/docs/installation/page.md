---
title: Installation
---

**Dock** can be installed via Homebrew for convenience or manually for more control.

---

## Installing with Homebrew

### Step 1: Add the Dock Tap
```bash
brew tap geeth24/dock
```

### Step 2: Install Dock
```bash
brew install dock
```

### Step 3: Verify Installation
```bash
dock --version
```

Once installed, Dock is ready to use for managing Docker Compose environments.

---

## Manual Installation

### Step 1: Clone the Repository
```bash
git clone https://github.com/geeth24/dock.git
cd dock
```

### Step 2: Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 3: Make the Script Executable
```bash
chmod +x dock
```

### Step 4: Add Dock to PATH
```bash
sudo mv dock /usr/local/bin/
```

### Step 5: Verify Installation
```bash
dock --version
```

Dock is now accessible from any directory in your terminal.

---

## What’s Next?

- Proceed to [Configuration](docs/configuration) to set up your `.dock` file.
- Explore [Commands](docs/commands/up) for managing environments.

Dock simplifies Docker Compose workflows—get started today!
