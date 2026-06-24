# Source: https://python.datalumina.com/tools/environment/dotenv

## 

[​](https://python.datalumina.com/#what-is-a-env-file)

What is a .env file?

A `.env` file is a simple text file that stores your environment variables. Instead of typing `export` commands, you write them once in a file.

## 

[​](https://python.datalumina.com/#basic-setup)

Basic setup

### 

[​](https://python.datalumina.com/#1-install-python-dotenv)

1\. Install python-dotenv

```
pip install python-dotenv
```

### 

[​](https://python.datalumina.com/#2-create-env-file)

2\. Create .env file

Create a file named `.env` in your project:

```
# .env
API_KEY=sk-1234567890abcdef
DATABASE_URL=sqlite:///myapp.db
DEBUG=True
```

### 

[​](https://python.datalumina.com/#3-load-in-python)

3\. Load in Python

```
from dotenv import load_dotenv
import os

# Load the .env file
load_dotenv()

# Now use your variables
api_key = os.environ.get('API_KEY')
debug = os.environ.get('DEBUG')

print(f"API Key: {api_key}")
print(f"Debug mode: {debug}")
```

That’s it! Much easier than export commands.

## 

[​](https://python.datalumina.com/#critical-add-to-gitignore)

Critical: Add to .gitignore

**Never commit .env files!** They contain secrets. Add to `.gitignore` immediately:

```
# .gitignore
.env
.venv/
__pycache__/
```

## 

[​](https://python.datalumina.com/#complete-example)

Complete example

Here’s a real example with an API:

```
# app.py
from dotenv import load_dotenv
import os
import requests

# Load environment variables
load_dotenv()

# Get API key
API_KEY = os.environ.get('OPENAI_API_KEY')

if not API_KEY:
    print("Please set OPENAI_API_KEY in .env file")
    exit(1)

# Use the API
headers = {"Authorization": f"Bearer {API_KEY}"}
# Make your API calls...
```

Your `.env` file:

```
# .env
OPENAI_API_KEY=sk-your-actual-key-here
MODEL=gpt-3.5-turbo
MAX_TOKENS=100
```

## 

[​](https://python.datalumina.com/#show-others-what-they-need)

Show others what they need

Create `.env.example` (this one you DO commit):

```
# .env.example
OPENAI_API_KEY=your-api-key-here
MODEL=gpt-3.5-turbo
MAX_TOKENS=100
```

This shows other developers what variables they need without exposing your actual keys.

## 

[​](https://python.datalumina.com/#rules-for-env-files)

Rules for .env files

- One variable per line
- No spaces around `=`
- No quotes (unless part of the value)
- Use `#` for comments
- Always UPPERCASE names

## 

[​](https://python.datalumina.com/#common-patterns)

Common patterns

```
# API Keys
OPENAI_API_KEY=sk-...
GITHUB_TOKEN=ghp_...

# Database
DATABASE_URL=sqlite:///local.db

# Settings
DEBUG=True
PORT=8000
LOG_LEVEL=INFO
```

## 

[​](https://python.datalumina.com/#quick-tips)

Quick tips

1. **Load early**: Put `load_dotenv()` at the start of your program
2. **Use defaults**: `os.environ.get('PORT', '8000')`
3. **Check your .gitignore**: Make sure `.env` is listed
4. **Keep it simple**: Only put configuration that changes

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

You now know how to manage secrets safely! Ready for modern Python tooling?

[**Modern Python**\\ \\ Next-level Python development](https://python.datalumina.com/tools/dependencies/index)

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/tools/environment/dotenv.mdx)

[Environment variables](https://python.datalumina.com/tools/environment/variables) [Formatting with Ruff](https://python.datalumina.com/tools/code-quality)

Ctrl+I