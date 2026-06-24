# Source: https://python.datalumina.com/getting-started/vscode-workspace

## 

[​](https://python.datalumina.com/#create-a-projects-folder)

Create a projects folder

Before we start coding, let’s create a dedicated place for all your Python projects.

Having one folder for all your projects keeps your computer organized and makes it easy to find your code later.

1. **Create a main folder** for all your Python work:
 - **Windows**: Create a folder called `PythonProjects` in your Documents
 - **macOS**: Create a folder called `PythonProjects` in your home directory
 - **Linux**: Create a folder called `PythonProjects` in your home directory
2. **Create your first project folder**:
 - Inside your PythonProjects folder, create a new folder called `python-for-ai` (all lowercase)
 - This will be our learning project for this course

You can name your project folder anything you like, but I usually use lowercase letters with dashes (called “kebab-case”) like `python-for-ai` or `my-first-project`. This matches how projects appear on GitHub (more on that later).

## 

[​](https://python.datalumina.com/#open-folder-in-vs-code)

Open folder in VS Code

Now let’s open this folder in VS Code. There are several ways: **Method 1: From VS Code**

1. Open VS Code
2. Click “File” > “Open Folder” (or press `Ctrl/Cmd + O`)
3. Navigate to your `python-for-ai` folder
4. Click “Select Folder” (Windows) or “Open” (Mac/Linux)

**Method 2: From file explorer**

- **Windows**: Right-click the folder > “Open with Code”
- **macOS**: Drag the folder onto the VS Code icon
- **Linux**: Right-click the folder > “Open with Code”

## 

[​](https://python.datalumina.com/#understanding-the-interface)

Understanding the interface

When you open a folder in VS Code:

- **Left sidebar**: Shows all files in your project (currently empty)
- **Main area**: Where you’ll write code
- **Bottom panel**: Terminal, problems, output
- **Top**: Menu and tabs for open files

VS Code always works with folders, not individual files. This helps it understand your project structure and provide better suggestions.

## 

[​](https://python.datalumina.com/#save-as-workspace)

Save as workspace

A workspace saves your project settings and makes it easy to return to your project later.

1. With your `python-for-ai` folder open, click “File” > “Save Workspace As…”
2. Save it in the same `python-for-ai` folder
3. Name it `python-for-ai.code-workspace`
4. Click “Save”

## 

[​](https://python.datalumina.com/#what’s-a-workspace)

What’s a workspace?

A workspace is like a bookmark for your project. It remembers:

- Which folder you’re working in
- Your editor settings for this project
- Which files you had open
- Your debugging configuration

## 

[​](https://python.datalumina.com/#test-your-workspace)

Test your workspace

Let’s make sure the workspace works:

1. Close VS Code completely
2. Go to your `python-for-ai` folder
3. Double-click the `python-for-ai.code-workspace` file
4. VS Code opens with your project ready!

You can create a desktop shortcut to your workspace file for even quicker access to your project.

## 

[​](https://python.datalumina.com/#project-structure)

Project structure

Your folder should now look like this:

```
PythonProjects/
└── python-for-ai/
    └── python-for-ai.code-workspace
```

We’re ready to create our first Python file!

## Your first Python file

Create and run your first Python program

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/getting-started/vscode-workspace.mdx)

[Install VS Code](https://python.datalumina.com/getting-started/vscode-setup) [First Python file](https://python.datalumina.com/getting-started/first-python-file)

⌘I