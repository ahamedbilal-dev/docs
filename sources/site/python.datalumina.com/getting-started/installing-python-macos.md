# Source: https://python.datalumina.com/getting-started/installing-python-macos

## 

[​](https://python.datalumina.com/#check-existing-python)

Check existing Python

macOS includes an older Python version for system use. Let’s check what you have:

1. Open Terminal:
 - Press `Cmd + Space` to open Spotlight
 - Type “Terminal” and press Enter
 - Or find Terminal in Applications > Utilities
2. Check Python version:

```
python3 --version
```

If you see a recent Python 3 version, you might already be set!

Some Mac users can use just `python` instead of `python3`, but this depends on your system configuration. When in doubt, use `python3`.

## 

[​](https://python.datalumina.com/#download-python)

Download Python

1. Go to [python.org/downloads](https://www.python.org/downloads/)
2. The site will detect you’re on macOS and show the latest version
3. Click the download button to get the `.pkg` installer

Always download from python.org to ensure you get the official, secure version.

## 

[​](https://python.datalumina.com/#install-python)

Install Python

1. Open the downloaded `.pkg` file
2. The Python installer will open
3. Click “Continue” through the introduction and license screens
4. Click “Agree” to accept the license
5. Click “Install” (you’ll need to enter your Mac password)
6. Wait for installation to complete
7. Click “Close” when you see “The installation was successful”

## 

[​](https://python.datalumina.com/#verify-installation)

Verify installation

Open a **new** Terminal window (important!) and check the version:

```
python3 --version
```

You should see the version you just installed. The exact number depends on when you download.

## 

[​](https://python.datalumina.com/#test-python)

Test Python

Let’s make sure Python works properly:

1. In Terminal, type:

```
python3
```

2. You’ll see something like:

```
Python 3.13.5 (v3.13.5:0fa1754080, Jul 29 2025, 09:45:56) [Clang 15.0.0] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

3. Try your first Python command:

```
print("Hello from Python!")
```

4. Press `Enter` and you should see:

```
Hello from Python!
```

5. To exit Python:
 - Type `exit()` and press Enter
 - Or press `Ctrl + D`

## 

[​](https://python.datalumina.com/#troubleshooting)

Troubleshooting

'python3' command not found

The Terminal might not see the new installation yet. 
 
**Solution 1**: Close Terminal completely and open a new window. 
 
**Solution 2**: Check if Python is installed but not in PATH:

```
ls /Library/Frameworks/Python.framework/Versions/
```

**Solution 3**: Add Python to your PATH manually:

```
echo 'export PATH="/Library/Frameworks/Python.framework/Versions/Current/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```
'python' command doesn't work

This is normal on macOS. You have three options: 
 
**Option 1**: Always use `python3` (recommended) 
 
**Option 2**: Create an alias:

```
echo 'alias python=python3' >> ~/.zshrc
echo 'alias pip=pip3' >> ~/.zshrc
source ~/.zshrc
```

**Option 3**: Check if the installer created a `python` link:

```
which python
```
SSL/Certificate errors

You forgot to install certificates. Fix it by 
 
Running from Terminal:

```
/Applications/Python\ 3.*/Install\ Certificates.command
```

Or manually installing certificates:

```
pip3 install --upgrade certifi
```
Multiple Python versions

macOS can have multiple Python versions. To manage them: 
 
**See all installed versions**:

```
ls -la /usr/local/bin/python*
```

**Use a specific version**:

```
python3.13 --version
python3.12 --version
```

**Set a default** (example for 3.13):

```
ln -s -f /usr/local/bin/python3.13 /usr/local/bin/python3
```

## 

[​](https://python.datalumina.com/#alternative-homebrew-installation)

Alternative: Homebrew installation

If you prefer using a package manager:

1

Install Homebrew

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

2

Install Python

```
brew install python@3
```

3

Verify installation

```
python3 --version
```

Homebrew Python might use different paths than the official installer. Both work fine.

## 

[​](https://python.datalumina.com/#next-steps)

Next steps

Perfect! Python is now installed on your Mac. Let’s set up your code editor.

## Continue to VS Code introduction

Install and configure Visual Studio Code

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/getting-started/installing-python-macos.mdx)

[Install on Windows](https://python.datalumina.com/getting-started/installing-python-windows) [Install on Linux](https://python.datalumina.com/getting-started/installing-python-linux)

⌘I