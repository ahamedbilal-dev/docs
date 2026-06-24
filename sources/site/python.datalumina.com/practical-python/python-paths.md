# Source: https://python.datalumina.com/practical-python/python-paths

## 

[​](https://python.datalumina.com/#the-most-confusing-part-of-python)

The most confusing part of Python

Understanding paths is probably the most confusing part when starting with Python. You’ll make mistakes with file paths and imports, and that’s totally fine. That’s how everyone learns. This page gives you a quick introduction. Some parts might not be completely clear right now, but as you practice, it will click. Come back to this page when you run into path issues - it happens to everyone!

## 

[​](https://python.datalumina.com/#the-mental-model)

The mental model

When working with multiple files, always think about two things:

1. **Where am I?** - What folder is my Python script in?
2. **Where do I want to go?** - What file or module do I need?

Then navigate:

- **Going down** into subfolders: Use `/` for files, `.` for imports
- **Going up** to parent folders: Use `../` for files, add to sys.path for imports
- **Same folder**: Just use the filename

```
# From script.py, accessing different locations:
"data/sales.csv"        # Down into data folder
"../config.json"        # Up one level
"helper.py"             # Same folder

# For imports:
import helper           # Same folder - no path needed!
import data.processor   # Down into data folder

# Parent folder imports need sys.path:
import sys
sys.path.append("..")   # Add parent to path
import parent_module    # Now you can import
```

## 

[​](https://python.datalumina.com/#the-simple-rule)

The simple rule

When Python runs, it has a “current working directory” - the folder it’s currently in. All file paths start from there.

```
import os

# See where Python is right now
print(os.getcwd())
```

Try this - it shows you exactly where Python is looking for files.

## 

[​](https://python.datalumina.com/#finding-your-files)

Finding your files

Let’s say you have this structure:

```
my-project/
├── script.py
├── data.txt
└── folder/
    └── other.txt
```

If you run `script.py`:

```
# Python can find these:
open("data.txt")           # Same folder
open("folder/other.txt")   # Subfolder

# Python CAN'T find these (they don't exist from here):
open("other.txt")          # Wrong! It's in a subfolder
open("../parent.txt")      # Looking in parent folder
```

## 

[​](https://python.datalumina.com/#files-vs-modules-key-difference)

Files vs modules - key difference

Python handles regular files and Python modules differently: **Regular files (CSV, TXT, JSON):**

- Use `open()` or file-reading functions
- Need the exact path from your current directory
- Use forward slashes: `data/sales.csv`

```
# Reading a CSV file - needs exact path
with open("data/sales.csv", "r") as file:
    content = file.read()
```

**Python modules (importing code):**

- Use `import` statements
- Python searches in multiple locations (sys.path)
- Use dots instead of slashes: `folder.module`

```
# Importing a module - Python searches for it
import mymodule                    # Looks for mymodule.py
from folder.utils import helper    # Looks for folder/utils.py
```

## 

[​](https://python.datalumina.com/#how-python-finds-modules)

How Python finds modules

Python looks for modules (other .py files) in specific places. You can see these places:

```
import sys
print(sys.path)  # List of folders Python checks
```

The list includes:

1. The folder containing your script
2. Python’s built-in library folders
3. Installed packages

## 

[​](https://python.datalumina.com/#adding-your-own-folders)

Adding your own folders

Sometimes you need Python to look in additional places:

```
import sys

# Add a folder to Python's search path
sys.path.append("/path/to/my/folder")

# Now you can import from that folder
import mymodule
```

Common example - importing from a parent folder:

```
import sys
import os

# Go up one level from current script
parent = os.path.dirname(os.path.dirname(__file__))
sys.path.append(parent)
```

## 

[​](https://python.datalumina.com/#common-mistakes)

Common mistakes

FileNotFoundError: No such file or directory

This happens when Python can’t find your file. The file path is wrong or you’re running from a different folder than expected.

```
# Debug it:
import os
print("Looking in:", os.getcwd())
print("Files available:", os.listdir())
```

Fix: Use the correct path from your current directory, or use absolute paths.

ModuleNotFoundError: No module named 'X'

Python can’t find the module you’re trying to import. It’s not in any of the folders Python searches.

```
# See where Python looks:
import sys
print("Python searches in:", sys.path)
```

Fix: Make sure the module is in one of those folders, or add its folder to sys.path.

Mixing up files and modules

Remember: regular files use paths with slashes, Python modules use dots.

```
# Wrong:
import data/helpers  # SyntaxError!

# Right:
import data.helpers  # For data/helpers.py
```

Running from the wrong folder

Your script works in VS Code but not in terminal? You’re probably in a different folder.

```
# Always check first:
import os
print("Running from:", os.getcwd())
```

Fix: Navigate to the right folder in terminal, or use the VS Code play button.

Using backslashes on Mac/Linux

Windows uses backslashes, but Mac/Linux use forward slashes. Use forward slashes - they work everywhere!

```
# Works everywhere:
"data/file.csv"

# Only works on Windows:
"data\\file.csv"
```

## 

[​](https://python.datalumina.com/#keep-it-simple)

Keep it simple

Remember, everyone struggles with paths at first. For now:

- Keep related files in the same folder
- Use the VS Code play button (it’s predictable)
- When confused, print `os.getcwd()` to see where you are
- Come back to this page when you hit path errors

The mental model: Know where you are, know where you want to go, then navigate with `/` for files. For imports, same folder needs no path, subfolders use `.`, parent folders need sys.path.

## Working with files

Apply these concepts to read and write files

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/practical-python/python-paths.mdx)

[Project structure](https://python.datalumina.com/practical-python/project-structure) [Working with files](https://python.datalumina.com/practical-python/working-with-files)

⌘I