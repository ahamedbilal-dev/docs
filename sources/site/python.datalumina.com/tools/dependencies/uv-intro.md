# Source: https://python.datalumina.com/tools/dependencies/uv-intro

## 

[​](https://python.datalumina.com/#see-the-difference)

See the difference

Let’s install a package with pip vs uv:

### 

[​](https://python.datalumina.com/#with-pip-traditional)

With pip (traditional)

```
pip install pandas
# ⏱️ Takes 15-30 seconds
```

### 

[​](https://python.datalumina.com/#with-uv-modern)

With uv (modern)

```
uv pip install pandas
# ⚡ Takes 1-2 seconds
```

That’s 10-30x faster! And it gets better.

## 

[​](https://python.datalumina.com/#real-world-comparison)

Real-world comparison

Creating a new project:

- Traditional way
 
- With uv
 

```
# Create virtual environment
python -m venv .venv

# Activate it (different per OS!)
# Windows: .venv\Scripts\activate
# Mac/Linux: source .venv/bin/activate

# Install packages
pip install requests pandas numpy

# Save dependencies
pip freeze > requirements.txt
```

**Time**: ~45 seconds **Commands**: 4+ (varies by OS)

```
# Everything in one command
uv init
uv add requests pandas numpy
```

**Time**: ~3 seconds **Commands**: 2

## 

[​](https://python.datalumina.com/#why-is-uv-so-fast)

Why is uv so fast?

1. **Written in Rust** - Compiled language, not interpreted Python
2. **Smart caching** - Reuses downloaded files intelligently
3. **Parallel downloads** - Gets multiple packages at once
4. **Better algorithms** - Optimized dependency resolution

## 

[​](https://python.datalumina.com/#more-than-just-speed)

More than just speed

### 

[​](https://python.datalumina.com/#one-tool-not-five)

One tool, not five

Traditional Python:

- `pip` for packages
- `venv` for virtual environments
- `pip-compile` for lock files
- `pyenv` for Python versions
- `pipx` for global tools

With uv:

- `uv` does it all

### 

[​](https://python.datalumina.com/#it-just-works)

It just works

No more:

- “Did I activate my venv?”
- “Which Python am I using?”
- “Why is this package conflicting?”

uv handles it automatically.

### 

[​](https://python.datalumina.com/#modern-features)

Modern features

- **Lock files** - Exact reproducible installs
- **Workspace support** - Multiple related projects
- **Script running** - Built-in task runner
- **Python management** - Install Python versions too

## 

[​](https://python.datalumina.com/#installing-uv)

Installing uv

One command for any system:

- Mac/Linux
 
- Windows
 

```
curl -LsSf https://astral.sh/uv/install.sh | sh
```

```
powershell -c "irm https://astral.sh/uv/install.ps1 | iex"
```

After installation, restart your terminal.

## 

[​](https://python.datalumina.com/#quick-commands)

Quick commands

Here’s what you need to know:

```
# Create new project
uv init my-project

# Add packages
uv add requests pandas

# Install from existing project
uv sync

# Run Python
uv run python script.py
```

## 

[​](https://python.datalumina.com/#should-you-switch)

Should you switch?

**Yes, if you want:**

- Faster development
- Simpler commands
- Less confusion
- Modern tooling

**Maybe wait if:**

- You’re in a team using pip
- You have complex legacy setups
- You’re just starting (learn basics first)

uv is backwards compatible - it can read requirements.txt and work with existing projects!

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Let’s see uv in action by creating a real project.

## Using uv

Create your first uv project

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/tools/dependencies/uv-intro.mdx)

[Modern Python](https://python.datalumina.com/tools/dependencies) [Using uv](https://python.datalumina.com/tools/dependencies/virtual-env)

⌘I