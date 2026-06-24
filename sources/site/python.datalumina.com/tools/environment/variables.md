# Source: https://python.datalumina.com/tools/environment/variables

## 

[​](https://python.datalumina.com/#what-are-environment-variables)

What are environment variables?

Environment variables are settings stored outside your code. Think of them as configuration that your program can read.

## 

[​](https://python.datalumina.com/#the-problem-they-solve)

The problem they solve

```
# BAD: Never hardcode sensitive data!
api_key = "sk-1234567890abcdef"  # Everyone can see this!
database = "production_database"  # Can't change without editing code
```

Problems:

- Secrets visible in code
- Can’t share code safely
- Different settings for different computers

## 

[​](https://python.datalumina.com/#how-environment-variables-work)

How environment variables work

Environment variables live in your system, not your code:

```
import os

# Read from environment
api_key = os.environ.get('API_KEY')
database = os.environ.get('DATABASE_NAME', 'default.db')

print(f"Using database: {database}")
```

## 

[​](https://python.datalumina.com/#setting-environment-variables)

Setting environment variables

You can set them temporarily in your terminal:

```
# Mac/Linux
export API_KEY=sk-1234567890abcdef
python app.py

# Windows
set API_KEY=sk-1234567890abcdef
python app.py
```

But they disappear when you close the terminal!

## 

[​](https://python.datalumina.com/#reading-in-python)

Reading in Python

```
import os

# Method 1: Get with default
api_key = os.environ.get('API_KEY', 'demo-key')

# Method 2: Check if exists
if 'API_KEY' in os.environ:
    api_key = os.environ['API_KEY']
else:
    print("No API key found")

# Method 3: Will crash if not found
api_key = os.environ['API_KEY']  # KeyError if missing!
```

## 

[​](https://python.datalumina.com/#common-uses)

Common uses

- **API Keys**: `OPENAI_API_KEY`, `GITHUB_TOKEN`
- **Database URLs**: `DATABASE_URL`, `REDIS_URL`
- **App Settings**: `DEBUG=True`, `PORT=8000`
- **File Paths**: `LOG_DIR`, `UPLOAD_FOLDER`

## 

[​](https://python.datalumina.com/#important-notes)

Important notes

- Environment variables are always strings
- Names are UPPERCASE by convention
- They’re different on each computer
- They don’t persist between terminal sessions

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Setting variables manually is tedious. Let’s use `.env` files for a better workflow.

## Using .env files

Easier way to manage variables

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/tools/environment/variables.mdx)

[Environment & secrets](https://python.datalumina.com/tools/environment) [Using .env files](https://python.datalumina.com/tools/environment/dotenv)

⌘I