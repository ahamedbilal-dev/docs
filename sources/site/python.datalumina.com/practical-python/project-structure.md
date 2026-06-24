# Source: https://python.datalumina.com/practical-python/project-structure

## 

[​](https://python.datalumina.com/#working-with-multiple-files)

Working with multiple files

So far, you’ve been writing single Python files. But real projects have multiple files, folders, and resources. Good organization makes your code easier to understand and maintain. Let’s organize your existing `python-for-ai` workspace with a proper structure.

## 

[​](https://python.datalumina.com/#organize-your-workspace)

Organize your workspace

You already have a `python-for-ai` workspace from the beginning of the course. Let’s create a folder for this project:

1. Open your `python-for-ai` workspace in VS Code
2. Create a `sales-analysis` folder
3. Inside `sales-analysis`, create these subfolders:

```
python-for-ai/
├── hello.py              # Your existing practice file
└── sales-analysis/       # New project folder
    ├── data/             # CSV files and data
    └── output/           # Generated files
```

Create folders in VS Code by right-clicking in the Explorer panel and selecting “New Folder”, or click the new folder icon at the top of the Explorer.

## 

[​](https://python.datalumina.com/#create-the-data-file)

Create the data file

Inside your `sales-analysis/data` folder, create a file called `sales.csv`:

```
date,product,quantity,price
2024-01-01,Laptop,2,999.99
2024-01-01,Mouse,5,29.99
2024-01-02,Keyboard,3,79.99
2024-01-02,Monitor,1,299.99
2024-01-03,Laptop,1,999.99
2024-01-03,Mouse,10,29.99
2024-01-04,Keyboard,2,79.99
2024-01-05,Monitor,2,299.99
```

Copy and paste this data into a new file called `sales.csv` in your `data` folder. Make sure the file extension is `.csv`, not `.txt`.

## 

[​](https://python.datalumina.com/#understanding-file-paths)

Understanding file paths

When your code needs to find files, you need to understand paths:

```
# When your script runs from sales-analysis folder
"data/sales.csv"           # Look in the data subfolder
"output/report.json"       # Save to the output subfolder

# Your project structure
# python-for-ai/
#   └── sales-analysis/
#       ├── analyzer.py      <- Your script is here
#       ├── data/sales.csv   <- Your data is here
#       └── output/          <- Results go here
```

## 

[​](https://python.datalumina.com/#create-your-first-script)

Create your first script

In the `sales-analysis` folder (not in a subfolder), create `analyzer.py`:

```
import os

# Check if we're in the right place
print("Current directory:", os.getcwd())

# Check if our data file exists
data_path = "data/sales.csv"
if os.path.exists(data_path):
    print(f"✅ Found {data_path}")
else:
    print(f"❌ Cannot find {data_path}")
    print("Make sure you're running from the sales-analysis folder!")
```

## 

[​](https://python.datalumina.com/#running-your-code)

Running your code

In VS Code, you have two simple ways to run Python code:

### 

[​](https://python.datalumina.com/#option-1-the-play-button)

Option 1: The play button

1. Open `analyzer.py` in VS Code
2. Click the ▶️ (play) button in the top right
3. The code runs and shows output in the terminal below

### 

[​](https://python.datalumina.com/#option-2-interactive-mode-recommended)

Option 2: Interactive mode (recommended)

1. Open `analyzer.py` in VS Code
2. Select the code you want to run (or place cursor on a line)
3. Press **Shift+Enter**
4. Code runs in the interactive window with instant feedback

Interactive mode (Shift+Enter) is great for testing code step by step. You can run one line at a time and see results immediately!

By keeping `analyzer.py` in the same folder as `data` and `output`, the file paths stay simple and work with both the play button and interactive mode.

## 

[​](https://python.datalumina.com/#best-practices)

Best practices

1. **Keep data separate** - Don’t mix code and data files
2. **Use clear names** - `data` for input files, `output` for results
3. **Simple structure** - Keep your main script at the project level
4. **Test as you go** - Use Shift+Enter to run code step by step

## Python paths

Understand how Python finds files

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/practical-python/project-structure.mdx)

[Practical Python](https://python.datalumina.com/practical-python) [Python paths](https://python.datalumina.com/practical-python/python-paths)

⌘I