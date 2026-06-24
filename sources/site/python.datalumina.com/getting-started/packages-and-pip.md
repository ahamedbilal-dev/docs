# Source: https://python.datalumina.com/getting-started/packages-and-pip

## 

[​](https://python.datalumina.com/#standing-on-the-shoulders-of-giants)

Standing on the shoulders of giants

One of Python’s superpowers is its massive collection of packages. Instead of writing everything from scratch, you can use code that others have already written, tested, and shared.

## 

[​](https://python.datalumina.com/#what-are-packages)

What are packages?

**Packages** are collections of Python code that solve specific problems:

- **requests** - Download web pages and data
- **pandas** - Work with spreadsheets and data
- **numpy** - Fast mathematical operations
- **openai** - Connect to AI models
- **beautifulsoup4** - Extract data from websites

Each package is like a toolbox with specialized tools for a specific job.

## 

[​](https://python.datalumina.com/#meet-pip)

Meet pip

**pip** (Pip Installs Packages) is Python’s package manager. It:

- Downloads packages from the internet
- Installs them in your environment
- Manages versions and dependencies

pip comes with Python, so you already have it! When you activated your virtual environment, you got your own copy of pip.

## 

[​](https://python.datalumina.com/#your-first-package-installation)

Your first package installation

Now we need to use the terminal - your command center for managing packages.

### 

[​](https://python.datalumina.com/#understanding-the-terminal)

Understanding the terminal

The terminal is where you type commands to control Python. Most of the time, VS Code handles everything automatically (like running your code). But for installing packages, we need to type commands ourselves. Open your terminal:

- **Keyboard shortcut**: Press `` Ctrl + ` `` (Windows/Linux) or `` Cmd + ` `` (macOS)
-   **Menu**: View > Terminal

When the terminal opens, you’ll see something like:

```
(.venv) PS C:\...\python-for-ai>
```

That `(.venv)` at the beginning? That’s VS Code telling you “I’ve activated your virtual environment for you!” This means any packages you install will go into your project, not your computer’s main Python.

### 

[​](https://python.datalumina.com/#install-your-first-package)

Install your first package

Let’s install the `requests` package:

```
pip install requests
```

Just type that command and press Enter. You’ll see output like:

```
Collecting requests
  Downloading requests-2.31.0-py3-none-any.whl (62 kB)
Installing collected packages: requests
Successfully installed requests-2.31.0
```

### 

[​](https://python.datalumina.com/#what-just-happened)

What just happened?

No magic here! When you ran `pip install requests`, here’s what happened:

1.  **pip connected to PyPI** (Python Package Index) - a huge website where developers share their code
2.  **Downloaded the requests package** - just a bunch of Python files that someone else wrote
3.  **Saved it in your `.venv` folder** - specifically in `.venv/lib/python3.x/site-packages/`

That’s it! You just downloaded someone else’s Python code and saved it in your project. Now you can use their code as if you wrote it yourself.

Want to see the actual files? Look in your `.venv` folder and navigate to `lib` > `python3.x` > `site-packages` > `requests`. It’s just Python files!

## 

[​](https://python.datalumina.com/#using-installed-packages)

Using installed packages

Now you can use this package in your Python code:

```
import requests

# Download a web page
response = requests.get("https://api.github.com")
print(response.status_code)  # Should print 200
```

Without the requests package, downloading web data would require dozens of lines of complex code. With it, it’s just two lines!

## 

[​](https://python.datalumina.com/#see-what’s-installed)

See what’s installed

To check which packages you have:

```
pip list
```

Output:

```
Package            Version
------------------ --------
certifi           2024.2.2
charset-normalizer 3.3.2
idna              3.6
pip               24.0
requests          2.31.0
urllib3           2.2.0
```

Notice how installing `requests` also installed other packages it needs (like `urllib3`). pip handles this automatically!

## 

[​](https://python.datalumina.com/#install-specific-versions)

Install specific versions

Sometimes you need a specific version of a package:

```
# Install exact version
pip install requests==2.30.0

# Install minimum version
pip install requests>=2.28.0

# Install compatible version
pip install requests~=2.31.0
```

## 

[​](https://python.datalumina.com/#uninstall-packages)

Uninstall packages

Made a mistake or no longer need something?

```
pip uninstall requests
```

pip will ask for confirmation before removing it.

## 

[​](https://python.datalumina.com/#where-packages-come-from)

Where packages come from

pip downloads packages from [PyPI](https://pypi.org/) (Python Package Index), which hosts over 500,000 packages! Anyone can upload packages there, which is why Python has tools for everything.

## 

[​](https://python.datalumina.com/#common-issues)

Common issues

pip: command not found

Your virtual environment might not be activated:

1.  Check for `(.venv)` in your terminal prompt
2.  If missing, activate it using VS Code’s Python interpreter selection
3.  Or activate manually with the terminal commands from the previous section

Permission denied

You’re probably trying to install in system Python:

-   Make sure your virtual environment is activated
-   Never use `sudo pip install`
-   Always see `(.venv)` before installing

Package not found

The package name might be different from what you expect:

-   Check the exact name on [pypi.org](https://pypi.org)
-   Example: “Beautiful Soup” is actually `beautifulsoup4`
-   Example: “OpenAI” is just `openai` (lowercase)

## 

[​](https://python.datalumina.com/#ready-for-interactive-python)

Ready for interactive Python

Now that you understand packages, let’s install what we need for interactive Python mode!

## Interactive Python

Learn my favorite way to write Python code

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/getting-started/packages-and-pip.mdx)

[Virtual environments](https://python.datalumina.com/getting-started/virtual-environments) [Interactive Python](https://python.datalumina.com/getting-started/interactive-python)

⌘I