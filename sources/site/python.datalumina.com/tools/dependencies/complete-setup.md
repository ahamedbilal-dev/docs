# Source: https://python.datalumina.com/tools/dependencies/complete-setup

## 

[​](https://python.datalumina.com/#new-project-checklist)

New project checklist

Follow these steps every time you start a new Python project.

## 

[​](https://python.datalumina.com/#step-1-open-terminal)

Step 1: Open terminal

Open your terminal:

- **Mac**: Terminal app or iTerm
- **Windows**: Terminal, Command Prompt, or PowerShell

## 

[​](https://python.datalumina.com/#step-2-navigate-to-your-projects-folder)

Step 2: Navigate to your projects folder

```
# Go to your projects directory
cd ~/Documents/Projects  # Mac
cd C:\Users\YourName\Documents\Projects  # Windows
```

Create a dedicated folder for all your Python projects. This keeps things organized!

## 

[​](https://python.datalumina.com/#step-3-create-the-project)

Step 3: Create the project

Use uv to create your project:

```
uv init my-awesome-project
```

**What happens:**

- Creates a new folder `my-awesome-project`
- Creates `.gitignore` (Git will ignore `.venv`, `.env`, etc.)
- Creates `.python-version` (specifies Python version)
- Creates `pyproject.toml` (project configuration)
- Creates `README.md` (project description)
- Creates `main.py` (example file)

**Initial structure:**

```
my-awesome-project/
├── .gitignore      # Git ignore rules
├── .python-version # Python version
├── pyproject.toml  # Project config
├── README.md       # Project description
└── main.py         # Example file
```

The `.venv` folder is created automatically when you run `uv add` to install your first package. Same with `uv.lock`.

## 

[​](https://python.datalumina.com/#step-4-open-in-vs-code)

Step 4: Open in VS Code

```
# Enter the project folder
cd my-awesome-project

# Open in VS Code
code .
```

**What happens:**

- VS Code opens with your project
- Python extension activates automatically
- Virtual environment is detected

If `code .` doesn’t work, see the Git section for setup instructions.

## 

[​](https://python.datalumina.com/#step-5-add-packages)

Step 5: Add packages

Open terminal in VS Code (`` Ctrl+` ``):

```
# Add packages you need
uv add requests
uv add pandas numpy
uv add python-dotenv

# For interactive Python (optional)
uv add ipykernel
```

**What happens:**

-   Packages download and install
-   `pyproject.toml` updates with dependencies
-   `uv.lock` locks exact versions

## 

[​](https://python.datalumina.com/#step-6-test-your-setup)

Step 6: Test your setup

Edit `main.py`:

```
import requests
from dotenv import load_dotenv
import os

# Load environment variables
load_dotenv()

# Test the setup
print("✅ Packages imported successfully!")

# Test environment variable
api_key = os.environ.get("API_KEY", "not-set")
print(f"✅ API_KEY: {api_key}")

# Test requests
response = requests.get("https://api.github.com")
print(f"✅ GitHub API status: {response.status_code}")
```

Run it:

```
uv run python main.py
```

## 

[​](https://python.datalumina.com/#step-7-set-up-environment-variables)

Step 7: Set up environment variables

Create `.env` for secrets:

```
# .env
API_KEY=your-secret-key-here
DATABASE_URL=postgresql://localhost/mydb
DEBUG=True
```

Create `.env.example` for others:

```
# .env.example
API_KEY=your-api-key-here
DATABASE_URL=your-database-url
DEBUG=True
```

**Important**: `.env` is already in `.gitignore` - your secrets are safe!

## 

[​](https://python.datalumina.com/#step-8-initialize-git)

Step 8: Initialize Git

```
# Initialize Git repository
git init

# Add all files
git add .

# First commit
git commit -m "Initial commit"
```

**What happens:**

-   Git starts tracking your files
-   All files except those in `.gitignore` are staged
-   Your first snapshot is saved

## 

[​](https://python.datalumina.com/#step-9-create-github-repository)

Step 9: Create GitHub repository

Create the repository directly from your terminal:

-   Using GitHub CLI (Recommended)
    
-   Using Git (Traditional)
    

```
# Create private repository
gh repo create my-awesome-project --private --source=. --remote=origin --push

# Or create public repository
gh repo create my-awesome-project --public --source=. --remote=origin --push
```

**What happens:**

-   Creates repository on GitHub
-   Sets up remote connection
-   Pushes your code automatically

If you don’t have GitHub CLI, install it:**Mac:**

```
brew install gh
```

**Windows:**

```
winget install --id GitHub.cli
# Or download from cli.github.com
```

**Linux:**

```
# Debian/Ubuntu
curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo dd of=/usr/share/keyrings/githubcli-archive-keyring.gpg
sudo chmod go+r /usr/share/keyrings/githubcli-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null
sudo apt update
sudo apt install gh
```

After installing, authenticate with:

```
gh auth login
```

If you prefer the traditional way:

1.  Go to [github.com](https://github.com)
2.  Click **+** > **New repository**
3.  Name it `my-awesome-project`
4.  Choose Private or Public
5.  **Don’t** add any files
6.  Click **Create repository**

Then run:

```
git remote add origin https://github.com/YOUR-USERNAME/my-awesome-project.git
git push -u origin main
```

**You’re done!** Your project is now:

-   Set up locally with uv
-   Tracked by Git
-   Backed up on GitHub

## 

[​](https://python.datalumina.com/#the-daily-workflow)

The daily workflow

From here, your routine is:

```
# Make changes to your code...

# Add packages as needed
uv add some-package

# Commit changes
git add .
git commit -m "Add new feature"

# Push to GitHub
git push
```

**Prefer clicking?** You can do all Git operations using VS Code’s UI:

-   **Source Control panel** (Ctrl+Shift+G): Stage, commit, and push with clicks
-   **Status bar**: Shows branch and sync button
-   **Command Palette** (Ctrl+Shift+P): Type “Git” to see all commands

See the Git & GitHub section for details!

## 

[​](https://python.datalumina.com/#quick-reference)

Quick reference

```
# Project setup (one time)
uv init project-name
cd project-name
code .
git init
git add .
git commit -m "Initial commit"
gh repo create project-name --private --source=. --remote=origin --push

# Daily development
uv add package-name        # Add packages
uv run python script.py    # Run code
git add .                  # Stage changes
git commit -m "message"    # Commit
git push                   # Push to GitHub
```

## 

[​](https://python.datalumina.com/#pro-tips)

Pro tips

1.  **Commit often** - Small commits are better than huge ones
2.  **Write clear messages** - “Fix login bug” not “updates”
3.  **Use .env** - Never hardcode secrets
4.  **Keep it simple** - Don’t over-engineer

## 

[​](https://python.datalumina.com/#commands-summary)

Commands summary

Here’s everything in one place:

```
# Setup (one time)
uv init my-project
cd my-project
code .
uv add requests pandas python-dotenv
uv add --dev ipykernel
echo "API_KEY=your-key" > .env
git init
git add .
git commit -m "Initial commit"
gh repo create my-project --private --source=. --remote=origin --push

# Daily workflow
uv add package-name        # Add packages
uv run python script.py    # Run code
git add .                  # Stage changes
git commit -m "message"    # Commit
git push                   # Push to GitHub
```

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next

You’ve completed the Python fundamentals course. Continue your journey with these next steps:

## Course summary

See what you’ve learned and continue with AI agents in Python

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/tools/dependencies/complete-setup.mdx)

[Using uv](https://python.datalumina.com/tools/dependencies/virtual-env)

⌘I