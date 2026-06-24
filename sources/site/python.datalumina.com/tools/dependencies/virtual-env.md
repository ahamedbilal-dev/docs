# Source: https://python.datalumina.com/tools/dependencies/virtual-env

## 

[​](https://python.datalumina.com/#creating-a-new-project)

Creating a new project

Let’s create a real project with uv:

```
# Create and enter project
uv init ai-assistant
cd ai-assistant
```

This creates:

```
ai-assistant/
├── .gitignore      # Git ignore file
├── .python-version # Python version for the project
├── pyproject.toml  # Project configuration
├── README.md       # Project readme
└── main.py         # Example script
```

The `.venv` folder and `uv.lock` file are created automatically when you first run `uv add` to install packages.

## 

[​](https://python.datalumina.com/#understanding-pyproject-toml)

Understanding pyproject.toml

This is your project’s configuration file:

```
[project]
name = "ai-assistant"
version = "0.1.0"
description = "Add your description here"
readme = "README.md"
requires-python = ">=3.12"
dependencies = []
```

It replaces:

- `requirements.txt`
- `setup.py`
- `setup.cfg`
- Multiple config files

One file to rule them all!

## 

[​](https://python.datalumina.com/#adding-packages)

Adding packages

Add packages with `uv add`:

```
# Add a package
uv add requests

# Add multiple packages
uv add pandas numpy matplotlib

# Add development dependencies
uv add --dev pytest black
```

Your `pyproject.toml` updates automatically:

```
[project]
name = "ai-assistant"
version = "0.1.0"
description = "Add your description here"
readme = "README.md"
requires-python = ">=3.12"
dependencies = [
    "requests>=2.32.0",
    "pandas>=2.2.0",
    "numpy>=1.26.0",
    "matplotlib>=3.8.0",
]

[tool.uv]
dev-dependencies = [
    "pytest>=8.0.0",
    "black>=24.0.0",
]
```

## 

[​](https://python.datalumina.com/#the-lock-file)

The lock file

uv creates `uv.lock` - this locks exact versions:

```
# uv.lock (auto-generated)
version = 1
requires-python = ">=3.12"

[[package]]
name = "requests"
version = "2.32.3"
dependencies = [
    { name = "certifi" },
    { name = "charset-normalizer" },
    ...
]
```

This ensures everyone gets exactly the same packages.

## 

[​](https://python.datalumina.com/#running-your-code)

Running your code

Three ways to run Python with uv:

```
# Method 1: uv run (recommended)
uv run python main.py

# Method 2: Activate venv (traditional)
source .venv/bin/activate  # Mac/Linux
# or
.venv\Scripts\activate     # Windows

# Method 3: Direct path
.venv/bin/python main.py
```

`uv run` is recommended - it always uses the right Python!

## 

[​](https://python.datalumina.com/#common-uv-commands)

Common uv commands

```
# Create new project
uv init project-name

# Add packages
uv add package-name

# Remove packages
uv remove package-name

# Install all dependencies
uv sync

# Update packages
uv add --upgrade package-name

# Show installed packages
uv pip list

# Run Python scripts
uv run python script.py
```

## 

[​](https://python.datalumina.com/#working-with-existing-projects)

Working with existing projects

Got a project with `requirements.txt`? No problem:

```
# Convert requirements.txt to pyproject.toml
uv add -r requirements.txt

# Or just install from requirements.txt
uv pip install -r requirements.txt
```

## 

[​](https://python.datalumina.com/#virtual-environment-details)

Virtual environment details

uv creates `.venv` automatically when you add packages:

- Created on first `uv add` command
- No activation needed with `uv run`
- Always in project directory
- Works with VS Code automatically
- Already in `.gitignore` (uv adds it)

## 

[​](https://python.datalumina.com/#tips-and-tricks)

Tips and tricks

1. **Global tools**: Install tools globally with uv
 
 ```
    uv tool install black
    uv tool install mypy
    ```
 
2. **Python versions**: uv can manage Python too
 
 ```
    uv python install 3.12
    uv python install 3.11
    ```
 
3. **Scripts**: Add custom commands
 
 ```
    [project.scripts]
    start = "ai_assistant.main:run"
    test = "pytest tests/"
    ```
 

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Ready to put it all together? Check out the complete project workflow!

## Complete workflow

Start-to-finish project guide

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/tools/dependencies/virtual-env.mdx)

[Why uv?](https://python.datalumina.com/tools/dependencies/uv-intro) [Complete workflow](https://python.datalumina.com/tools/dependencies/complete-setup)

⌘I