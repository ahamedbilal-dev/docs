# Source: https://python.datalumina.com/getting-started/virtual-environments

## 

[​](https://python.datalumina.com/#your-python-installation)

Your Python installation

Remember when we installed Python? That installation lives in a specific folder on your computer:

- **Windows**: `C:\Users\[YourName]\AppData\Local\Programs\Python\Python313\`
- **macOS**: `/Library/Frameworks/Python.framework/Versions/3.13/`
- **Linux**: `/usr/bin/python3`

This is your “system Python” - it’s shared by everything on your computer.

## 

[​](https://python.datalumina.com/#the-problem-with-sharing)

The problem with sharing

Imagine you’re working on two projects:

- **Project A** needs version 1.0 of a tool
- **Project B** needs version 2.0 of the same tool

If you install version 2.0 for Project B, you just broke Project A! This is where virtual environments save the day.

## 

[​](https://python.datalumina.com/#what-are-virtual-environments)

What are virtual environments?

A virtual environment is like a private copy of Python for each project. Think of it as:

- A separate folder for each project
- Its own Python installation
- Its own place to install packages
- Complete isolation from other projects

Virtual environments are so important that I create a new one for EVERY project. It’s a Python best practice that will save you from many headaches.

## 

[​](https://python.datalumina.com/#understanding-packages)

Understanding packages

Before we continue, let’s understand what packages are: **Packages** are pre-written code that others have created for us to use. Instead of writing everything from scratch, we can import these packages. For example:

- `requests` - for downloading web pages
- `pandas` - for working with data
- `openai` - for using AI models

Each package has different versions, and different projects might need different versions.

## 

[​](https://python.datalumina.com/#create-your-first-virtual-environment)

Create your first virtual environment

Let’s create one for our `python-for-ai` project. You have two methods:

### 

[​](https://python.datalumina.com/#method-1-vs-code-command-palette-easier)

Method 1: VS Code Command Palette (easier)

1. Open your project in VS Code
2. Press `Ctrl/Cmd + Shift + P`
3. Type “Python: Create Environment”
4. Select “Venv”
5. Select your Python installation
6. VS Code creates and activates everything for you!

### 

[​](https://python.datalumina.com/#method-2-terminal-command)

Method 2: Terminal command

1. Open the terminal in VS Code (View > Terminal)
2. Make sure you’re in your project folder
3. Run this command:

- Windows
 
- macOS/Linux
 

```
python -m venv .venv
```

```
python3 -m venv .venv
```

What this does:

- `python -m venv` - Run Python’s virtual environment module
- `.venv` - The name of the folder to create (convention is to use “.venv” with a dot)

## 

[​](https://python.datalumina.com/#what-just-happened)

What just happened?

Look at your project folder - you now have a new `.venv` folder:

```
python-for-ai/
├── .venv/          # Your virtual environment (hidden folder)
├── hello.py        # Your code
└── python-for-ai.code-workspace
```

The dot in `.venv` makes it a hidden folder on Mac/Linux. This keeps your project clean since you don’t need to see this folder often.

This `.venv` folder contains:

- A copy of Python
- A place to install packages
- Scripts to activate/deactivate

## 

[​](https://python.datalumina.com/#activate-your-virtual-environment)

Activate your virtual environment

VS Code makes activation super easy:

1. Press `Ctrl/Cmd + Shift + P` to open Command Palette
2. Type “Python: Select Interpreter”
3. Choose the one that says `.venv` (it will show the full path like `./.venv/bin/python`)
4. That’s it! VS Code automatically activates it for you

You’ll know it’s working when you see `(.venv)` in your terminal:

```
(.venv) PS C:\...\python-for-ai>
```

This is my recommended approach. VS Code remembers your choice and automatically activates the environment every time you open the project!

## 

[​](https://python.datalumina.com/#common-issues)

Common issues

Command not found

If `python -m venv` doesn’t work, you might need to install it:**Ubuntu/Debian**:

```
sudo apt install python3-venv
```

**Other systems**: It should come with Python by default

Permission denied

On macOS/Linux, you might need to make the activate script executable:

```
chmod +x .venv/bin/activate
```

VS Code not recognizing venv

1. Reload VS Code window: `Ctrl/Cmd + Shift + P` > “Developer: Reload Window”
2. Manually select interpreter again
3. Make sure the Python extension is installed

## 

[​](https://python.datalumina.com/#what-about-anaconda)

What about Anaconda?

You might have heard of Anaconda - it’s another tool that manages Python environments and packages. It’s popular in the data science world because it comes pre-loaded with many data science packages. However, I don’t recommend using Anaconda unless you have a specific reason to.

Stick with Python’s built-in virtual environments unless your company or a specific project requires Anaconda. You’ll have a lighter, faster, and simpler setup.

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Your virtual environment is ready! Now let’s learn about Python packages and how to install them.

## Python packages

Understanding pip and package management

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/getting-started/virtual-environments.mdx)

[Course resources](https://python.datalumina.com/getting-started/course-resources) [Packages and pip](https://python.datalumina.com/getting-started/packages-and-pip)

⌘I