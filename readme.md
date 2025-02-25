# Welcome to uv!

**uv** is a **fast Python package and project manager** built in **Rust**. In simple terms, uv helps you set up Python projects quickly and manage everything you need—like installing Python versions, creating project folders, and handling all your packages (dependencies)—all with a few simple commands.

*Still confused? No worries! Just dive into the full docs and you'll get the hang of everything about uv.*

---

## What Does uv Do?

Imagine you have a toolbox that not only gives you the tools (like Python versions and libraries) but also organizes them for you. That's what uv does!

- **Install Python Versions:** Need a specific Python version? uv's got you covered.
- **Create Projects:** Start a new project with a simple command.
- **Manage Dependencies:** Add, update, or remove packages with ease.
- **Run Your Code:** Execute your Python scripts without hassle.

---

## How to Use uv—Step by Step

### 1. Install a Python Version

Want Python 3.12? Just run:

```bash
uv python install 3.12
```

This command downloads and sets up Python 3.12 for you.

---

### 2. Start a New Project

Create a new project folder with:

```bash
uv init my-new-project
```

Then check out your new project folder:

```bash
ls -la  # Lists all files and folders
cd my-new-project  # Go into your project folder
```

---

### 3. Set Up a Virtual Environment

Keep your project’s packages separate from your system’s packages:

```bash
uv venv --python 3.13
```

Then activate it with:

```bash
source .venv/bin/activate
```

> **Note:** The `.venv` folder is usually ignored by Git, so you won’t accidentally upload your virtual environment.

---

### 4. Manage Your Project Dependencies

#### **Adding Packages**

Need Flask? Just type:

```bash
uv add flask
```

Want SciPy? Try:

```bash
uv add scipy
```

uv will handle installing these packages along with any other things they need.

#### **Editing Dependencies Manually**

You might sometimes list dependencies in a file, like:

```python
dependencies = [
    "pandas>=2.1.1"
]
```

After making changes, run:

```bash
uv sync
```

This command quickly checks your list and installs or removes packages as needed.

#### **Removing Packages**

To remove a package like Flask:

```bash
uv remove flask
```

Or simply delete its entry from your list and run:

```bash
uv sync
```

---

### 5. Run Your Python Script

To run a script called `hello.py`, just use:

```bash
uv run hello.py
```

This ensures your script runs with the right Python version and settings.

---

### 6. Check Your Python Interpreter

Curious about which Python you're using? Check with:

```bash
which python3
```

This shows you the path to the active Python interpreter.

---

## Quick Summary

- **uv** is a fast Python project helper written in Rust.
- It helps you **install Python versions**, **create projects**, **manage packages**, and **run scripts**.
- Use simple commands like:
  - `uv python install <version>`
  - `uv init <project-name>`
  - `uv venv --python <version>`
  - `uv add <package>`
  - `uv sync`
  - `uv remove <package>`
  - `uv run <script.py>`

---

## Final Thoughts

uv is like having a smart assistant that handles Python installations, virtual environments, and package dependencies—all with just a few commands.
