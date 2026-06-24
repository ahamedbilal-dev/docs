# Source: https://python.datalumina.com/getting-started/vscode-setup

## 

[​](https://python.datalumina.com/#download-vs-code)

Download VS Code

Visual Studio Code is available for all operating systems. The installation is quick and straightforward.

- Windows
 
- macOS
 
- Linux
 

1. Go to [code.visualstudio.com](https://code.visualstudio.com/)
2. Click the big download button (it detects Windows automatically)
3. Run the downloaded installer
4. **Important**: Check these options during installation:
 - ✓ Add “Open with Code” action to Windows Explorer file context menu
 - ✓ Add “Open with Code” action to Windows Explorer directory context menu
 - ✓ Register Code as an editor for supported file types
 - ✓ Add to PATH
5. Click “Next” and “Install”
6. Click “Finish” when done

1. Go to [code.visualstudio.com](https://code.visualstudio.com/)
2. Click the download button (it detects macOS automatically)
3. Open the downloaded `.zip` file
4. Drag **Visual Studio Code** to your **Applications** folder
5. Optional but recommended:
 - Right-click VS Code in Applications
 - Select “Options” > “Keep in Dock”

**First time opening**:

- You might see “Visual Studio Code is from an unidentified developer”
- Go to System Preferences > Security & Privacy
- Click “Open Anyway”

VS Code is available through multiple installation methods:**Ubuntu/Debian** (recommended):

```
# Download the .deb package
wget -O vscode.deb "https://code.visualstudio.com/sha/download?build=stable&os=linux-deb-x64"

# Install it
sudo apt install ./vscode.deb
```

**Snap package** (works on most distributions):

```
sudo snap install code --classic
```

**Other distributions**: Visit [code.visualstudio.com](https://code.visualstudio.com/) and select your package format (.rpm, .tar.gz, etc.)

## 

[​](https://python.datalumina.com/#verify-installation)

Verify installation

Once installed, let’s make sure VS Code is working:

1. Open VS Code:
 - **Windows**: Search “Visual Studio Code” in Start menu
 - **macOS**: Find it in Applications or press `Cmd + Space` and search
 - **Linux**: Type `code` in terminal or find it in your applications menu
2. You should see the Welcome tab
3. The interface should look clean and modern

## 

[​](https://python.datalumina.com/#install-python-extension)

Install Python extension

VS Code needs the [Python extension](https://marketplace.visualstudio.com/items?itemName=ms-python.python) to work properly with Python files:

1. Click the Extensions icon in the left sidebar (it looks like 4 squares)
2. Search for “Python”
3. Find the one by **Microsoft** (it has millions of downloads)
4. Click “Install”
5. Wait for installation to complete

The Python extension adds syntax highlighting, code completion, debugging, and more. It’s essential for Python development.

## 

[​](https://python.datalumina.com/#configure-python-execution)

Configure Python execution

After installing the Python extension, enable this important setting:

1. Open Settings (`Ctrl/Cmd + ,`)
2. Search for “Python Terminal Execute In File Dir”
3. Check the box to enable it

**What this does**: When you run a Python file, VS Code will execute it from the file’s directory instead of your workspace root. **Why I recommend it**: This prevents common path-related errors. For example, if your script reads a file with `open('data.csv')`, it will look for the file in the same folder as your script, which is usually what you want. Without this setting, it would look in your project root instead, causing “file not found” errors.

## 

[​](https://python.datalumina.com/#additional-recommended-extensions)

Additional recommended extensions

While VS Code works great with just the Python extension, here are a few more I recommend:

### 

[​](https://python.datalumina.com/#pylance)

Pylance

- Search for “Pylance” by Microsoft
- Provides even better code completion and error detection
- Works alongside the Python extension

### 

[​](https://python.datalumina.com/#jupyter)

Jupyter

- Search for “Jupyter” by Microsoft
- Enables interactive Python mode (we’ll use this later)
- Essential for data science and AI work

## 

[​](https://python.datalumina.com/#customize-appearance-optional)

Customize appearance (optional)

I’ve been using these settings for years - they’re easy on the eyes:

### 

[​](https://python.datalumina.com/#theme)

Theme

- Install “Atom One Dark Theme”
- Press `Ctrl/Cmd + K`, then `Ctrl/Cmd + T` to select it

### 

[​](https://python.datalumina.com/#icons)

Icons

- Install “Material Icon Theme” by Philipp Kief
- Makes file types easier to recognize

### 

[​](https://python.datalumina.com/#tree-indentation)

Tree indentation

- Open Settings (`Ctrl/Cmd + ,`)
- Search for “tree indent”
- Change from 8 to 20 for clearer folder structure

**View keyboard shortcuts**: Open Command Palette (`Ctrl/Cmd + Shift + P`) and search “keyboard shortcuts”. You can search for any command and change its shortcut by clicking the pencil icon.

## 

[​](https://python.datalumina.com/#check-python-detection)

Check Python detection

After setting up VS Code:

1. Press `Ctrl + Shift + P` (Windows/Linux) or `Cmd + Shift + P` (macOS)
2. Type “Python: Select Interpreter”
3. You should see your Python installation listed
4. If not, we’ll fix this in the next section

## Create a workspace

Learn how to organize your Python projects

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/getting-started/vscode-setup.mdx)

[Why VS Code](https://python.datalumina.com/getting-started/vscode-introduction) [Creating projects](https://python.datalumina.com/getting-started/vscode-workspace)

⌘I