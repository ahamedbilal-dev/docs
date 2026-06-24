# Source: https://python.datalumina.com/libraries-apis/importing-modules

## 

[​](https://python.datalumina.com/#using-packages)

Using packages

Python packages add new functionality to your programs. There are two types:

- **Built-in**: Come with Python (no installation needed)
- **External**: Need to install first with pip

## 

[​](https://python.datalumina.com/#understanding-the-terminology)

Understanding the terminology

Let’s clarify what these terms mean:

- **Module**: A single Python file (like `math.py`)
- **Package**: A folder containing multiple modules
- **Function**: A reusable block of code (like `print()` or `sqrt()`)
- **Class**: A blueprint for creating objects (we’ll cover this later)

Think of it like this:

- A **module** is like a toolbox
- A **package** is like a garage with multiple toolboxes
- A **function** is like a specific tool (hammer, screwdriver)
- A **class** is like a blueprint for building tools

## 

[​](https://python.datalumina.com/#import-patterns-explained)

Import patterns explained

```
# Pattern 1: Import the whole module
import math
# Now use: math.sqrt(16)

# Pattern 2: Import specific items from a module
from math import sqrt, pi
# Now use: sqrt(16)
```

What’s happening:

- `import math` - brings in the entire math toolbox
- `from math import sqrt` - takes just the sqrt tool from the math toolbox

## 

[​](https://python.datalumina.com/#built-in-modules)

Built-in modules

Python includes many useful modules:

```
# Import entire module
import random

# Use module functions
number = random.randint(1, 10)
choice = random.choice(["apple", "banana", "orange"])
```

### 

[​](https://python.datalumina.com/#common-built-in-modules)

Common built-in modules

```
# Date and time
import datetime
today = datetime.date.today()
print(today)  # 2024-01-15

# Operating system
import os
current_dir = os.getcwd()
print(current_dir)

# JSON data
import json
data = {"name": "Alice", "age": 30}
json_string = json.dumps(data)
```

## 

[​](https://python.datalumina.com/#import-methods)

Import methods

Different ways to import:

```
# Import entire module
import math
result = math.sqrt(16)

# Import specific functions
from math import sqrt, pi
result = sqrt(16)
circle_area = pi * radius ** 2

# Import with alias
import pandas as pd
df = pd.DataFrame(data)

# Import everything (avoid this!)
from math import *
```

Avoid `from module import *` as it can cause naming conflicts and makes code harder to understand.

## 

[​](https://python.datalumina.com/#installing-packages)

Installing packages

External packages need installation:

```
# Install a package
pip install requests

# Install specific version
pip install requests==2.28.0

# Install multiple packages
pip install pandas numpy matplotlib
```

Always ensure your virtual environment is activated before installing! This is the #1 source of import errors. If you get “ModuleNotFoundError” after installing, you probably installed to the wrong environment. [Learn more about virtual environments](https://python.datalumina.com/getting-started/virtual-environments).

## 

[​](https://python.datalumina.com/#sharing-your-project-requirements-txt)

Sharing your project: requirements.txt

When you share your Python project, others need to know which packages to install. The standard way is using a `requirements.txt` file:

### 

[​](https://python.datalumina.com/#creating-requirements-txt)

Creating requirements.txt

List all your project’s packages:

```
pip freeze > requirements.txt
```

This creates a file like:

```
certifi==2024.2.2
charset-normalizer==3.3.2
idna==3.6
requests==2.31.0
urllib3==2.2.0
```

### 

[​](https://python.datalumina.com/#installing-from-requirements-txt)

Installing from requirements.txt

When someone gets your project, they run:

```
pip install -r requirements.txt
```

This installs all the packages at once!

Later in the course, we’ll learn about `uv` - a modern, faster alternative to pip that makes package management even easier.

## 

[​](https://python.datalumina.com/#using-external-packages)

Using external packages

After installation, import and use:

```
# Web requests
import requests

response = requests.get("https://api.example.com/data")
data = response.json()

# Data analysis
import pandas as pd

# Create a simple DataFrame
data = {
    'name': ['Alice', 'Bob', 'Charlie'],
    'age': [25, 30, 35],
    'city': ['NYC', 'LA', 'Chicago']
}
df = pd.DataFrame(data)
print(df)
```

Always use virtual environments for projects. They prevent package conflicts between different projects.

## 

[​](https://python.datalumina.com/#finding-packages)

Finding packages

Where to find packages:

- [PyPI](https://pypi.org) - Official Python package index
- [Awesome Python](https://github.com/vinta/awesome-python) - Curated list
- **ChatGPT** - Ask “What Python package should I use for \[task\]?” - Great for recommendations and comparisons
- Google “Python package for \[task\]”

ChatGPT is excellent for finding packages. Try asking: “What’s the best Python package for reading Excel files?” or “Compare pandas vs polars for data analysis.” It can explain which package to use and why.

## 

[​](https://python.datalumina.com/#common-mistakes)

Common mistakes

Import errors

```
# Wrong - package not installed or venv not activated
import pandas  # ModuleNotFoundError

# Right - install first
# Run: pip install pandas
import pandas
```
Name conflicts

```
# Wrong - overwrites built-in
import datetime
datetime = "2024-01-01"  # Now module is gone!

# Right - use different names
import datetime
date_string = "2024-01-01"
```

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Learn to connect to APIs and fetch data from the internet!

## Working with APIs

Connect to online services

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/libraries-apis/importing-modules.mdx)

[External tools](https://python.datalumina.com/libraries-apis) [Working with APIs](https://python.datalumina.com/libraries-apis/working-with-apis)

⌘I