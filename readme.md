## What is uv?

**uv** is a **fast Python package and project manager** written in **Rust**. Its main goal is to make your development workflow smoother and faster. Think of it as a powerful tool that not only helps you install Python versions and create projects but also manages all your project dependencies seamlessly. (still confused, just read through the whole documentation—after that, you'll understand everything about uv! )

-------------------------------------------------------------------------------------------------

## Why Use a Package Manager?

A **package manager** is a tool that automates the process of:

- **Installing:** Quickly adding libraries (or packages) that your project needs.
- **Updating:** Keeping your libraries up-to-date.
- **Removing:** Cleaning up unused dependencies.

With uv, you can handle all these tasks with simple commands, ensuring your development environment is always in sync with your project's requirements.

-------------------------------------------------------------------------------------------------

## How Does uv Work? — A Step-by-Step Guide

Here’s a breakdown of some common commands and concepts to help you understand how to use uv effectively.

### 1. **Installing a Python Version**

You can install specific versions of Python directly through uv:

- uv python install 3.12

This command downloads and sets up Python 3.12 for your projects.

-------------------------------------------------------------------------------------------------

### 2. **Initializing a New Project**

Create a new project with a predefined structure:

- uv init my-new-project

Then, navigate to your project folder:

- ls -la           # List all files to see the project structure
- cd my-new-project

-------------------------------------------------------------------------------------------------

### 3. **Setting Up a Virtual Environment**

Create a virtual environment with a specific Python version:

- uv venv --python 3.13

Activate the environment:

- source .venv/bin/activate  # '.venv' is typically ignored by git to keep your env private

-------------------------------------------------------------------------------------------------

### 4. **Managing Dependencies**

uv makes dependency management super easy:

#### **Adding Dependencies with Commands:**

To add a library like Flask:

- uv add flask

Similarly, add other libraries such as SciPy:

- uv add scipy

uv takes care of installing Flask (or SciPy) along with any other packages they might need.

#### **Manual Dependency Editing:**

Sometimes, you might prefer to add dependencies by editing a list directly. For example, you might have a file with a dependency list like this:


dependencies = [
    "pandas>=2.1.1"
]

After making your changes, run:

- uv sync

This command scans your dependencies, installs new ones, and removes any that are no longer needed—all in under a second!

#### **Removing Dependencies:**

- **Manually:** Delete the entry from your dependency list and run 

- uv sync

- **Via Command:**

- uv remove flask

This removes Flask from your project dependencies.

-------------------------------------------------------------------------------------------------

### 5. **Running Your Project**

To run your Python script, simply use:

- uv run hello.py

This command ensures that your script runs with the correct Python interpreter and environment settings.

-------------------------------------------------------------------------------------------------

### 6. **Checking Your Python Interpreter**

If you want to see which Python interpreter is active, you can use:

- which python3

This shows the path to the current Python version, similar to what happens when you run your script with uv.

-------------------------------------------------------------------------------------------------

## Quick Reference Summary

- **uv**: A fast package and project manager for Python (written in Rust).
- **Package Manager**: A tool that automates installing, updating, and removing project dependencies.
- **Common Commands**:
  - `uv python install <version>`: Install a Python version.
  - `uv init <project-name>`: Create a new project.
  - `uv venv --python <version>`: Set up a virtual environment.
  - `uv add <package>`: Add a new dependency.
  - `uv sync`: Synchronize your project’s dependencies.
  - `uv remove <package>`: Remove a dependency.
  - `uv run <script.py>`: Run your project script.

-------------------------------------------------------------------------------------------------

## Final Thoughts

Using **uv** simplifies many of the routine tasks in Python project management. It’s like having a smart assistant that handles Python installations, virtual environments, and package dependencies—all with just a few commands.

-------------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------------
