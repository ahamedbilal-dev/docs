# Source: https://python.datalumina.com/getting-started/first-python-file

## 

[​](https://python.datalumina.com/#create-a-new-file)

Create a new file

With your `python-for-ai` project open in VS Code:

1. Click the “New File” button in the Explorer (looks like a page with a +)
2. Name it `hello.py`
3. Press Enter

Make sure to include the `.py` extension! This tells VS Code and Python that this is a Python file.

## 

[​](https://python.datalumina.com/#understanding-file-extensions)

Understanding file extensions

File extensions tell your computer and VS Code what type of file you’re working with. There are many files type, here are some examples:

- `.txt` - Plain text file, no special formatting
- `.md` - Markdown file, for documentation
- `.py` - Python file, contains Python code

When you save a file with `.py`, VS Code:

- Adds syntax highlighting (colors your code)
- Enables Python-specific features
- Shows Python in the bottom-right corner

## 

[​](https://python.datalumina.com/#write-your-first-program)

Write your first program

In your `hello.py` file, type:

```
print("Hello, World!")
print("I'm learning Python for AI")
```

The `print()` function displays text or values on your screen - we’ll use it throughout this course to see what our code is doing.

Notice how VS Code colors your code:

- `print` is highlighted as a function
- Text in quotes is shown in a different color
- This helps you spot errors quickly

## 

[​](https://python.datalumina.com/#select-python-interpreter)

Select Python interpreter

Before running your code, make sure VS Code is using the right Python:

1. Look at the bottom-right corner of VS Code
2. You should see something like “Python 3.x.x”
3. If not, click the area that says “Select Python Interpreter”
4. Choose the Python version you installed earlier

We’re using the main Python installation for now. Later in the course, you’ll learn about virtual environments for more advanced project management.

## 

[​](https://python.datalumina.com/#run-your-program)

Run your program

There are three ways to run your Python code: **Method 1: Run button** (easiest)

- Click the triangle “Run” button in the top-right corner
- Or select the down arrow next to it and select “Run Python File”

**Method 2: Right-click menu**

- Right-click anywhere in your code
- Select “Run Python File in Terminal”

**Method 3: Keyboard shortcut**

- Press `Ctrl + F5` (Windows/Linux) or `Cmd + F5` (macOS)

## 

[​](https://python.datalumina.com/#understanding-the-output)

Understanding the output

When you run your code, the terminal opens at the bottom. You’ll see something like this (yours will look slightly different):

```
cd /path/to/your/project
/path/to/python /path/to/your/project/hello.py
Hello, World!
I'm learning Python for AI
```

What’s happening here:

1. **First line**: VS Code navigates to your project folder
2. **Second line**: VS Code runs Python with the full path to your file
3. **Following lines**: Your program’s output!

Don’t worry about the long paths - VS Code handles all of this automatically. The important part is seeing your output: “Hello, World!”

## 

[​](https://python.datalumina.com/#what’s-happening-behind-the-scenes)

What’s happening behind the scenes?

When you click the “Run” button in VS Code, it’s actually running a command in the terminal for you. Let’s understand what’s really happening:

### 

[​](https://python.datalumina.com/#the-basic-command)

The basic command

At its core, running a Python file is simple:

```
python hello.py
```

This tells your computer:

1. **python** - Find the Python program
2. **hello.py** - Open this file and execute the code inside

### 

[​](https://python.datalumina.com/#how-python-executes-your-code)

How Python executes your code

Here’s what happens when you run `python hello.py`:

1. **Python reads your file** - Opens `hello.py` and reads the text
2. **Python interprets the code** - Converts your code into instructions the computer understands
3. **Python executes line by line** - Runs each instruction from top to bottom, left to right
4. **Output appears in terminal** - Any `print()` statements display their results

Python always executes code **top to bottom** (one line after another) and **left to right** (within each line). This means the order of your code matters!

```
print("Hello, World!")  # Line 1: Python reads this
                        # Python converts it to machine instructions
                        # Python executes: display "Hello, World!"
                        # You see: Hello, World!

print("I'm learning Python")  # Line 2: Same process
```

This execution order means:

- Line 2 can’t run before Line 1
- What you write first happens first
- Later in the course, you’ll see how to control this flow with conditions and loops

### 

[​](https://python.datalumina.com/#running-manually-from-the-terminal)

Running manually from the terminal

You can run Python files directly in the terminal without using VS Code’s button:

```
# Make sure you're in the same folder as your file
python hello.py
```

Or with the full path:

```
# You can run from anywhere if you use the full path
python /Users/yourname/python-for-ai/hello.py
```

VS Code’s “Run” button is just a convenient way to run `python your_file.py` in the terminal. The underlying process is exactly the same!

### 

[​](https://python.datalumina.com/#python-vs-python3)

Python vs python3

On some systems (especially Mac/Linux), you might need to use `python3` instead of `python`:

```
python3 hello.py
```

This ensures you’re using Python 3.x instead of the older Python 2.x. VS Code usually handles this automatically.

### 

[​](https://python.datalumina.com/#why-this-matters)

Why this matters

Understanding this is important because:

- You can run Python files from any terminal, not just VS Code
- You’ll see these commands in tutorials and documentation
- Later, you’ll pass arguments to your programs: `python script.py --option value`
- This is how Python works everywhere: on servers, in production, in automation scripts

Think of VS Code as a fancy wrapper around the terminal. When you click “Run,” you’re really just typing `python hello.py` into the terminal. VS Code makes it easier, but the fundamentals stay the same.

## 

[​](https://python.datalumina.com/#the-integrated-terminal)

The integrated terminal

The terminal at the bottom is the same as your system’s terminal, but inside VS Code. Here’s how to work with it:

### 

[​](https://python.datalumina.com/#opening-and-closing-the-terminal)

Opening and closing the terminal

- **Open**: View > Terminal (or press `` Ctrl + ` `` on Windows/Linux, `` Cmd + ` `` on macOS)
-   **Hide**: Click the X or press the same shortcut again
-   **New terminal**: Click the + button or Terminal > New Terminal

### 

[​](https://python.datalumina.com/#terminal-basics)

Terminal basics

-   You can type commands directly
-   Try typing `python --version` and press Enter
-   Type `cls` (Windows) or `clear` (Mac/Linux) to clear the screen
-   Use the up arrow to recall previous commands

The integrated terminal means you never have to leave VS Code. You can write code, run it, install packages, and manage files all in one place.

## 

[​](https://python.datalumina.com/#experiment)

Experiment

Try changing your code and running it again:

```
print("Hello, World!")
print("I'm learning Python for AI")
print("My name is [Your Name]")
print("Today is a great day to code!")
```

Each `print()` statement creates a new line of output.

## 

[​](https://python.datalumina.com/#save-your-work)

Save your work

Remember to save your file:

-   Press `Ctrl + S` (Windows/Linux) or `Cmd + S` (macOS)
- Or use File > Save

VS Code shows a dot next to unsaved files in the tab.

## 

[​](https://python.datalumina.com/#what-you’ve-learned)

What you’ve learned

Congratulations! You’ve:

- Created your first Python file
- Written Python code
- Selected the Python interpreter
- Run a Python program
- Understood the terminal output

This is the foundation for everything else you’ll learn in Python.

[**Course resources**\\ \\ Download all templates, files, and cheat sheets](https://python.datalumina.com/getting-started/course-resources)

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/getting-started/first-python-file.mdx)

[Creating projects](https://python.datalumina.com/getting-started/vscode-workspace) [Course resources](https://python.datalumina.com/getting-started/course-resources)

Ctrl+I