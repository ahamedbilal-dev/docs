# Source: https://python.datalumina.com/advanced/classes/first-class

## 

[​](https://python.datalumina.com/#how-classes-work)

How classes work

Working with classes follows a simple pattern:

1. **Define the class** - Create a blueprint with the `class` keyword
2. **Add an `__init__` method** - Set up initial data when objects are created
3. **Create instances** - Make actual objects from your class
4. **Access the data** - Use the attributes you defined

Let’s go through each step to build your first class.

## 

[​](https://python.datalumina.com/#basic-class-structure)

Basic class structure

Every class starts with the `class` keyword:

```
class Dog:  # Note: class names use PascalCase
    pass  # Empty class
```

## 

[​](https://python.datalumina.com/#adding-an-initializer)

Adding an initializer

The `__init__` method runs when you create a new object:

```
class Dog:
    def __init__(self, name, breed):
        self.name = name
        self.breed = breed

# Create dog objects - using positional arguments
dog1 = Dog("Buddy", "Golden Retriever")
dog2 = Dog("Max", "Beagle")

# Or with named arguments (clearer)
dog3 = Dog(name="Charlie", breed="Poodle")

print(dog1.name)   # Buddy
print(dog2.breed)  # Beagle
```

Yes, `__init__` looks weird with those double underscores! This is called a “dunder” method (double underscore). It’s just how Python works - you’ll need to type it exactly like this. Don’t worry, after writing it a few times it becomes second nature. Think of it as Python’s special way of saying “this is the setup method”.

## 

[​](https://python.datalumina.com/#understanding-self)

Understanding self

`self` refers to the current object. It’s how an object keeps track of its own data:

When defining methods in a class, you always include `self` as the first parameter. But when calling the method, you don’t pass it - Python does that automatically!

```
class Dog:
    def __init__(self, name):
        self.name = name  # self.name belongs to this specific dog

# Using positional argument
dog1 = Dog("Buddy")

# Using named argument (same result)
dog2 = Dog(name="Max")

# Each dog has its own name
print(dog1.name)  # Buddy
print(dog2.name)  # Max
```

## 

[​](https://python.datalumina.com/#real-world-example-configuration)

Real-world example: configuration

Here’s a practical class for AI engineering:

```
class APIConfig:
    def __init__(self, api_key, model="gpt-3.5-turbo", max_tokens=100):
        self.api_key = api_key
        self.model = model
        self.max_tokens = max_tokens
        self.base_url = "https://api.openai.com/v1"

# Create different configurations
# Using positional for required arg, named for optional
dev_config = APIConfig("sk-dev-key", max_tokens=50)

# Using all named arguments (clearest)
prod_config = APIConfig(api_key="sk-prod-key", model="gpt-4", max_tokens=1000)

# Access the configuration
print(dev_config.model)        # gpt-3.5-turbo
print(prod_config.model)       # gpt-4
print(prod_config.max_tokens)  # 1000
```

## 

[​](https://python.datalumina.com/#class-vs-instance)

Class vs instance

- **Class**: The blueprint (like a recipe)
- **Instance/Object**: What you create from the class (like a cake from the recipe)

```
# APIConfig is the class
# config1 and config2 are instances
config1 = APIConfig(api_key="key1", max_tokens=50)
config2 = APIConfig(api_key="key2", max_tokens=200)

# Each instance has its own data
print(config1.max_tokens)  # 50
print(config2.max_tokens)  # 200

# Changing one doesn't affect the other
config1.max_tokens = 75
print(config1.max_tokens)  # 75
print(config2.max_tokens)  # 200 (unchanged)
```

Always use clear, descriptive names for your classes. In Python, class names use PascalCase (like `TextProcessor` or `DataLoader`), while variable names use snake\_case (like `text_processor` or `data_loader`).

## 

[​](https://python.datalumina.com/#common-mistakes)

Common mistakes

Forgetting self in \_\_init\_\_

```
# Wrong - forgot self parameter
class Dog:
    def __init__(name):  # Missing self!
        name = name

# Right - include self
class Dog:
    def __init__(self, name):
        self.name = name
```
Not using self for attributes

```
# Wrong - creates local variable
class Dog:
    def __init__(self, name):
        name = name  # Just a local variable!

# Right - use self
class Dog:
    def __init__(self, name):
        self.name = name  # Instance attribute
```
Forgetting parentheses when creating instance

```
# Wrong - assigns the class itself
my_config = APIConfig  # Not an instance!

# Right - call with parentheses
my_config = APIConfig(api_key="api-key")  # Creates instance
```
Modifying class instead of instance

```
# Wrong - modifies the class
class Counter:
    count = 0

c1 = Counter()
c1.count += 1  # This affects the class!

# Right - instance attribute
class Counter:
    def __init__(self):
        self.count = 0  # Each instance gets its own
```

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Now that you understand how to create classes and store data in them, let’s learn how to add behavior with methods.

[**Methods and attributes**\\ \\ Add behavior to your classes](https://python.datalumina.com/advanced/classes/methods-attributes)

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/advanced/classes/first-class.mdx)

[Classes](https://python.datalumina.com/advanced/classes) [Methods and attributes](https://python.datalumina.com/advanced/classes/methods-attributes)

Ctrl+I