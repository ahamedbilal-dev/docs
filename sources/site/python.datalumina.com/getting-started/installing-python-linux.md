# Source: https://python.datalumina.com/getting-started/installing-python-linux

## 

[​](https://python.datalumina.com/#check-existing-python)

Check existing Python

Most Linux distributions come with Python pre-installed. Let’s check:

```
python3 --version
```

If you see a recent Python 3 version, you’re ready! Most modern Linux distributions include Python 3.

Linux uses `python3` to distinguish from the older Python 2. Some distributions let you use just `python`, but `python3` always works.

## 

[​](https://python.datalumina.com/#install-or-update-python)

Install or update Python

Choose your Linux distribution below:

- Ubuntu/Debian
 
- Fedora/RHEL/CentOS
 
- Arch/Manjaro
 
- openSUSE
 
- Alpine
 

### 

[​](https://python.datalumina.com/#update-package-lists)

Update package lists

```
sudo apt update
```

### 

[​](https://python.datalumina.com/#install-python-and-essential-tools)

Install Python and essential tools

```
sudo apt install python3 python3-pip python3-venv
```

### 

[​](https://python.datalumina.com/#install-development-headers-for-compiling-packages)

Install development headers (for compiling packages)

```
sudo apt install python3-dev build-essential
```

### 

[​](https://python.datalumina.com/#for-the-latest-python-version)

For the latest Python version

If your distribution doesn’t have the latest Python:

```
# Add the deadsnakes PPA
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update

# Install specific version (example: 3.13)
sudo apt install python3.13 python3.13-venv python3.13-dev
```

### 

[​](https://python.datalumina.com/#install-python-and-pip)

Install Python and pip

```
sudo dnf install python3 python3-pip python3-devel
```

### 

[​](https://python.datalumina.com/#install-compilation-tools)

Install compilation tools

```
sudo dnf groupinstall "Development Tools"
```

### 

[​](https://python.datalumina.com/#for-newer-python-versions)

For newer Python versions

```
# Check available versions
dnf search python3

# Install specific version
sudo dnf install python3.13
```

### 

[​](https://python.datalumina.com/#python-is-usually-pre-installed)

Python is usually pre-installed

```
# If needed, install Python
sudo pacman -S python python-pip
```

### 

[​](https://python.datalumina.com/#install-base-development-tools)

Install base development tools

```
sudo pacman -S base-devel
```

### 

[​](https://python.datalumina.com/#for-specific-versions)

For specific versions

```
# Search available versions
pacman -Ss python3

# Install from AUR if needed
yay -S python313
```

### 

[​](https://python.datalumina.com/#install-python-and-pip-2)

Install Python and pip

```
sudo zypper install python3 python3-pip python3-devel
```

### 

[​](https://python.datalumina.com/#install-development-pattern)

Install development pattern

```
sudo zypper install -t pattern devel_basis
```

### 

[​](https://python.datalumina.com/#install-python-and-pip-3)

Install Python and pip

```
apk add python3 py3-pip python3-dev
```

### 

[​](https://python.datalumina.com/#install-build-tools)

Install build tools

```
apk add build-base
```

## 

[​](https://python.datalumina.com/#verify-installation)

Verify installation

Check that Python and pip are installed:

```
python3 --version
pip3 --version
```

You should see version numbers for both.

## 

[​](https://python.datalumina.com/#test-python)

Test Python

1. Start Python:

```
python3
```

2. You’ll see the Python prompt:

```
Python 3.13.5 (main, Jul 29 2025, 12:03:01) [GCC 11.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

3. Try a simple command:

```
print("Hello from Linux!")
```

4. Exit Python:
 - Type `exit()` or press `Ctrl + D`

## 

[​](https://python.datalumina.com/#troubleshooting)

Troubleshooting

Permission denied

**For system packages**: Always use `sudo`:

```
sudo apt install python3-pip
```

**For pip packages**: Install in user space:

```
pip3 install --user package-name
```

**Best practice**: Use virtual environments to avoid permission issues entirely.

python3: command not found

Python isn’t installed. Install it using your package manager:

```
# Ubuntu/Debian
sudo apt update && sudo apt install python3

# Fedora
sudo dnf install python3

# Arch
sudo pacman -S python
```
pip3: command not found

pip isn’t installed. Fix it.

```
# Ubuntu/Debian
sudo apt install python3-pip

# Fedora
sudo dnf install python3-pip

# From Python
python3 -m ensurepip
```

Outdated Python version

Your distribution has an old Python. Options: 
 
**Option 1**: Use deadsnakes PPA (Ubuntu/Debian):

```
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
sudo apt install python3.13
```

**Option 2**: Compile from source:

```
# Install dependencies
sudo apt install build-essential zlib1g-dev libncurses5-dev \
  libgdbm-dev libnss3-dev libssl-dev libreadline-dev \
  libffi-dev libsqlite3-dev wget libbz2-dev

# Download and compile
wget https://www.python.org/ftp/python/3.13.5/Python-3.13.5.tgz
tar -xf Python-3.13.5.tgz
cd Python-3.13.5
./configure --enable-optimizations
make -j $(nproc)
sudo make altinstall
```

**Option 3**: Use pyenv for version management 
 

externally-managed-environment error

Modern Linux prevents pip from installing system-wide. Solutions: 
 
**Use virtual environments** (recommended):

```
python3 -m venv myenv
source myenv/bin/activate
pip install package-name
```

**Install in user directory**:

```
pip3 install --user package-name
```

**Use pipx for applications**:

```
sudo apt install pipx
pipx install application-name
```

## 

[​](https://python.datalumina.com/#next-steps)

Next steps

Great! Python is ready on your Linux system. Let’s set up your development environment.

## Continue to VS Code introduction

Install and configure Visual Studio Code

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/getting-started/installing-python-linux.mdx)

[Install on macOS](https://python.datalumina.com/getting-started/installing-python-macos) [Why VS Code](https://python.datalumina.com/getting-started/vscode-introduction)

⌘I