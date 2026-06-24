# Source: https://python.datalumina.com/advanced/classes

## 

[​](https://python.datalumina.com/#what-is-object-oriented-programming)

What is object-oriented programming?

Object-oriented programming (OOP) is a way to organize code by grouping related data and functions together. Instead of having separate variables and functions scattered around, you bundle them into objects. Think of it like organizing a toolbox:

- **Without OOP**: Tools scattered everywhere
- **With OOP**: Tools organized in labeled compartments

Classes are a more advanced Python concept. Don’t worry if they feel confusing at first - they’ll click with practice. Many Python programs work perfectly fine without classes, but they become valuable as your projects grow.

## 

[​](https://python.datalumina.com/#what-is-a-class)

What is a class?

A class is a blueprint for creating objects. It defines:

- **Attributes**: What data the object stores
- **Methods**: What the object can do

```
# Without classes - data and functions separate
name = "OpenAI"
model = "gpt-4o-mini"

def generate_response(prompt):
    # Process prompt...
    return response

# With classes - everything bundled together
class OpenAIClient:
    def __init__(self, name, model):
        self.name = name
        self.model = model
    
    def generate_response(self, prompt):
        # Process prompt...
        return response
```

## 

[​](https://python.datalumina.com/#why-use-classes)

Why use classes?

Classes help you write more understandable programs as they grow. Here’s the typical progression of a Python developer: **1\. Single file scripts** (where you started):

```
# everything.py - All code in one file
api_key = "sk-..."
prompt = "Explain Python"
response = make_api_call(api_key, prompt)
print(response)
```

**2\. Functions** (where you are now):

```
# main.py - Organized with functions
def setup_api(key):
    return {"key": key, "base_url": "https://api.openai.com"}

def generate_response(api_config, prompt):
    # Make API call
    return response

api = setup_api("sk-...")
result = generate_response(api, "Explain Python")
```

**3\. Multiple files** (getting organized):

```
# api_utils.py
def setup_api(key):
    return {"key": key, "base_url": "https://api.openai.com"}

# main.py
from api_utils import setup_api
api = setup_api("sk-...")
```

**4\. Classes** (where we are now):

```
# client.py
class OpenAIClient:
    def __init__(self, api_key):
        self.api_key = api_key
        self.base_url = "https://api.openai.com"
    
    def generate(self, prompt):
        # All logic encapsulated here
        return response

# main.py
from client import OpenAIClient
client = OpenAIClient("sk-...")
response = client.generate("Explain Python")
```

**In the context of AI**, classes specifically help you:

- Build clean interfaces to APIs
- Manage complex data pipelines
- Create reusable components
- Organize stateful operations

[**Your first class**\\ \\ Create a simple class](https://python.datalumina.com/advanced/classes/first-class)

[**Methods and attributes**\\ \\ Add functionality to classes](https://python.datalumina.com/advanced/classes/methods-attributes)

[**Inheritance**\\ \\ Build on existing classes](https://python.datalumina.com/advanced/classes/inheritance)

[**When to use classes**\\ \\ Best practices and guidelines](https://python.datalumina.com/advanced/classes/when-to-use)

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/advanced/classes/index.mdx)

[Common errors](https://python.datalumina.com/advanced/error-handling/common-errors) [Your first class](https://python.datalumina.com/advanced/classes/first-class)

Ctrl+I