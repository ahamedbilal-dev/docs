# Source: https://python.datalumina.com/advanced/classes/methods-attributes

## 

[​](https://python.datalumina.com/#attributes-storing-data)

Attributes: storing data

Attributes are variables that belong to an object. There are two types: **Instance attributes** (unique to each object):

```
class APIClient:
    def __init__(self, api_key, base_url):
        self.api_key = api_key      # Each client has its own key
        self.base_url = base_url    # Each client has its own URL
        self.request_count = 0      # Track requests per client

# Creating instances with named arguments
client1 = APIClient(api_key="key1", base_url="https://api1.com")
client2 = APIClient(api_key="key2", base_url="https://api2.com")
```

**Class attributes** (shared by all objects):

```
class APIClient:
    version = "1.0"              # Same for all clients
    max_retries = 3              # Same for all clients
    
    def __init__(self, api_key):
        self.api_key = api_key   # Unique to each client
```

## 

[​](https://python.datalumina.com/#methods-adding-behavior)

Methods: adding behavior

Methods are functions that belong to a class. They always have `self` as the first parameter, but you don’t pass it when calling:

```
class DataValidator:
    def __init__(self):
        self.errors = []
    
    def validate_email(self, email):
        if "@" not in email:
            self.errors.append(f"Invalid email: {email}")
            return False
        return True
    
    def validate_age(self, age):
        if age < 0 or age > 150:
            self.errors.append(f"Invalid age: {age}")
            return False
        return True
    
    def get_errors(self):
        return self.errors

# Use the validator
validator = DataValidator()

# Notice: we don't pass self, just the email
validator.validate_email(email="bad-email")
validator.validate_age(age=200)

# Or using positional arguments
validator.validate_email("another-bad-email")
validator.validate_age(150)

print(validator.get_errors())
# ['Invalid email: bad-email', 'Invalid age: 200', 'Invalid email: another-bad-email']
```

When you call a method like `validator.validate_email("test@example.com")`, Python automatically passes the validator object as `self`. You only provide the other arguments.

## 

[​](https://python.datalumina.com/#common-mistakes)

Common mistakes

Modifying mutable class attributes

```
# Wrong - shared list!
class TodoList:
    items = []  # Class attribute

list1 = TodoList()
list1.items.append("Buy milk")

list2 = TodoList()
print(list2.items)  # ['Buy milk'] - Oops!

# Right - instance attribute
class TodoList:
    def __init__(self):
        self.items = []  # Each instance gets its own
```
Not initializing attributes

```
# Wrong - attribute might not exist
class Counter:
    def increment(self):
        self.count += 1  # Error if count doesn't exist!

# Right - initialize in __init__
class Counter:
    def __init__(self):
        self.count = 0
    
    def increment(self):
        self.count += 1
```

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Let’s explore inheritance - how classes can build on other classes.

## Inheritance

Build on existing classes

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/advanced/classes/methods-attributes.mdx)

[Your first class](https://python.datalumina.com/advanced/classes/first-class) [Inheritance](https://python.datalumina.com/advanced/classes/inheritance)

⌘I