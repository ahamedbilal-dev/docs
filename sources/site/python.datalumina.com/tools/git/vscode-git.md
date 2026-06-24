# Source: https://python.datalumina.com/tools/git/vscode-git

## 

[​](https://python.datalumina.com/#git-without-the-terminal)

Git without the terminal

VS Code has Git built in. You can do everything with clicks instead of commands.

## 

[​](https://python.datalumina.com/#the-source-control-panel)

The Source Control panel

Look at the left sidebar in VS Code. You’ll see this icon:

- **Source Control** icon (looks like a branch)
- Shows all your changed files
- One-click commits

## 

[​](https://python.datalumina.com/#basic-workflow)

Basic workflow

### 

[​](https://python.datalumina.com/#1-see-your-changes)

1\. See your changes

Open the Source Control panel:

- Changed files appear under “Changes”
- Click any file to see what changed
- Green lines = added
- Red lines = removed

### 

[​](https://python.datalumina.com/#2-stage-changes)

2\. Stage changes

Before committing, you “stage” files:

- Hover over a file
- Click the **+** icon
- Or click **+** next to “Changes” to stage everything

### 

[​](https://python.datalumina.com/#3-commit)

3\. Commit

Once files are staged:

1. Type a message in the text box
2. Press `Ctrl/Cmd + Enter` (or click ✓)

That’s a commit!

### 

[​](https://python.datalumina.com/#4-push-to-github)

4\. Push to GitHub

After committing:

- Click the **…** menu in Source Control
- Click “Push”
- Or click the sync icon in the bottom status bar

## 

[​](https://python.datalumina.com/#visual-features)

Visual features

### 

[​](https://python.datalumina.com/#see-changes-inline)

See changes inline

- Modified files show a colored bar in the editor
- Click the bar to see what changed
- Blue = modified, Green = added, Red = deleted

## 

[​](https://python.datalumina.com/#common-vs-code-git-tasks)

Common VS Code Git tasks

Initialize a new repo

1. Open your project folder
2. Open Source Control panel
3. Click “Initialize Repository”
4. That’s it! Your project now uses Git

Clone a repository

1. Press `Ctrl/Cmd + Shift + P`
2. Type “Git: Clone”
3. Paste the GitHub URL
4. Choose where to save
5. VS Code opens it automatically

Create a .gitignore

1. Create new file: `.gitignore`
2. VS Code suggests common patterns
3. Or use Python template:

```
.venv/
.env
__pycache__/
*.pyc
.vscode/
.DS_Store
```

Discard changes

Made a mistake? Undo changes:

1. In Source Control panel
2. Right-click the file
3. Select “Discard Changes”
4. Confirms before reverting

## 

[​](https://python.datalumina.com/#sync-button-magic)

Sync button magic

The status bar shows a sync button:

- **↓ 3** means “3 commits to pull”
- **↑ 2** means “2 commits to push”
- Click it to sync everything

## 

[​](https://python.datalumina.com/#tips-for-beginners)

Tips for beginners

1. **Commit often**: Every small feature or fix
2. **Write clear messages**: “Fix login bug” not “changes”
3. **Pull before starting**: Get latest changes first
4. **Don’t commit secrets**: Check your .gitignore

Never commit `.env` files or API keys! Always add them to `.gitignore` first.

## 

[​](https://python.datalumina.com/#terminal-vs-ui)

Terminal vs UI

Both work! Use what feels comfortable:

| Task | Terminal | VS Code UI |
| --- | --- | --- |
| Stage files | `git add .` | Click + icon |
| Commit | `git commit -m "message"` | Type message + Enter |
| Push | `git push` | Click sync |
| Pull | `git pull` | Click sync |

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Now you know Git! Let’s learn about environment variables and keeping secrets safe.

## Environment & secrets

Keep your API keys safe

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/tools/git/vscode-git.mdx)

[Clone and create](https://python.datalumina.com/tools/git/clone-create) [Environment & secrets](https://python.datalumina.com/tools/environment)

⌘I