# Source: https://python.datalumina.com/tools/git/version-control

## 

[​](https://python.datalumina.com/#the-problem-git-solves)

The problem Git solves

Imagine working on a Python project. You’ve probably done this:

- `my_script.py`
- `my_script_v2.py`
- `my_script_v2_final.py`
- `my_script_v2_final_ACTUALLY_FINAL.py`
- `my_script_backup_before_breaking_everything.py`

Git solves this mess by tracking changes properly.

## 

[​](https://python.datalumina.com/#how-git-works)

How Git works

Think of Git as taking snapshots of your code:

1. **You write code** - Make changes to your files
2. **You save a snapshot** - Called a “commit” in Git
3. **Git remembers everything** - Every snapshot, who made it, when, and why

```
# Monday: Your code works
def calculate_price(amount):
    return amount * 1.20  # 20% markup

# Tuesday: Boss wants 25% markup
def calculate_price(amount):
    return amount * 1.25  # Changed from 20% to 25%

# Wednesday: "Actually, can we go back to 20%?"
# With Git: Easy! Just go back to Monday's version
# Without Git: Hope you still have that file somewhere...
```

## 

[​](https://python.datalumina.com/#key-concepts-all-you-need)

Key concepts (all you need)

**Repository (repo)**: A project tracked by Git

- Your `python-for-ai` folder can be a repository

**Staging**: Choosing which changes to save

- Like selecting items to put in a box before shipping

**Commit**: A saved snapshot of your code

- Like saving in a video game - you can always go back

**Push**: Upload your commits to GitHub

- Backs up your code online

**Pull**: Download changes from GitHub

- Get updates when working with others

**Clone**: Copy a project from GitHub

- How you get AI projects to try

## 

[​](https://python.datalumina.com/#first-install-git)

First: Install Git

Check if you have Git:

```
git --version
```

If you see a version number, you’re good! If not, install Git:

- Windows
 
- macOS
 
- Linux
 

1. Download from [git-scm.com](https://git-scm.com/download/win)
2. Run the installer
3. Keep all default settings
4. Restart VS Code after installation

Visit [git-scm.com/downloads/mac](https://git-scm.com/downloads/mac) for installation options.**Easiest method (recommended):**

```
# If you have Homebrew installed
brew install git
```

**Alternative:** Install Xcode Command Line Tools (includes Git):

```
git --version
```

macOS will prompt to install if Git is not found. Click “Install” and wait a few minutes.

```
# Ubuntu/Debian
sudo apt update
sudo apt install git

# Fedora
sudo dnf install git

# Arch
sudo pacman -S git
```

## 

[​](https://python.datalumina.com/#the-simplest-git-workflow)

The simplest Git workflow

Here’s literally all you need to know for now:

These are terminal commands, not Python code! Run them in VS Code’s terminal.

```
# 0. First time only - initialize Git in your project
git init

# 1. Save your changes locally
git add .
git commit -m "Add price calculation function"

# 2. Upload to GitHub (after connecting to GitHub - see next pages)
git push

# That's it! Your code is saved and backed up
```

If you see “fatal: not a git repository”, you need to run `git init` first. This only needs to be done once per project.

You can run these commands:

- **One by one**: Type each command and press Enter
- **All together**: Copy and paste all three lines - the terminal runs them in sequence

## 

[​](https://python.datalumina.com/#common-questions)

Common questions

Do I need to use the terminal?

No! VS Code has buttons for all Git operations. We’ll show you both ways, but you can stick to clicking buttons if you prefer.

What if I mess up?

Git is very forgiving. Every commit is saved forever, so you can always go back. It’s actually harder to lose work with Git than without it.

Is Git the same as GitHub?

No. Git is the tool on your computer. GitHub is a website that stores Git projects. You can use Git without GitHub, but GitHub makes sharing easier.

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Let’s create your GitHub account so you have somewhere to store your code.

## GitHub setup

Create your account in 5 minutes

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/tools/git/version-control.mdx)

[Git & GitHub](https://python.datalumina.com/tools/git) [GitHub setup](https://python.datalumina.com/tools/git/github-setup)

⌘I