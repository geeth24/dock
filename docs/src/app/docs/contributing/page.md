---
title: Contributing to Dock
---

We welcome contributions to **Dock**! Whether it’s fixing bugs, adding features, or improving documentation, your help is appreciated.

---

## How to Contribute

### 1. Fork the Repository

Visit the [Dock GitHub repository](https://github.com/geeth24/dock) and fork the project.

### 2. Clone Your Fork

```bash
git clone https://github.com/<your-username>/dock.git
cd dock
```

### 3. Create a New Branch

Create a branch for your feature or fix:

```bash
git checkout -b feature/your-feature
```

### 4. Make Changes

Make your changes to the codebase. Ensure your code adheres to the project's coding standards.

### 5. Test Your Changes

Test your changes locally to ensure they work as expected:

```bash
pytest
```

### 6. Commit and Push

Commit your changes with a descriptive message:

```bash
git add .
git commit -m "Add new feature: your-feature"
git push origin feature/your-feature
```

### 7. Submit a Pull Request

Go to your fork on GitHub and submit a pull request to the main repository. Include a clear description of your changes and why they are necessary.

---

## Guidelines

- Follow the coding style used in the repository.
- Add comments to explain non-obvious code.
- Update or create documentation for new features.
- Test your changes thoroughly.

---

## Development Workflow

### Installing Dependencies

```bash
pip install -r requirements.txt
```

### Running Tests

Run the test suite to verify your changes:

```bash
pytest
```

---

Thank you for contributing to Dock! Your efforts help make Docker Compose workflows simpler and more efficient.
