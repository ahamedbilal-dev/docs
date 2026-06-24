# Source: https://python.datalumina.com/tools/git/clone-create

## 

[​](https://python.datalumina.com/#two-things-you’ll-do-often)

Two things you’ll do often

1. **Clone** - Download existing projects from GitHub
2. **Create** - Start new projects and upload them

Let’s learn both.

## 

[​](https://python.datalumina.com/#cloning-a-repository)

Cloning a repository

Cloning means downloading a project from GitHub to your computer.

### 

[​](https://python.datalumina.com/#example-clone-an-ai-project)

Example: Clone an AI project

Let’s clone a real project to see how it works:

**Pro tip**: Instead of using `cd` to navigate:**Mac**: Right-click a folder in Finder > Services > New Terminal at Folder (or hold Option and right-click > “Open in Terminal”)**Windows**: Right-click a folder in File Explorer > “Open in Terminal” (or Shift + right-click > “Open PowerShell window here”)This opens the terminal already in that folder!

- HTTPS (Recommended)
 
- SSH
 

```
# Open Terminal (Mac) or Command Prompt (Windows)
# Navigate to where you want the project
cd ~/Documents  # Mac
cd C:\Users\YourName\Documents  # Windows

# Clone using HTTPS URL
git clone https://github.com/openai/openai-quickstart-python.git

# Go into the project
cd openai-quickstart-python

# Open in VS Code (see note below if this doesn't work)
code .
```

```
# Open Terminal (Mac) or Command Prompt (Windows)
# Navigate to where you want the project
cd ~/Documents  # Mac
cd C:\Users\YourName\Documents  # Windows

# Clone using SSH URL
git clone git@github.com:openai/openai-quickstart-python.git

# Go into the project
cd openai-quickstart-python

# Open in VS Code (see note below if this doesn't work)
code .
```

**If `code .` doesn’t work**, you need to enable it first:**Mac:**

1. Open VS Code
2. Press `Cmd + Shift + P`
3. Type “Shell Command: Install ‘code’ command in PATH”
4. Press Enter
5. Restart your terminal

**Windows:**

1. During VS Code installation, check “Add to PATH”
2. If you missed it, reinstall VS Code and check that option
3. Or manually: Right-click project folder > “Open with Code”

That’s it! You now have the entire project on your computer.

### 

[​](https://python.datalumina.com/#what-just-happened)

What just happened?

- Git downloaded all files
- Git downloaded all history
- You can now run, modify, and learn from this code

Always clone into a sensible location. I recommend having a `projects` or `repos` folder in your Documents.

## 

[​](https://python.datalumina.com/#creating-your-own-repository)

Creating your own repository

Let’s put your `python-for-ai` project on GitHub.

**Critical**: Before pushing to GitHub, create a `.gitignore` file! This prevents uploading your `.venv` folder, which can be gigabytes in size and cause push failures.

### 

[​](https://python.datalumina.com/#step-0-create-gitignore-file)

Step 0: Create .gitignore file

Before anything else, create a `.gitignore` file in your project:

```
# .gitignore - tells Git what NOT to track
.venv/
.env
__pycache__/
*.pyc
.DS_Store
```

Save this file in your project root. Git will now ignore these files.

### 

[​](https://python.datalumina.com/#step-1-create-on-github)

Step 1: Create on GitHub

1. Go to [github.com](https://github.com)
2. Click the green “New” button (or + icon > “New repository”)
3. Fill in:
 - **Repository name**: `python-for-ai`
 - **Description**: “Learning Python for AI development”
 - **Public/Private**: Choose Private for now
 - **Don’t** add README, .gitignore, or license
4. Click “Create repository”

### 

[​](https://python.datalumina.com/#step-2-connect-your-local-project)

Step 2: Connect your local project

GitHub will show you commands. Choose based on your authentication method:

- HTTPS (Recommended)
 
- SSH
 

```
# Open Terminal (Mac) or Command Prompt (Windows)
# Navigate to your python-for-ai folder
cd ~/Documents/python-for-ai  # Mac
cd C:\Users\YourName\Documents\python-for-ai  # Windows

# Initialize Git in your project
git init

# Add all your files
git add .

# Create your first commit
git commit -m "Initial commit"

# Rename branch to main
git branch -M main

# Connect to GitHub with HTTPS (use YOUR username)
git remote add origin https://github.com/YOUR-USERNAME/python-for-ai.git

# Push your code
git push -u origin main
```

```
# Open Terminal (Mac) or Command Prompt (Windows)
# Navigate to your python-for-ai folder
cd ~/Documents/python-for-ai  # Mac
cd C:\Users\YourName\Documents\python-for-ai  # Windows

# Initialize Git in your project
git init

# Add all your files
git add .

# Create your first commit
git commit -m "Initial commit"

# Rename branch to main
git branch -M main

# Connect to GitHub with SSH (use YOUR username)
git remote add origin git@github.com:YOUR-USERNAME/python-for-ai.git

# Push your code
git push -u origin main
```

When you push, GitHub will ask for your username and the personal access token (not your password!). VS Code will remember it.

## 

[​](https://python.datalumina.com/#the-daily-workflow)

The daily workflow

Once your project is on GitHub:

```
# Make changes to your code...

# Save changes
git add .
git commit -m "Add new feature"

# Upload to GitHub
git push
```

That’s 90% of what you’ll do with Git!

## 

[​](https://python.datalumina.com/#common-tasks)

Common tasks

Clone with VS Code UI

1. Press `Ctrl/Cmd + Shift + P`
2. Type “Git: Clone”
3. Paste the repository URL
4. Choose where to save it
5. VS Code opens the project automatically

Private vs Public repos

- **Private**: Only you can see it (good for learning)
- **Public**: Anyone can see it (good for portfolio)
- You can change this later in Settings

The .gitignore file

```
# .gitignore - tells Git what NOT to track
.venv/
.env
__pycache__/
*.pyc
.DS_Store
```

Add this file to keep junk out of your repo. The `.venv/` folder can be several gigabytes!

## 

[​](https://python.datalumina.com/#practice-exercise)

Practice exercise

Try this:

1. Clone any Python project that interests you
2. Create a new repo for one of your practice scripts
3. Make a change, commit, and push

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

VS Code makes Git even easier with visual tools. Let’s explore those.

## VS Code Git

Use Git without the terminal

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/tools/git/clone-create.mdx)

[GitHub setup](https://python.datalumina.com/tools/git/github-setup) [VS Code Git](https://python.datalumina.com/tools/git/vscode-git)

⌘I